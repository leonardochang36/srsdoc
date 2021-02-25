# Game Name Here
> Game Design Document

# Table of Content

- [Game Design](#game-design)
    - [Summary](#summary)
    - [Gameplay](#gameplay)
    - [Mindset](#mindset)
- [Technical](#technical)
    - [Screens](#screens)
    - [Controls](#controls)
    - [Mechanics](#mechanics)
- [Level Design](#level-design)
    - [Themes](#themes)
    - [Game Flow](#game-flow)
- [Development](#development)
    - [Abstract Classes / Components](#abstract-classes--components)
    - [Derived Classes / Component Compositions](#derived-classes--component-compositions)
- [Graphics](#graphics)
    - [Style Attributes](#style-attributes)
    - [Graphics Needed](#graphics-needed)
- [Sounds/Music](#soundsmusic)
    - [Style Attributes](#style-attributes-1)
    - [Sounds Needed](#sounds-needed)
    - [Music Needed](#music-needed)
- [Schedule](#schedule)



# Game Design

## Summary
Sum up your game idea in 2 sentences. A kind of elevator pitch. Keep it simple!

## Gameplay
What should the gameplay be like? What is the goal of the game, and what kind of obstacles are in 
the way? What tactics should the player use to overcome them?

## Mindset
What kind of mindset do you want to provoke in the player? Do you want them to feel powerful, or 
weak? Adventurous, or nervous? Hurried, or calm? How do you intend to provoke those emotions?

# Technical
 
## Screens

```
1. Title Screen
    a. Options
2. Level Select
3. Game
    a. Inventory
    b. Assessment / Next Level
4. End Credits
```

_(example)_

## Controls
How will the player interact with the game? Will they be able to choose the controls? What kind of 
in-game events are they going to be able to trigger, and how? (e.g. pressing buttons, opening doors, etc.)

## Mechanics
Are there any interesting mechanics? If so, how are you going to accomplish them? Physics, 
algorithms, etc.

# Level Design
 (Note : These sections can safely be skipped if they’re not relevant, or you’d rather go about it another way. For most games, at least one of them should be useful. But I’ll understand if you don’t want to use them. It’ll only hurt my feelings a little bit.)

## Themes
```
1.	Forest
    a.	Mood
        i.	Dark, calm, foreboding
    b.	Objects
        i.	Ambient
            1.	Fireflies
            2.	Beams of moonlight
            3.	Tall grass
        ii.	Interactive
            1.	Wolves
            2.	Goblins
            3.	Rocks
2.	Castle
    a.	Mood
        i.	Dangerous, tense, active
    b.	Objects
        i.	Ambient
            1.	Rodents
            2.	Torches
            3.	Suits of armor
        ii.	Interactive
            1.	Guards
            2.	Giant rats
            3.	Chests
```

_(example)_

## Game Flow
```
1.	Player starts in forest
2.	Pond to the left, must move right
3.	To the right is a hill, player jumps to traverse it (“jump” taught)
4.	Player encounters castle - door’s shut and locked
5.	There’s a window within jump height, and a rock on the ground
6.	Player picks up rock and throws at glass (“throw” taught)
7.	… etc.
```
(example)


# Development
 
## Abstract Classes / Components
```
1.	BasePhysics
    a.	BasePlayer
    b.	BaseEnemy
    c.	BaseObject
2.	BaseObstacle
3.	BaseInteractable
```
_(example)_ 

## Derived Classes / Component Compositions
```
1.	BasePlayer
    a.	PlayerMain
    b.	PlayerUnlockable
2.	BaseEnemy
    a.	EnemyWolf
    b.	EnemyGoblin
    c.	EnemyGuard (may drop key)
    d.	EnemyGiantRat
    e.	EnemyPrisoner
3.	BaseObject
    a.	ObjectRock (pick-up-able, throwable)
    b.	ObjectChest (pick-up-able, throwable, spits gold coins with key)
    c.	ObjectGoldCoin (cha-ching!)
    d.	ObjectKey (pick-up-able, throwable)
4.	BaseObstacle
    a.	ObstacleWindow (destroyed with rock)
    b.	ObstacleWall
    c.	ObstacleGate (watches to see if certain buttons are pressed)
5.	BaseInteractable
    a.	InteractableButton
```
_(example)_

# Graphics

## Style Attributes
What kinds of colors will you be using? Do you have a limited palette to work with? A post-processed HSV map/image? Consistency is key for immersion.

What kind of graphic style are you going for? Cartoony? Pixel-y? Cute? How, specifically? Solid, thick outlines with flat hues? Non-black outlines with limited tints/shades? Emphasize smooth curvatures over sharp angles? Describe a set of general rules depicting your style here.

	Well-designed feedback, both good (e.g. leveling up) and bad (e.g. being hit), are great for teaching the player how to play through trial and error, instead of scripting a lengthy tutorial. What kind of visual feedback are you going to use to let the player know they’re interacting with something? That they *can* interact with something?

## Graphics Needed
```
1.	Characters
    a.	Human-like
        i.	Goblin (idle, walking, throwing)
        ii.	Guard (idle, walking, stabbing)
        iii.	Prisoner (walking, running)
    b.	Other
        i.	Wolf (idle, walking, running)
        ii.	Giant Rat (idle, scurrying)
2.	Blocks
    a.	Dirt
    b.	Dirt/Grass
    c.	Stone Block
    d.	Stone Bricks
    e.	Tiled Floor
    f.	Weathered Stone Block
    g.	Weathered Stone Bricks
3.	Ambient
    a.	Tall Grass
    b.	Rodent (idle, scurrying)
    c.	Torch
    d.	Armored Suit
    e.	Chains (matching Weathered Stone Bricks)
    f.	Blood stains (matching Weathered Stone Bricks)
4.	Other
    a.	Chest
    b.	Door (matching Stone Bricks)
    c.	Gate
    d.	Button (matching Weathered Stone Bricks)
```
_(example)_

_(Note : If you’re soloing you might not need to define this part, as you can just use the Derived_ 
_Classes + Themes section as a reference. It’s up to you.)_


# Sounds/Music
 
## Style Attributes
Again, consistency is key. Define that consistency here. What kind of instruments do you want to use in your music? Any particular tempo, key? Influences, genre? Mood?

Stylistically, what kind of sound effects are you looking for? Do you want to exaggerate actions with lengthy, cartoony sounds (e.g. mario’s jump), or use just enough to let the player know something happened (e.g. mega man’s landing)? Going for realism? You can use the music style as a bit of a reference too.
	
Remember, auditory feedback should stand out from the music and other sound effects so the player hears it well. Volume, panning, and frequency/pitch are all important aspects to consider in both music and sounds - so plan accordingly!

## Sounds Needed
```
1.	Effects
    a.	Soft Footsteps (dirt floor)
    b.	Sharper Footsteps (stone floor)
    c.	Soft Landing (low vertical velocity)
    d.	Hard Landing (high vertical velocity)
    e.	Glass Breaking
    f.	Chest Opening
    g.	Door Opening
2.	Feedback
    a.	Relieved “Ahhhh!” (health)
    b.	Shocked “Ooomph!” (attacked)
    c.	Happy chime (extra life)
    d.	Sad chime (died)
```
_(example)_

## Music Needed
```
1.	Slow-paced, nerve-racking “forest” track
2.	Exciting “castle” track
3.	Creepy, slow “dungeon” track
4.	Happy ending credits track
5.	Rick Astley’s hit #1 single “Never Gonna Give You Up”
``` 
_(example)_

_(Note : Again, if you’re soloing you might be able to / want to skip this section. It’s up to you.)_

# Schedule
 
(what is a schedule, i don’t even. list is good enough, right? if not add some dates i guess)

```
1.	develop base classes
    a.	base entity
        i.	base player
        ii.	base enemy
        iii.	base block
    b.	base app state
        i.	game world
        ii.	menu world
2.	develop player and basic block classes
    a.	physics / collisions
3.	find some smooth controls/physics
4.	develop other derived classes
    a.	blocks
        i.	moving
        ii.	falling
        iii. breaking
        iv.	cloud
    b.	enemies
        i. soldier
        ii.	rat
        iii. etc.
5.	design levels
a.	introduce motion/jumping
b.	introduce throwing
c.	mind the pacing, let the player play between lessons
6.	design sounds
7.	design music
```
_(example)_

