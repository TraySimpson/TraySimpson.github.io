---
title: My Dumb Thoughts on AI in 2026
date: 2026-05-14 17:47:00 +0600
categories: [Thoughts]
tags: [ai, art, game-development, general]
image:
    path: assets/img/AI-Thumbnail.png
---

It's been over a year since I've posted anything here, and I've been thinking a lot about AI. 
I'm not going have any opinion you haven't heard before. I'm not going to try and convince you it's great or it's horrible.
Instead, I just want to document my own current thoughts and feelings, so that I can look back on this and see what's changed

* As a disclaimer, all of this post (and every other on this site) are written by my dirty human hands*

### My Background

I've been a professional software since I graduated in 2020, so I got very lucky to get work experience before the value of entry-level developers dropped in the last few years. I've worked as a full-stack engineer, then as a platform engineer (covering everything from infrastructure, IT, regulation policy, and more software development at a small company), then back to a software engineer at a larger company.

I wouldn't call myself an artist, but on the side I love creating art. From silly little sketches in a notebook, to pixel art for a game jam, to more serious "art studies" that I can never get consistent about, I like making art. I value very deeply what it means to create things and think that's a very human thing.

In between these two side, I find that my thoughts around AI are seasonal and often conflicting with eachother. My views about what may be the best way to live my life or be the best at my job feel like they battle what I worry about for future generations.

I know with certainty that just 6 years after graduating I can no longer recommend younger people to take the same path that I did. It would be foolish to not mention that new paths have been created because of these same causes, but I still find myself with worry about what will be the "ideal cushy work-from-home tech job" in the future or whether we'll all be laborers.

### My (Current) Views

I want to be clear that these can vary from week-to-week or even day-to-day, but overall I know these to be true to myself:

1. Everything requires nuance
2. AI is a tool that is incredibly capable
3. There is something inately human about creativity that we have yet to define

That's all a bunch of nice word garbage, so I want to dive into some specific examples to document my thoughts a little better than 3 random sentences I've just decided to write.

#### AI Efficacy

As someone who works daily with AI, I think this is one of the most misunderstood-by-the-masses point I see online. AI has become incredibly good at doing things.
It wouldn't be so threatening if it wasn't good, and I think that's part of the problem that most people misunderstand. The "AI Slop" images are the way they look because they're *lazily made*, not because AI images are graphically inferior to real art made by hand. People identify AI-written articles because they're *lazily made*.

I think the important thing to understand is that properly providing content **is** a skill, as silly as that sounds. Seeing a job opening offering 6 figures for a "Prompt Engineer" absolutely sounds stupid as hell, until you understand that a lot of the human work that goes into that is what makes the difference between AI slop and generated content you wouldn't notice

#### Game Dev

As an example, about a month ago I tried a month-long trial of Claude Code to prototype a game idea I had in Godot. If I wanted to, I could have just jumped right in and described what I wanted, then gone back and forth with it until I hit my billing limit or the project was done (I hit my usage limit like 4 times in 2 days which was fun).

Instead, I spent the first 2-3 hours *just* generating documentation for exactly what I wanted. I specified style guides (which I allowed it to design), architecture guidelines, and the various gameplay systems in depth so that nothing was up to it to "decide". I think that's a big piece of where "slop" comes from, when uncreative people can't think of something they let the plagarism decide.

Once I finished this large documentation repo, I had it walk through each system and implement it, and I ran into a total of about 2 issues. In terms of "vibe coding", it was very successful. I had a playable demo that was what I had wanted, but really there was a few issues:

1. I wasn't perfectly specific enough about the enemies, so rather than asking/flagging it as a gap, it guessed and created some very generic "Goblin" enemies and "Relic Monster", etc.
2. The UI was what I described, but still looked "different" from what I imagined. I think this largely comes from my own lack of experience making these, so I still have a large gap between my minds image and real things
3. I didn't feel very connected to the project. I designed everything, but I didn't really feel the excitement of "making something"

Problems 2 and 3 were largely the reasons I cancelled my trial, as I totally see the utilitarian value in it, but I want my hobbies to be something I actually... do

#### Art

One of my first negative experiences with AI was art, largley because I think artist are already highly devalued and struggle to exist in most cases. Additionally, what I consider to be an ideal society is one that has erradicated the laborious and undesirable jobs, and has the freedom to be scholars and artists just for the fullfilment of it. I'm usually not big on quotes, but I dig this one:

> "I must study Politicks and War that my sons may have liberty to study Mathematicks and Philosophy. My sons ought to study Mathematicks and Philosophy, Geography, natural History, Naval Architecture, navigation, Commerce, and Agriculture, in order to give their Children a right to study Painting, Poetry, Musick, Architecture, Statuary, Tapestry, and Porcelaine."
> - John Adams (maybe, I'm not a historian)

With all that already part of my core beliefs, I think it's of little suprise that I find the whole idea of AI-generated images rather gross. 

#### Society

I'm getting lazy here, but just a few bullet thoughts:

- I worry that AI will consolidate wealth more than it already is
- Nearly all good AI services are not owned by the people who buy them. They can become enshitified (already starting)
- Hardware shortages affecting RAM, storage, GPUS, etc (ideally short term, but still)
- Could be a boomer thought, but I worry about people being overly dependent and getting dumber. Personally I worry about my own skills degrading
- It's never been easier to be a scammer
- Anyone can "make anything" (aka "we've democratized ..!"), which may be a good starting point for some people. But I worry about the quality of things actually made if the people doing it don't have the passion/knowledge/etc as people doing it without AI
- Companies over-prescribing AI agents to try and add shareholder value makes me want to swallow a wrench

I've also seen some conversations on Reddit comparing the AI in society now versus Star Trek's holodeck, and I think it's a very interesting idea. A big reason people hate AI so much is societal. There is one of the biggest incentives in our lives (economic) to make slop in the hopes of "making it big". Let's flood Reddit with bots. Let's generate automated short video content to generate $2.03 in ad revenue (ew, what a sicko. Can you imagine trying to automate that?). Let's steal people's art style and flood a T-shirt company with it's design because my mom told me I was special too much as a child.

I joke, but I think a lot of these problems go away when people **have what they need, and feel complete as humans**. The whole "post-scarcity utopia" in Star Trek is something I've been thinking about a lot more with AI, because what are we currently striving for with AI? To replace as much human-generated content as possible in the hopes that we can make money? 

There's way too much to talk about with that idea, but I really enjoyed a recent Hank Green video that talked about AI removing the bottleneck from intelligence while most of the "world's biggest problems" are actually limited by wisdom. 

#### Software

This is one that I feel somewhat positive on, but still gives me some existential dread occasionally. AI for programming is really powerful. Also, it's really interesting to learn about how LLMs and agents actually work, and what they can do in *actually good use cases* is awesome! I think it's why so many people who are deep into AI just make AI tools; they get carried away with the cool theory that they realize they don't actually have any problems for them to solve with it (yet).

I don't have too many thoughts here, as I feel most have already been said. My only thing to add is that the current "Everyone should learn how to be a code architect" advice being given (like that I've heard at my own company) I fear will soon be outdated. If it can code, why won't it be able to design? It already can. Soon I imagine it will just be a few engineers supporting agents across large companies, while users either interact directly with the agents to generate features, or the agents themselves are so autonomous that they implement everything themselves. Sounds like a fun GPU compute bill




That's all the thoughts I can think of for now. I'm worried, and slightly over hearing the same things repeated (ironic, I'm sure), but I hope that with more and more change people will value wisdom more and more.
