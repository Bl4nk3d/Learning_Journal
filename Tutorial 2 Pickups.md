For the second tutorial I will be explaining how to create simple pickups that can be collected by the player and counted towards a UI count 

First we need to make the pickups themselves

For simplicity we will be making basic coins to collect. In the Heiarchy right click an empty space and create a Cylinder, scale it down using R and rotate it using  the Transform axis in its inspector tab (usually X -90)

![Screenshot 2024-11-26 142212](https://github.com/user-attachments/assets/920baac7-e779-4094-ad9a-77f3a4c953a8)
![image](https://github.com/user-attachments/assets/ef45f4d0-0728-4da4-ad2e-ad1440c59161)
![image](https://github.com/user-attachments/assets/81b8bdf8-414d-4022-9b8a-9f8371fcb26d)

No we need to make this look more like a coin in game using its Mesh renderer. Go to the assets folder, create a new folder named Materials right click, go to create and make a new Material

![image](https://github.com/user-attachments/assets/b7a71d6d-8fdd-4257-b80d-75bb265b5994)
![image](https://github.com/user-attachments/assets/53fdb35c-ae8c-467b-81be-7ed67b645d45)


To get that nice gold metal gleam effect, slide the metalic slider up to 1 and then choose an appropriate colour for our coin. I will be using a nice blue for this demo. I like blue :D

![image](https://github.com/user-attachments/assets/f199a1dd-826a-4f8a-a0e8-9ddc7cb8fb23)
![image](https://github.com/user-attachments/assets/2321cc01-6dc6-45ca-bf72-ab0d8fde1fff)


Finally drag the new material into the Mesh Renderer Element and the coin should now take whataver settings you apply to that material

![image](https://github.com/user-attachments/assets/ded22e7e-8050-4a99-9712-baaeaa2984dc)

Next return to assets folder, click on the cylinder in the heiarchy and rename it Coin. Drag the coin into the Assets table at the bottom of the screen and this will make it a set Asset that can be repated and inserted multiple times and be edited as a group rather than as indiduals. This means any changes will occur with all coins made from this asset.

![image](https://github.com/user-attachments/assets/98cef2ba-f6bc-4445-8543-9a209a71fddf)


Delete the coin from the heirarchy on the left and then drag and drop however many coins as you wish from the new one in the Assets table. 

![image](https://github.com/user-attachments/assets/1369fa2e-6e92-451c-91fb-c5487e1c6c8e)

Find your "player" in your scene and attach a new script to it named "CoinCount" 

Insert the following script into the file:

![image](https://github.com/user-attachments/assets/919248f9-a405-44a6-8a1c-a4a9ecf748bb)

After that we need to add in the item that will display the number of coins on our screen and make sure that it stays in frame during gameplay

Head to game objects at the top of your screen and find the Text Mesh Pro in the UI tab

![image](https://github.com/user-attachments/assets/fe4eadcf-7fb6-4c41-b57f-2d3f5dd4330e)

If you cannot find this add on simply download it from the Package Manager

![image](https://github.com/user-attachments/assets/adab8768-565a-475d-95e5-0731697b2ec8)





Click on the Coin asset to open up its inspector and attach a new script to it. Name this script "Pickup"

Next write the following above the Start function 

void OnTriggerEnter(Collider other)
{ 
  CoinCount player = other.GetComponent<CoinCount>();
if (player!= null)
{
player.AddCoin();
gameobject.SetActive(false);
}

It should look like the following

![image](https://github.com/user-attachments/assets/7ab998fc-c56d-4599-a648-3b273936465c)

Essentially what this code is doing is that it is detecting when a collsion is occuring with another object and when that object hits the player it adds a score to the number of coins collected and then sets itself unactive, dissapearing from the scene. 
This ensures that it is not picked up again until the next reload of the area. 








