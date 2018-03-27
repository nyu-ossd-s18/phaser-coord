# phaser-coord

_Meetings on Tuesdays at 6:30pm_

## March 27th Meeting Notes 
Objective: Narrow focus for the goal of the project.

Progress: Now that we are all a bit more familar with Phaser, we have decided how we will focus on our long-term goals for contributing. We've decided that we will have two focuses:

1. Creating new examples: Marcus, Matthew
- [**fill here will details**]
2. Fixing broken examples: Melissa, Gabe, Daisy
- Several examples in the phaser3-examples repository are broken due to changes in the API from version 2 to version 3. As this switch was very recent, there is a lot still to fix. The documentation isn't even done yet! 

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
