## YOUR FIRST HOUR WITH UNREAL ENGINE
Day : Wednesday and Thursday

Date : 17- june and 18-June-2020

### Welcome to the launcher

* Home
* Store
* Library
* Friends
* Unreal Engine

#### Unreal Engine
This is Unreal Engine main page like the home page it lists everything new and exciting in the world of the Unreal Engine. It focuses entiry on development


#### Learn Tab
In this tab we have suggested learning resources as well as hotlinks to documentaion, video tutorials, and the community Wiki page.

#### Marketplace Tab
we find both free and paid content as there much in there that can help any project
#### Library Tab
* Engine Versions
* My Projects
* Unreal Studio Beta
* Vault Section (All of our plugins and purchased Marketplace content reside)

### Creating Your First Projects

Normally Software saves with exe i.e executable extention 

like Unreal Engine,

Level Editor saves with umap extention
Asset Editor Saves with uasset extention
Material Editor Saves uasset extention

#### Step 1: 
  Click on Launch button to open up the Unreal Engine

#### Step 2:
Click on the **New Project Tab** this tab allows us some fundamentals for our game for example 
* Blueprint-based projet
* C++ based project 
* Unreal Studio
Select any Template That You want -> Project Setting If needed ->Choose directory and Name your Project->**Click on Create project**

Bottom of the screen - **Content Directory**. (contains all the models, textures and otherassets in your project)

On the Left side of the screen - **Modes panel** - With this we can place series of assetsin our level (example. Cinematic, Geometry, Lights etc)
Also contains the level editing tools. (vertex paintaing,fooleage paintaing etc)

Center of the screen - Viewport - It shows us our open level. Can add assets into viewport
WASD style movement to navigate or with mouse wheel


#### Navigate the view :

Simply Right-Click and drag to rotate camera
Left-Click and drag to move forward and backward
finally we can use Middle Button to pan around the scene if we have mouse wheel

OR

instead of this you can use W,A,S and D to move forward, back, left and right

#### Transform HotKeys

**W** to Move
**E** to Rotate
**S** to Scale

In orde to turn off all widgets and see the game in apreview like view use 'G' key to toggle
Game mode

-Using **Ctrl + 1** keys allow us to bookmark our number
-Using **F11** key will toggle you in and out the imersive mode
-Finally **F** key will focus on any selected objets


#### Working With Content

Luckily Unreal Engine 4 gives us several ways get some content to work with our first game.

* Starter Content
* Marketplace
* Migrate from other Projects 
* Import Content Directory

#### Starter Content
When we created our project we had option to add the starter content To do this 
**Add New Button** In the Content Browser then Select Add Feature or Content Pack from in th enext dialog we can add content from

 Blueprint feature, C++ feature, Unreal Studio feature any of these three then select tab for starter content and then click on **Add to Project**
The starter content added to our projects content directory. to use just simple drag and drop


**To get a specific content from some project**

**Go to learn tab** - Locate Realistic rendering project -> Download and create new
realistic rendering project -> double click on .uproject file -> you will see a realistic scene, to migrate the assets from this scene to your project, navigate to ‘ArchVis’ folder in content browser then select an item and then select ‘Asset action’ then ‘migrate’ by right click.

**Migrate this into 'content' directory of your project**
We dont need to copy the fily manually from hard drive

**What if we want to migrate all the content of realistic rendering project to our project?**

* ArchVis - Right click - migrate - migrate all to content folder of our project.

#### Import Content Directly


* Static Meshes
* Sound Files.
* Images.
* Skeletal Meshes
* Alembic Animations.


#### Building Your First Level

Create new folder by **Right-Clicking in the content Browser and selecting new folder rename that folder as Levels**

**Levels** : Levels are effectively the container for scene that we want to make. The average project will consist of multiple levels.
* Within a level that our assets, lights,effects,sounds and all other asset types will live.

* for creating our first level. in Levels folder Right-Click choose 'level' rename it to my_first_level and you will get a blank space

