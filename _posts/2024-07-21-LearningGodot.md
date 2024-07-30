---
title: Learning Godot
date: 2024-07-21 19:32:00 +0600
categories: [Game Dev]
tags: [godot, gdscript, game-development, engine]
---

### Background
Over the last few years, I've always used Unity to prototype different game ideas or simulations. However, given their recent [stunt trying to charge users per install](https://www.wired.com/story/unity-walks-back-policies-lost-trust/), I decided it was time to learn something new.

Currently, the most popular alternatives to Unity are the 3D behemoth Unreal Engine and the free-and-open-source Godot. Given that I'm currently wanting to work on smaller-scoped 2D games, I decided to give Godot a try.

### Approach
I started by diving straight into Godot's documentation and [Getting Started](https://docs.godotengine.org/en/stable/getting_started/introduction/introduction_to_godot.html#what-is-godot) tutorials. This walked me through installation, basic concepts of the engine, and finally creating my own example game.

I was really impressed with how lightweight the engine is. After unzipping, the entire executable is barely over 100MB. Compared to the experience of trying to run the Unity Hub and having it murder my laptop, I was also excited to see how well Godot performed on limited hardware.

After completing the first tutorial, I foolishly jumped into an overly-ambitious game idea. Luckily I realized after a few days this was too much, and came back to a much better process:

#### My Learning Process
1. **Learn the basics** - Read or watch a guide of the fundamentals. Usually this is reading documentation or a starter tutorial
2. **Copy Something Simple** - Find a simple idea to recreate (ex. Flappy Bird) then use any tutorials/guides needed to finish the project
3. **Individual Project** - Apply what I learned by making a slightly different project, ideally in the same realm as the copied project
4. **Repeat**

### Takeaways
#### Godot's Structure
Everything in Godot is structured around the idea of Nodes arranged in a tree structure. Rendering a sprite is a node. Applying physics is a node. Nearly all game objects are collections of nodes in a trenchcoat. It's a very object-oriented way to design game assets for reusability.

#### GDScript
The biggest issue I had with my time in Godot came down to it's scripting language, GDScript. While it technically supports C# (that I love working with), build support isn't available for web platforms and is very limited on mobile. If you want to use Godot 4 for anything other than Windows builds, you kind of have to use GDScript.

GDScript on the surface is great. It's a scripting-style language that feels familiar to Python, with a built-in code editor that has some great features. You can Ctrl + Click nearly anything to jump to documentation for methods/properties. It's quick to write in. It's built right into the engine so no need to juggle different windows.

The issues I encountered were mostly from trying to use a scripting language for something (in my opinion) is too large for it. For example:
- **Dynamic typing** - static typing is not only faster, but helps prevent so many bugs during runtime. I will always take more verbose variable declarations over strange corner case runtime bugs. GDScript technically supports this, but it's not nearly as mature as something like C#
- **Duck typing** - similar to above, duck typing is needlessly unstable compared to static type-enforced method calls. Which leads me to:
- **No Interfaces** - Given how object-oriented the rest of the engine is, it's frustrating to not have the ability to assign and enforce interfaces to objects.

When I'm learning new things, I try to leave any opinions I have at the door so I can embrace new ways of doing things. However, when the issues I run into don't exist in other technologies I've used, it can be frustrating to have to worry about such avoidable problems.

#### The Editor
Once I spent some time in it, the Godot editor felt very familiar to Unity. The built-in code editor was slightly polarizing, because while it did offer some cool features, it also meant not using other tools I'm already experience with (like VS Code or Rider). 

My biggest complaint is that file tabs for open scripts are placed on the left navigation bar, rather than the top like any other code editor. They have a fair point about it making better use of the space, but I never got used to it. Looking online, I'm not the first person to have this complaint.

### Closing Thoughts
With all that said, I really enjoyed my time learning Godot. It definitely has some quirks I'd love to see improved (mainly C# build support), but there's a lot of potential in this engine. The strongest part of Godot is it's community, and I have little doubt it will be a vastly better engine in the years to come.

### Deliverables
- [Playable "Vampire Surivors" Demo (locked at 1080p)](https://shiftycow.itch.io/wizard-survivors)
- [Source Code](https://github.com/TraySimpson/WizardSurvivors)
