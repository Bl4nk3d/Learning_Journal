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

Next we will be using the animator window to set our animation frames to the correct transitions and states. Open the animator windowto begin setting this up. If you cannot find the animator window heas to Window at the top of the screen Go to Animation - Animator then drag the window to where you find appropriate. I personaly put my window next to my project and console tabs. 

![image](https://github.com/user-attachments/assets/c4961d8c-ece7-438b-9eba-7ce7821921a4)

In your Animator window your states should look like the image below. 

![image](https://github.com/user-attachments/assets/70a35a35-f105-4f83-bf9a-bc9bb086ac04)

This is not a good layout for the states of the door. First move away the red Exit button as they door will not leave the states we have previously made. Next set the Layer Default state to the static door frame not the Door open State. This will be the frame that the door is in at the start of the scene. After that layout your states like so for easy visualisation and editing.

![image](https://github.com/user-attachments/assets/0add756e-caf0-460b-b59d-d3e88e9d9b52)

Next we need to create a new Bool and to do this head to the parameters tab within the animator window and click the plus dropdown menu and hit Bool. Name it something simple such as DoorOpen.

![image](https://github.com/user-attachments/assets/13af2cd6-3aa5-4297-bd05-a5388c691d7b)

Now we can start making these transitions. Right click the DoorStatic state which should be colored yellow as it is the new default state and hit make new transitions. It will make a new arrow which you can than drag to the doorOpen state as it needs to open upon being triggered. Inside the transition arrow there shoul be a menu that says 'Conditions'. Click the small plus sign and it will create a new condition for this transition. The condition that it makes innitially which should be DoorOpen - true is the transition that we need. 

![image](https://github.com/user-attachments/assets/a8990cf0-d688-468c-b48c-4891f93a1bbd)

Next make these same transtions between the Door Open and Door Close states with the Open to close state being DoorOpen - false for its conditions and the DoorClose being the same condition as the Static to Open. 

![image](https://github.com/user-attachments/assets/d45224a7-6497-441b-89da-b5ba57bc978d)

Finally to make the doors have a smooth in between animation and to be able to distrub the animations partway with movement untick the Has Exit Time on all transitions we have made. 

![image](https://github.com/user-attachments/assets/fd5e7c88-61de-4310-b4a1-87e99bfbc97c)




















