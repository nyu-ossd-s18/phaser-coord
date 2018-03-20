# phaser-coord

Meetings on Tuesdays at 6:30pm

## March 20th Meeting Notes  
Objective: Go through Phaser3 tutorial and examples sandbox to find bugs.

We found a number of errors while going through sandbox examples together, although many of them were already reported. 

- Pacman: Game will not load because of TypeError: this.body.setTypeB is not a function
- Cannon: Game will not load because of TypeError: this.load.obj is not a function
(We noticed that both of these games are made of multiple files while others are not. It's possible that whatever mechanism is meant to integrate these files together may be the problem.)
- Flood: Bug with position of monsters during game play. The monsters move away from their intended positions. Issue appears to occur when mousing over the icon frequently.
Potential fix for issue: 
```
this.monsterTween.targets[0].y = icon.y
```
- Geom/Point/Add: This function seems to be causing issues for most of the bugs relating to Geom/Point. In the main Phaser repository, src/geom/Add.js happens to be missing 
