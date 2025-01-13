For this tutorial I will be making a proper first person camera on a moving player object 

The aim of this tutorial is to make a smooth fully operation firts person perspective of a playr within a scene that can move around and interact with other things in the future.

To begin this tutorial we need to make a new script. Name this script FPSController or anything that you will remember.

Now we can start inserting the code that will help us move. 

First above public class insert the following line of code. This code will insert a character controller into the scene if it is missing. It should look like the image below.

![image](https://github.com/user-attachments/assets/b9ce12ae-3799-43ab-a25f-7736a7758ce7)

Next we need to add the variables that will determine the various features of the movement script and how they work. For this we will need how fast the player walks, how fast they are when they sprint, how high they can jump and how much they are affected by gravity.
This also includes how quickly the camera rotates with the mouse. The variables will be layed out as the following. 

![image](https://github.com/user-attachments/assets/3b45bcdf-f798-450e-be69-8009be21fdd1)

