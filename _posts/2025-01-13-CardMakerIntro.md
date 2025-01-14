---
title: Generating Trading Cards from CSV Data
date: 2025-01-13 20:09:00 +0600
categories: [Automation]
tags: [automation, game-development, game, python]
image:
    path: assets/img/CSVCardMaker.png
---

TODO COVER IMAGE

Lately, I've been playing around with game prototyping by using physical game pieces, mainly from other board games.

Since I've never gotten remotely close to finishing any of my game dev projects (outside of a [game jam I did last year]({% post_url 2024-08-30-GMTKGameJam2024 %})), this strategy of prototyping has been a breath of fresh air. There's no programming. There's no rules set in stone. And most of all, it's just fun to get instant feedback on game ideas.

The only problem is it can be tricky and time consuming to create one of the most important parts of board games: *cards*.


#### Approach 1: Printing out a spreadsheet
For some of my early testing, I used Google Sheets and just made a rough table of the cards I wanted to try. I printed out this table as a kind of "cheat sheet", then used a standard deck of playing cards to actually handle shuffling, drawing, etc. On the printed table, each card had a playing card it mapped to (for example, the "Bombadier" character was any 8).

It was slightly annoying having to lookup details in a printed table as we played, and it definitely slowed down the game too much with my (very patient) partner, so I looked for a better solution.

#### Approach 2: Handmade cards
Next I tried taking 3x5 index cards and handmaking my playing cards. I at least had the bright idea of using sticky notes for things that might change (like different unit's moves or abilities), but even that took about 20 minutes to make 6 poor looking cards :)

### The Solution: Card Maker
Knowing that I could end up with potentially hundreds of unique cards, I spent some time looking for a way to get the best of both worlds: a spreadsheet-driven, printable, set of playing cards.

After some searching, I found this nearly ten year old project [Card Maker](https://github.com/nhmkdev/cardmaker). It would read in whatever data you provided as a CSV and generate card images using custom templates you could define. It was actually perfect.

I spent the rest of the evening filling out a spreadsheet with different card types, moves, and descriptions, all before even looking at how exactly this magical "Card Maker" would work :)

Luckily for me, it had a suprisingly intuitive design. It feels incredibly dated (looking at you floating windows), but in the best kind of way where everything is incredibly functional. I spent about 5 minutes glossing over the docs, spent about 10 minutes exploring the example project, and from there I was able to make my own templates pretty easily.

I won't make this a detailed Card Maker tutorial (as the documentation, example projects, and GitHub project already do an excellent job), but the main idea is:
- Define the size of your cards and create a template
- Add a "reference" (CSV datasource) to your template
- Create whatever elements you want. These could be images, text, or graphics (simple shapes)

Wherever you want dynamic data, you'd use it's special interpreted language (It also had an option for Javascript, but I didn't explore that) For example, if I had a CSV column named "card title", I could put the string `@[card_title]` in the element, and this would be generated dynamically from the contents of my CSV. Neat!

### The Printing Problem
The only issue I ran into (other than needing colored ink to print in black and white... thanks HP) was that the PDF export didn't work well for me. The first time I tried it, I just got a cryptic error message. When I tried just before writing this, I successfully got a PDF, but the sizes were incosistent, and it seemed to have a lot of duplicates.

Instead, I had to use the image export, which produced a individual image for every single card. I did not want to individual print all of those, so I decided to generate and write a Python script that would pack them for me.

The script itself is pretty simple, but it seemed helpful enough to document and upload [here](https://github.com/TraySimpson/image-packer). I spent some extra time getting it configurable and documented, but this allowed me to easily print all my cards and specify how many of each I wanted printed.

#### Conclusion
I would highly recommend trying to create any game ideas you have first as board games. Obviously there are a lot of genres and ideas where that isn't practical, but it's been a lot of fun play testing something so fast.

I just thought this was an interesting thing to share, and I always love when I find people have already made the exact tool I was looking for. Cheers
