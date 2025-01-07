For this tutorial we will be making a simple automatic door opening sequence using the Unity Animator functions. This will consist of using Unitys in built animation software to create different forms of the door and animate them accordingly to where the player is located within the immediate vicinity

To begin we need the basis for the door. To do this create a few cubes and rectangles to act as the door and wall or brace that holds the doors. Similar to shown below 

![image](https://github.com/user-attachments/assets/9b2e8000-36cb-4d84-9da8-aafcbb7dd822)

Next we need to make the animations for the doors that will open and close. Open up the Animator window if it is not open already. The window can be located as shown here 

![image](https://github.com/user-attachments/assets/1df5caba-d772-4dd1-b7a4-eb5c20271fcd)

First select the group of objects you wish to animate, in this case the whole of the door including both the moving segments and any braces you have made. In the animation window select Create and name the first file something along the lines of Door opening.

![image](https://github.com/user-attachments/assets/317c0599-a464-4aa7-bff9-4bf7c7ecca49)

After the file is created return to the animation window and begin recording the changes made to the object using the small red dot. This will mark changes saved across the timeline and play them back when you hit the small traingle platy button. 

![image](https://github.com/user-attachments/assets/7d53b64f-3ca3-410e-8f13-cf4c7bd69e41)

Create the first timestamp where the doors are closed fully in thier default stance and bring the slider over to the end and move the door objects to the most open position and save again.
This will create the two points of range that the door will travel between and playing the animations will have them opening repeatedly within that range.

Next we need to the same thing but in reverse. Create a new clip animation shown below, name it Door close and repeat the previous step, but have the first frame be the open doors and the last be the close. Playing this should resemble somethign similar to the last animation in reverse. 

![image](https://github.com/user-attachments/assets/e62f1e26-220e-4af6-9e58-2c9fd59d8ecf)

Finally make a third clip which is simply just the doors closed. This will be used as our static state of the door where nothing is happening to the doors and is where the animations will start and end.
