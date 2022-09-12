The .ani2d interface
===================

The .ani2d interface consists of a set of tools to allow easy and modular animation management (creation, edition and playback) for pygame applications. Such tools are:

- a json based data model used to describe animations with
  well defined rules to make animations versatile, flexible
  and manageable;
- a python package called "anim" which contains:
  - a subpackage to process the animation data described by
    the data model;
  - a subpackage containing an animation manager class which
    retrieves the animation data processed and can:
    - play animations;
    - edit them;
    - create/delete them;
  - a module containing a node class whose instances are
    manipulated by the animation manager in order to convey
    the illusion of movement and are arranged and rearranged
    in many different tree-like structures by the animation
    manager;
  - a class called WalkingDeque which consists of a
    powerful collections.deque subclass designed to support
    efficient index rotation (it is even used in other
    packages I developed as well) which is usually
    placed outside the anim package depending on the
    application due to its multiple usages;


The data model (.ani2d json files)
---------------------------------

The animation data model consists of a way of representing animations in a way that both humans and computers can understand. It is a json based data model developed by Kennedy Richard for usage in the pygame library (a SDL library binding which uses Python). The .ani2d interface "ecosystem" is composed of the json data and the anim software package which contains functions and classes to assist in managing animations (creation, edition and playback) in pygame applications. There's also a graphical desktop application being developed which already works but lacks some more widgets in order to be published.

Here's the definition of animation according to wikipedia:

    Animation is a method in which pictures are manipulated to appear as moving images.

This defines the approach we used for animations in this data model.

In a library like pygame, animations in their simplest form are achieved by blitting a set of images sequentially (in pygame, images are converted into surface objects). Changing the surface's positions over time also may convey the illusion of animation. Rotating and scaling them also does that, though in pygame this isn't usually done in real time, but rather stored as pre-rendered effects for efficiency as well as better results.

In more complex animations on the other hand, multiple objects are animated at the same time, laid out together in a tree-like structure. In such structures, all nodes have parent and/or children relationships with each other. They all have a parent node, except for the topmost node, called "root", which has no parent.

All nodes have their own surface animations. Except for the root node, all other nodes also have position animation. Such positions are relative to the root node, that is, distances from the root node, not absolute positions.

Since simple animations can be considered tree-structure animations consisting of one single root node, the model also treats them as "animation trees".

Since animating multiple objects at once may bring many complications and complexity, making it hard to create, edit and manage animations, some design rules were defined to facilitate the animation management. In the next sections we present a step by step guide of how animations were first conceived and managed in pygame and each problem appeared and gave birth to features and design rules which ended up comprising the system we have today. A compilation of the rules is also presented in the next session.
