# Project-2

# Description
The game is a simulation of climbing in which you have a certain energy to start with, and the higher you climb, your energy decrease. The height of the mountain varies from the path you take. If your energy burns out, you will fall. Your goal is to find the best path for reaching the top. You get a max score if you save the most energy.

# How It Works
As we were unable to implement the game to any meaningful capacity, here is what the goal was: The wall is essentially the only avenue of input available to the player. The wall will have handholds. These handholds will be the only interactive pieces, allowing players to grip and hoist themselves. We could then institute either a high score system, based on climbing an infinite wall and judging maximum height reached, or a difficulty system, in which we either hard code several walls or have progressively harder sets of handholds randomly generated. Some of the handholds will be infected with COVID-19 and visible and some will be hidden. The player has to avoid these and reach the maximum height.

# Climbing

The climbing functionality was attempted as follows. First, we created a class that would apply to each hand called "Pull", which primarily served to define "prevPos", or the position of the hand on the previous frame, and "canGrip", which would return a Boolean concerning whether the hand Collider was within another Collider.

![Image](https://github.com/CodesbyA/Project-2/blob/main/image.png)

Then we created the "GripManager" script to apply the movement to the XR Rig. We first attempted to simply not apply hand movement once the grip was engaged, and instead apply the reverse of the hand movement to the Body to simulate the pulling force, but that yielded no results. The most successful attempt was when we spawned a Configurable Joint on the gripped Collider that would, theoretically, lock the hand in place automatically, and we could simply change the spring force on the joint that would move the Body for us. This attempt yielded only moving the body through the floor on release of the joint, regardless of what we tried to fix or change it. Most of that code is in the snippet below.

![Image](https://github.com/CodesbyA/Project-2/blob/main/image1.png)

# Menu:

The menu was created by importing an asset from the Asset Store. The actual asset is tailored for a RPG game. The following changes were made to the asset to make it compatible with our game: 

- The Extras Section was removed from the actual menu. 
- Settings menu was removed since it involved details regarding the RPG game. 
- The audio on clicking the buttons has been changed. 
- Background music has been edited out to suit the game. 
- Since the buttons in the menu are co- related, the script was edited to make the functionality better suited to our game as deleting the buttons was not possible (created stagnant menu with no option to resume or exit game).
- The theme was edited.

![Image](https://github.com/CodesbyA/Project-2/blob/main/Meu%201.JPG)
![Image](https://github.com/CodesbyA/Project-2/blob/main/Menu%202.JPG)
![Image](https://github.com/CodesbyA/Project-2/blob/main/Menu%203.JPG)


# Team Contribution:

- Brian: Map, Presenting the presentation slides and Report.  
- Ajay: Menu, Presentation Slides and Report. 
- Yuanxu: Handholds and Report. 

# Mid Review Feedback:

- How would orientation work on this?

- Big Chungus?

- Will there be hand tracking?

- isn't the appeal of rock climbing physical exertion? sorry if i missed it, but will the user just be waving their arms around?

- isn't the appeal of rock climbing physical exertion? sorry if i missed it, but will the user just be waving their arms around?

# Potential Features: 

- Voice Commands
- Multiple Modes



