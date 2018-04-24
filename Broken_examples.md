## List of broken examples we've found

* Pacman: Game will not load because of TypeError: this.body.setTypeB is not a function
* Cannon: Game will not load because of TypeError: this.load.obj is not a function (We noticed that both of these games are made of multiple files while others are not. It's possible that whatever mechanism is meant to integrate these files together may be the problem.) 
* all files under the game objects/graphics/_mesh, a lot of functions not in api, but examples are new
* Flood: Bug with position of monsters during game play. The monsters move away from their intended positions. Issue appears to occur when mousing over the icon frequently. Potential fix for issue:
`this.monsterTween.targets[0].y = icon.y`
* Geom/Point/Add, Subtract, Divide, Multiply: These functions seem to be causing issues for most of the bugs relating to Geom/Point. In the main Phaser repository, each of these seem to be missing. Is this intentional? If so, the examples all need to be reworked. If it's not intentional, then there's a mistake in Phaser's core code.
* Input/Mouse/Top Only: Doesn't do anything.  Seems like the input events aren't being called.  They may be malformed according to [this page](https://phaser.io/phaser3/api/input) in the API.
