# Learning_Journal
Progress of Project and Notes

15/10/24
Created learning journal 

When making the tutorials make them unlinked so that none require a watch of another to understand the statements used. 

Use tutorial tips in Week 2 notes

22/10/24

Started making the script for the first tutorial. Decided to make a 3d movement script that moves a cube around a space.

Cube is able move horizontally but collision with objects sends it flying. Will fix next week

29/10/24

Cube's flying issue was solved by locking rotations of the cube in its inspector window.

The movement code felt to stiff for smooth movement and would immediatly change direction when inputs where pressed. 

Going to research how to keep momentum  over movement

5/11/24

Found out how to keep momentum so changed the movement code to use float commands ands use the scenes time to determine speed.

Experimenting with the movement itself I want to add a boost type of button that lets my character move at increased speeds. Like a sprint button

12/11/24

Boost button was added by adding force to the body with its vector and impulses. 

Movement codes tutorials is being written. Will decide the next code next week. 

19/11/24

1st tutorials script is now complete and I can begin the next code. 

Ive decided tyo do a pickup script tutorial as that will be the main goal for the end prototype game, picking up coins. 

I have made the coin assets and found out how to colour them using the materials in unity.

The script has been started but not much progress yet. Will work on it more next week.

26/11/24

Pickup script has been finished, had some issues with the coins not detecting the player and the canvas not changing when they were picked up.

Coins being picked up was easily fixed with making a tag for the player which then was detected by the code instead. 

Canva's issues were helped by Paul, seemed to be an issue with the UI picking up changes from the code due to parenting issues and code not being in the right place.

Started writing the tutorial for pickups.

3/12/24

2nd Tutorial is finisshed along with final touchups for the pickup script.

I want to do something unique with this tutorial so ill take inpspiration from the Binding of Isaac.

I want to have simialr door mechanics to top down games that open when the player goes near them. Did some reserach on the Unity animator window that allows objects to have states saved and move between them within unity under certain conditions. Im going to find a tutorial on how to use this properly.

Found how to use the Unity animator with cube blocks that move inward and outward away from each other. Now i just need to make these into a door shape.

10/12/24

I made the door asset quicky using some blocks for the walls and doors of the object and started making the animation states. Had some issues at first with the states not saving properly but was fixed after I started using the record button and creatign a Bool

The states of the door are now saved so im going to start putting this into some code. 

Easiest way to detect collsion was to make an invisble box that detects the player approaching the door. 

Quivkly finished the code for the door as it wasnt too long to make. Had some issues with the code making the states move back and forth but this was fixed quickly with setting the Bool to be changed. 

17/12/24


