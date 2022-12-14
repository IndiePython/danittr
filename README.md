# Dani To The Rescue (game prototype)

Dani To The Rescue (or danittr) is a game prototype made with the [pygame](https://pygame.org) library. It is a platformer.

![danittr screenshot](https://i.imgur.com/mVItT7D.jpg)

I'm [Kennedy Richard S. Guerra](https://kennedyrichard.com), 31, and made this prototype as part of the [Indie Python](https://indiepython.com) project.

This was my first somewhat complex pygame app I've ever made. It was made when I was still learning pygame and had almost no experience with Python as well. As such, the code represents the work of a beginner in both Python and pygame. Even so, I believe despite some poorly design choices there are parts of the code that are very useful and can still be used as-is or after refactoring.

Check this [youtube video](https://www.youtube.com/watch?v=O9F5E1CEWK8) presenting this prototype.

At the time I was working on this game, it was not meant to be a prototype, but a full-fledged game meant to be completed. However, I paused work in this project to work on tools to help me complete this game and others I plan to do in the future. One of those tools is already released, which is [nodezator][] (node editor app), on which I've been working most of the time recently (you can also watch a [video about nodezator](https://www.youtube.com/watch?v=GlQJvuU7Z_8)). Other tools are yet to be finished and released, like an [animation editor][] and a [level editor][] as well.


## Installation

This game doesn't need to be installed, but if you want, you can install it via pip.

If you have Python installed in your system and it has pygame available, all you need to do is download this repository and inside the repository folder run the `python -m danittr` command.

If you want to install it, just execute the command below. It will install danittr and also, if not available yet, pygame.
 
```bash
pip install danittr
```

If everything went well, after installing, you should be able to start by simply typing `danittr` or `python3 -m danittr` in your command line.

That's all, but, if you encounter any problems, contact me with one of the methods described further below in the contact section.


## Usage (controls)

- up, left, down, right: W, A, S, D
- jump: K
- fire: J
- interaction: E (talk to npc, pick items, save on satellites)
- advance dialogue/deny prompt: SPACE
- accept prompt: ENTER


## Features

The prototype has almost no playable content, but there's a single level where you can walk, talk to npcs, save the game, access different areas, pick item and throw items.

As I said however, there are a lot of stuff that may be useful to reuse or learn from:

- menu screen;
- option screen;
  - adjustable music and sfx volume;
  - configurable keys;
- state saving/loading;
  - load state screen with thumbs;
- comic-like dialogues with generated speech bubbles;
- level data that works in tandem with my yet to be released [level editor][];
- a multi-sprite animation system that works in tandem with my yet to be released [animation editor][].

Again, remember the code was made when I was a total beginner, so most of it is poorly designed.

Some of the code (after refactored/improved) and many of the lessons I gained from my experience developing this prototype can be seen in my most recent and more mature app, [nodezator][], which uses pygame as well.


## Gotchas

There's a pit on the highest peak of the level (after climbing all the vegetation, to the left). If you fall there, there is no way to get out, so you'll have to load your save again. It was supposed to have a giant serpent boss for the player to defeat.


## Contributing and Issues

This project is a prototype and isn't under development anymore. It was published for educational purposes only and is actually archived, so it isn't receiving contributions or issue reports anymore.

Of course, though, if you are having trouble trying to run it, let me know via one of the contact methods below and I'll be glad to help.


## Contact

Contact me any time via [Twitter](https://twitter.com/KennedyRichard) or [email](mailto:kennedy@kennedyrichard.com).

You are also welcome on the Indie Python's [discord server](https://indiepython.com/discord).


## Patreon and donations

Please become a patron of the Indie Python project to support the creation of free open-source code like this prototype, tools like the already released [nodezator][] app and also future complete games to be released. You can become our patron on [patreon](https://patreon.com/KennedyRichard) or [liberapay](https://liberapay.com/KennedyRichard). Also check the project's [donation page](https://indiepython.com/donate) for other donation methods.

## License

### Code

This Dani To The Rescue game prototype is dedicated to the public domain with [The Unlicense][].

### graphics

The pygame logo is not mine. The indie python logo is.

All the other graphics/sprites were made by me and are also in the public domain with [The Unlicense][].

### Music and sfx

Music and sfx are not mine, they are royalty-free resources downloaded more or less 5 years ago.

I'll update this section giving credit to the authors when/if I find the links to the original resources. I apologize for this. My old laptop died on me a couple years ago and I lost the original links.


[nodezator]: https://github.com/IndiePython/nodezator
[animation editor]: https://www.youtube.com/watch?v=gj_yfWpYnYE
[level editor]: https://www.youtube.com/watch?v=TwmAVV_1Gs4
[The Unlicense]: https://unlicense.org/
