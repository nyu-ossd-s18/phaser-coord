# Team Phaser
**NYU Open Source Software Development** by Professor Joanna Klukowska, Spring 2018   
  
Gabe Gordon  
Marcus Guimaraes  
Matthew Herman  
Melissa Lopez  
Daisy Zheng  

[Check out our final presentation slides here!](https://docs.google.com/presentation/d/1RvqHb_Uuuika4nDF1sxnTS19hqrcL5O-_VVcLwX8I2s/edit?usp=sharing)  
[See a summary of our contributions here!](https://github.com/nyu-ossd-s18/phaser-coord/blob/master/summary.md)  

_Meetings on Tuesdays at 6:30pm_

## April 17 Meeting Notes
Objective: Complete full draft of presentation

Progress: Presentation available [here](https://docs.google.com/presentation/d/1RvqHb_Uuuika4nDF1sxnTS19hqrcL5O-_VVcLwX8I2s/edit?usp=sharing)!

## April 10 Meeting Notes
No meeting today! 

## April 3 Meeting Notes
Objective: Continue working on example fixes and our new example

Progress:

Marcus: 
Helped clean Matthew's shooter example game.

Matthew:
Worked on new camera feature of shooter example.

Gabe: Fixed the Geom / Point / Get Magnitude Sq example. PR: https://github.com/photonstorm/phaser3-examples/pull/106

Daisy: Found fix for zig-zag path: https://github.com/photonstorm/phaser3-examples/issues/104

Melissa: (wasn't able to be at the meeting) Worked on another PR: https://github.com/photonstorm/phaser3-examples/pull/105

## March 27th Meeting Notes 
Objective: Narrow focus for the goal of the project.

Progress: Now that we are all a bit more familar with Phaser, we have decided how we will focus on our long-term goals for contributing. We've decided that we will have two focuses:

1. Creating new examples: Marcus, Matthew
- We've decided to make a top-down shooter, showing off features of Phaser that aren't in current game examples.
- Our goal is 200 LOC--we'll fit in as many features as we can within it
- We'll collaborate remotely on this.
2. Fixing broken examples: Melissa, Gabe, Daisy
- Several examples in the phaser3-examples repository are broken due to changes in the API from version 2 to version 3. As this switch was very recent, there is a lot still to fix. The documentation isn't even done yet! 
- We each have created a card in the "In Progress" column of our GitHub project detailing what sections of the API we are focusing on.

## March 20th Meeting Notes  
Objective: Go through Phaser 3 tutorial and examples sandbox to find bugs.

Progress:
We found a number of errors while going through sandbox examples together, although some of them were already reported. 

- Pacman: Game will not load because of TypeError: this.body.setTypeB is not a function
- Cannon: Game will not load because of TypeError: this.load.obj is not a function
(We noticed that both of these games are made of multiple files while others are not. It's possible that whatever mechanism is meant to integrate these files together may be the problem.)
- Flood: Bug with position of monsters during game play. The monsters move away from their intended positions. Issue appears to occur when mousing over the icon frequently.
Potential fix for issue: 
```
this.monsterTween.targets[0].y = icon.y
```
- Geom/Point/Add, Subtract, Divide, Multiply: These functions seem to be causing issues for most of the bugs relating to Geom/Point. In the main Phaser repository, each of these seem to be missing. Is this intentional? If so, the examples all need to be reworked. If it's not intentional, then there's a mistake in Phaser's core code.