* moving onwards use UE4's Content-sensitive search to find 'SM_XO' Bridge select one of the item and drag drop it
into the viewport. we will see this item in world outliner, but wont be able to see it on viewport.

* UE4 works like a physical world, so you wont be able to see anything in viewport untill
you add light to it.
for that, go to light section in the modes panel, and drag it into the scene.

* Now the tile we selected may have positioned anywhere and we need to give it a position.

* In details panel, set ‘location’ parameter as 0 0 0.
You can set the location of the light with the same method.

* In the right upper corner of the viewport, select snapping to closely map our tile.

**Duplicate this single tile, and make a floor of tiles.**

**To stop the endless fall, go to modes panel and search for start, and drag the player’s
start to our game and set its position in the details panel. 0 0 200**

**Set the background as sky.**

* Search fog in modes panel. Set location as **0 0 300.**

* We can control the fog and place the Sun more accurately in details panel.

* Details search panel -> search for **fog** and select light.

**And add reflection capture from modes menu. Just serach for ‘reflection’ drag it and set its position to 0 0 500.**

Again for capturing scene go to Build --> **Build reflection capture.**

* Search for **static meshes** in content browser and place one of the meshes and start building

#### Visual Control

There is no light hitting it all in real time its very difficult to calculate that kind of light thats called bounced light
select the sky light it will give us the ambient lighting we need just drag that in viewport
For Better Shadows change the position to 0,0,400 in the Details Panel

* In th modes panel, search for Post and select post process volume and set its position 0 0 0

* Post-Process Volume :- with this we can effect all cameras in the scene from a singular control

* Go to details section, and make exposure min and max both to 1.

In post process volume settings, serach for infinite and enable infinite extend. This wil
give it complete domain over our level rather than contained to specific area.
So, we will have a stable exposure.

**Now add sky sphere**

* In the modes panel search for sky select BP_sky_sphere and set its position to 0 0 0

* In Details Panel, drop down to directional Light Actor and select ‘DirectionLight’

* In world outliner, select, ‘Atmospheric fog’, ‘BP_Sky_Sphere’ and ‘SkyLight’, right click
it and select move to new folder ’ !World Lighting’ and last set brightness to 1

**make Sun more Alive and attractive**

* Go to direction light and enable Light Shaft Occlusion and Light Shaft Bloom.

**Set Brightness**

* Go to BP_Sky_Sphere, and adjust intensity.

#### Actors

Actor is kind of container much like the level or is a made up of same thing that go into the level

**What is static Meshes**
Dead element that provies our scenescape.



* Create a new folder in content browser, **BP_Actors(for Blueprint Actors)** inside that folder, right click in the content Browser select **blueprint class** and select Actor from the subsequent Menu. **Name it BP_Lamp**

* In the content browser search **SM_Plains Castle Arch_Iron_Torch_01** just drag and drop into the blueprint Editor viewport

* Search the content folder for **P_Fire** again drag this into the window as well adjust a window as per requirements

* From the Add Component menu at the leftmost corner, add point Light.
Do hierarchy by using the ‘Attach’ menu

**Now we can drag this BP_Lamp into our earlier scene.**

Open the BP_Lamp and select **Event graph** We will see some starting nodes called Events.These events trigger action.We will use the BeginPlay event to get the lights flicker. Drag from this event, let goof the drag and select delay. We will get a node called Delay.Now in this delay node, it will expect a Duration input.Drag that Duration and search random, and select **Random float In range** node.set its min value and max value to **0 and 0.2** respectively.

**And we have a delay which will wait for random duration of 0 to 0.2 seconds.**

Next, drag a reference to our point light. Pull out a drag from this node and search for intensity, and copy the Random float node near Set Intensity node. and set the min and max values to **900 and 3000** respectively.


**Now lets connect delay node event line to Set Intensity node.**

* We wait for a random amount of time, then light will adjust its intensity to a random brightness, and repeat that indefinately, to repeat that indefinately, end of set intensity node and plug it to start of delay node.

