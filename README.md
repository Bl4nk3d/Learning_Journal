# Learning_Journal
Progress of Project and Notes

15/10/24
Created learning journal 

When making the tutorials make them unlinked so that none require a watch of another to understand the statements used. 

Use tutorial tips in Week 2 notes

22/10/24

Making new tutorial video

Basing subject on 3D movement with possible physics based mechanics (gravity)

Week 4 

In this tutorial  I will be presenting how to code simple 3D movement within a space 

First create a new project as a 3D rpoject and name it Move the Cube

![image](https://github.com/user-attachments/assets/d354a0d7-6212-40aa-b936-38cb0f467f37)

After the project has been opened head to the Edit tab at the top left of the screen and go to Project Settings. Here we want to edit what keys trigger movement within the code. Withint Project settings open the sub tab Vertical and remove the primary buttons associated with it. This will ensure that our code does not clash with pre set buttons. 

![image](https://github.com/user-attachments/assets/6578d5d0-337e-4192-b095-f5f6ff73655e)
![image](https://github.com/user-attachments/assets/eab2108c-826d-4e88-9f53-9f5b47235997)

Close the tab and we can begin making our mover.

In the Scene box right click and click 3D Object - Cube to place a cube within our scene. Repeat this with a Plane and place it below our cube. This will be so we can clearly see the ways our cube moves. 

![image](https://github.com/user-attachments/assets/8a5442d6-9bfe-4d4b-a03e-72801fb58859)

Next go to our Folders and create a new Folder called Scripts, this is where we will keep our code that determines how our cube works. 

![image](https://github.com/user-attachments/assets/1b112a2d-ea41-4bb5-ad14-80560af91f46)

Using the same create menu, make a new script within our new folder and call it CubeMove and open it.

![image](https://github.com/user-attachments/assets/cbd195db-ea73-4e33-ad68-44712a5cfe4a)

Brefore we begin to edit what it in the script we should first assign it to the cube we wish to move. Select the cube in the hierarchy or just click on it within the scene and find Add Components.

![image](https://github.com/user-attachments/assets/946df887-ca7b-4071-ae17-37c653257c49)

Next drag the script file over the Add component button to assign it directly to the object 

![image](https://github.com/user-attachments/assets/0bb94933-c4bd-46b6-aaaa-1414280c9afa)

Now we can start coding. Go back to the open script and within void update insert (public float speed = 5f) above the green start line and the following code. This code will determine that when an Input relating to a dimension is pushed its postion along that respective axis will be changed, moving it around as the player desires. 

![image](https://github.com/user-attachments/assets/fd12479a-5dac-4b83-9a4e-52e3a4f0fbcc)

You will notice with this code however that only horizontal movement is available with the arrow keys and this is because the default keys to move along that axis was removed earlier. However it should work when using W and S. 

Underneath t

