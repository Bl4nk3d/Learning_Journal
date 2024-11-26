For the second tutorial I will be explaining how to create simple pickups that can be collected by the player and counted towards a UI count 

First we need to make the pickups themselves

For simplicity we will be making basic coins to collect. In the Heiarchy right click an empty space and create a Cylinder, scale it down using R and rotate it using  the Transform axis in its inspector tab (usually X -90)

(SC of making cyclinder and editing shape)

No we need to make this look more like a coin in game using its Mesh renderer. Go to the assets folder, create a new folder named Materials right click, go to create and make a new Material


To get that nice gold metal gleam effect, slide the metalic slider up to 1 and then choose an appropriate colour for our coin. I will be using a nice blue for this demo. I like blue :D


Finally drag the new material into the Mesh Renderer Element and the coin should now take whataver settings you apply to that material


Next return to assets folder, click on the cylinder in the heiarchy and rename it Coin. Drag the coin into the Assets table at the bottom of the screen and this will make it a set Asset that can be repated and inserted multiple times and be edited as a group rather than as indiduals. This means any changes will occur with all coins made from this asset.


Delete the coin from the heirarchy on the left and then drag and drop however many coins as you wish from the new one in the Assets table. 




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

(Image of Pcikup script here)

Essentially what this code is doing is that it is detecting when a collsion is occuring with another object and when that object hits the player it adds a score to the number of coins collected and then sets itself unactive, dissapearing from the scene. 
This ensures that it is not picked up again until the next reload of the area. 