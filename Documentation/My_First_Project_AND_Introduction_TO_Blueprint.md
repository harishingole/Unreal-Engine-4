**Date : 19-June-2020
Day : Friday**

****
****

**"I tried to create a simple project so terms and problem i note it down..."**

Click on **New Project** we've two choices; either Blueprint or C++. 
**Blueprint** is Unreal's visaul scripting language, which is amazing and Which is pretty good
**C++** is our old school proper coding. for that we need to able to c++ to create a game but for large a game go with c++.

* Choose Template like First Person, Flying, Puzzle etc
* I choose First Person the some settings
* like Desktop, Starter Content, Performance of display then create project

**Create new level :** Go to File - New Level or Ctrl+N select default level

****
****

# Introduction to Landscape 

**How to create Landscape in Unreal Engine**

**Step 1 :** Go to landscape in Modes panel and click or you can press 'Shift +3'
 
 * in the modes select manage section of the tool within that there is lots of different bits and bobs that we can change : 

* **Create New :** It will create a new landscape
* **Import From File:**  bring the eternal information
* **Material :** Assign a material it can be grass or choose other
* **Layer :** it covers Location, Rotation and scale
* **Section Size :** this is important for determining how UE4 handles the level of detail and calling via landscape 
* **Section per Components:** it is also tied to level of detail system. Its a largest unit of a landscape, each component can be made up of multiple sections for ex.it could be either 1*1 which is one square.
* **Overall resolution:** this is the number of vertices that ae used in your landscape the higher the number more detailed it'll be but the more CPU intensive.
* **Total Components:** this basically takes all the settings above into considerationand calculate how many components in your landscape is going to be made up of last two buttons at the bottom are filled world which wll just create the largest possible landscape that the engine can handle. chnage the details and **create it**

The details are :
Section Size is 31*31;
Section Per Components : 1*1;
now just click on **create button**

## Introduction to Blueprint
The **Blueprints Visual Scripting** system in Unreal Engine is a complete gameplay scripting system based on the concept of using a node-based interface to create gameplay elements from within Unreal Editor. As with many common scripting languages, it is used to define object-oriented (OO) classes or objects in the engine. As you use UE4, you'll often find that objects defined using Blueprint are colloquially referred to as just "Blueprints."



**How Do Blueprints Work?**
In their basic form, Blueprints are visually scripted additions to your game. By connecting Nodes, Events, Functions, and Variables with Wires, it is possible to create complex gameplay elements.

Blueprints work by using graphs of Nodes for various purposes object construction, individual functions, and general gameplay events that are specific to each instance of the Blueprint in order to implement behavior and other functionality.

**Level Blueprint**

![Level Blueprint](https://docs.unrealengine.com/Images/Engine/Blueprints/GettingStarted/Level_Blueprint_Main.webp)

The Level Blueprint fills the same role that Kismet did in Unreal Engine 3, and has the same capabilities. Each level has its own Level Blueprint, and this can reference and manipulate Actors within the level, control cinematics using Matinee Actors, and manage things like level streaming, checkpoints, and other level-related systems. The Level Blueprint can also interact with Blueprint Classes (see the next section for examples of these) placed in the level, such as reading/setting any variables or triggering custom events they might contain.

**Blueprint Class**


Blueprint Classes are ideal for making interactive assets such as doors, switches, collectible items, and destructible scenery. In the image above, the button and the set of doors are each separate Blueprints that contain the necessary script to respond to player overlap events, make them animate, play sound effects, and change their materials (the button lights up when pressed, for example).

In this case, pressing the button activates an event inside the door Blueprint, causing it to open - but the doors could just as easily be activated by another type of Blueprint, or by a Level Blueprint sequence. Because of the self-contained nature of Blueprints, they can be constructed in such a way that you can drop them into a level and they will simply work, with minimal setup required. This also means that editing a Blueprint that is in use throughout a project will update every instance of it.

![](https://docs.unrealengine.com/Images/Engine/Blueprints/GettingStarted/Blueprint_Main.webp)
