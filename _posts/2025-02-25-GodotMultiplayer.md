---
title: Learning To Make Multiplayer Games In Godot
date: 2025-02-25 21:49:00 +0600
categories: [Game Dev, Godot]
tags: [game-development, game, networking, multiplayer, godot]
image:
    path: assets/img/GodotMultiplayer.png
---

I've always heard that if you wanted to make a multiplayer game, you shouldn't start with making a singleplayer game because nearly the entire codebase would need to be rewritten when you moved to multiplayer. This advice, paired with the fact that I already sucked at finishing smaller singleplayer projects, led me to never touch multiplayer.

I think this is fair advice for full-time game devs (or anyone on a strict time budget) but **horrible** advice for hobbyist.

So for no reason at all, let's learn how to make a multiplayer game using examples in Godot!

[Here's the repo if you're impatient](https://github.com/TraySimpson/godot-multiplayer-testing) :)

### The Goal

For this test game, I wanted to make a simple chatroom where you could move your character around and type horrible messages that would appear above your head for a short time before disappearing.

Basically I'm ripping off Club Penguin.

After that, I also added a paintball gun that could be used to shoot other players or paint patterns over the map, allowing for group drawing sessions (which definitely wouldn't be abused).

### The Basics

Godot has some excellent resources for learning multiplayer that I'll link at the bottom of this page, but I'll briefly touch on the 3 main components that handle multiplayer:

1. **MultiplayerSpawner**: This node can be added to a scene to synchronize when scenes are instantiated, so that all peers have the same nodes
2. **MultiplayerSynchronizer**: This node can be added to any scene to synchronize specific *public* properties (using the `@export` annotation) of the attached scene
3. **@rpc annotation**: This can be added above any function to allow it to be called as a Remote Procedure Call. 

RPC functions can be called:
- Just on the server by checking `multiplayer.is_server()` in the function
- On all peers including the caller using the `"call_local"` option
- On a specific peer using `rpc_id(<some-peer-id>)` instead of just `.rpc()`
- On all peers except the caller, which is the default behavior

### The Secret Sauce

Here's the biggest points I learned:

- The `multiplayer_authority` on a node needs to match on all peers and is **not** automatically synchronized
- The "Spawn" sync option for `MultiplayerSynchronizer` is applied when the scene is added to the tree, usually with `add_child()` (so you can set props after instantiation)
- When creating scenes with the `MultiplayerSpawner`, ensure you use the force_readable_name option when adding to the tree by calling `add_child(<your-node>, true)`. This avoids errors when calling on other peers
- RPCs don't automatically serialize complex data structures. This is annoying since `MultiplayerSynchronizer` does this for you

99% of the time, clients should just make RPC calls to the server to instantiate/update scenes that are controlled by MultiplayerSpawners/MultiplayerSynchronizer. This ensures they automatically get reflected to other peers. The 1% scenario is if you truly want your peers to have authority over specific scenes. This can be viable, but opens the door to cheating

### Good Resources

- [Godot Docs: High-level multiplayer](https://docs.godotengine.org/en/stable/tutorials/networking/high_level_multiplayer.html)
- [Godot Blog: Scene Replication](https://godotengine.org/article/multiplayer-in-godot-4-0-scene-replication/) - don't follow too closely for examples, but gives good overview of `MultiplayerSpawner`, `MultiplayerSynchronizer`, and the `@rpc` annotation
- [Godot Example Projects (GitHub)](https://github.com/godotengine/godot-demo-projects) - specifically the `networking/multiplayer_bomber` project
- [clumsy](https://jagt.github.io/clumsy/index.html) - great Windows tool for faking network latency, packet loss, etc
