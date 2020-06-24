**Date : 23-June-2020 ||
Day :Tuesday**
****
****
## Lesson 3 

In this Lesson I am going to start working on the **Game Info Instance**. Which will set up our front end and handle the main menu, as well as some of the other settings like launching lobbies and things like that

Q.1 What is Event Graph.?

The EventGraph of a Blueprint contains a node graph that uses events and function calls to perform actions in response to gameplay events associated with the Blueprint. This is used to add functionality that is common to all instances of a Blueprint. This is used to handle events for the level as a whole and to add functionality for specific instances of Actors and Blueprints within the world.

In either case, an EventGraph is used by adding one or more events to act as entry points and then connecting Function Calls, Flow Control nodes, and Variables to perform the desired actions.

### Working with Graphs

The Graph tab displays the visual representation of a particular graph of nodes as it shows all of the nodes contained in the graph as well as the connections between them. It provides editing capabilities for adding and removing nodes, arranging nodes, and creating links between nodes. Breakpoints can also be set in the Graph tab to aid in debugging Blueprints.

This is the example of Event graph

![Event-Graph](https://docs.unrealengine.com/Images/Engine/Blueprints/UserGuide/EventGraph/k2_graphview.webp)

### **Now Lets Graph Editor is What Actually Looks Like..?**

The Graph Editor panel is the heart of the Blueprint system. It is here that you will create the networks of nodes and wires that will define your scripted behavior. Nodes can quickly be selected by clicking on them and repositioned via dragging

![GraphEditor](https://docs.unrealengine.com/Images/Engine/Blueprints/Editor/UIComponents/GraphEditor/GraphEditor.webp)

1. **Graph Area** - This is where you will actually lay out all of your nodes.

2. **Forward and Back Buttons** - These allow you to jump between different graphs very much as you would navigate a web browser.

3. **Tabs area** - As you open different graphs, tabs for each one will open here, allowing you to quickly jump between different graphs.

4. **Breadcrumbs** - These show a progression of graphs and subgraphs. As you step down into functions or collapsed graphs, this will show you where you are within your network.

5. **Zoom Factor** - This simply shows the current zoom ratio in the graph editor.

6. **Blueprint label** - This shows the type of Blueprint you are editing. As you edit Blueprint Interfaces, Animation Blueprints, Macros, and other types, this label will update


#### *Now Lets go into Blueprint -> AllLevels -> GameInfoInstance by double-click on that. it will open a fresh graph, so lets start working inside the graph*



### 1.**Show Main Mnu and Enable Mouse Cursor**
1. Right-Click on graph and create custom Event rename it with *"ShowMainMenu"*        
2. Right-Click on graph and create widget.
3. Right-Click on Return Value in widget -> **Promote to Variable**, rename the variable **MainMenuWB**
4. Go to Details Panel just for cleanliness, make the category call Widgets.
5. Select the **MainMenuWB**, Hold Control and drag it into the graph and Drag of this and type Is Valid.
6. Plug in with the variables.

>The Essentiall this is check the widget already bee created, if it has we are going to do is add to the viewport, if it hasn't then we are going to create it

7. Right-Click and type *"Get Player Controller"*
8. drag off the return value from Get Player Controller, search **Set Show Mouse Cursor** connct with Return value anothe plug in to viewport.

**Look at the below Image** 

![Show Main Menu and Enable Mouse Cursor](https://user-images.githubusercontent.com/67138369/85398940-91311180-b573-11ea-946e-f7c5d918834d.png)

Just like the above custom event i created 9 see the following images which I have created events

### 2.**Host Game Menu** 

![Host Game Menu](https://user-images.githubusercontent.com/67138369/85399488-875bde00-b574-11ea-9cec-17077562e095.png)

### 3.**Shows the Server Menu -  Created each time its called**

![Shows the Server Menu -  Created each time its called](https://user-images.githubusercontent.com/67138369/85399704-dbff5900-b574-11ea-86cb-e2c8b9de2898.png)

### 4.**Show The Options Menu**

![Show the Options Menu](https://user-images.githubusercontent.com/67138369/85399843-1b2daa00-b575-11ea-8ae7-29517d5792a3.png)

### 5.**Shows the loading Screen When Called**

![Shows the loading Screen When Called](https://user-images.githubusercontent.com/67138369/85400051-6fd12500-b575-11ea-91ed-af03fad2a188.png)

### 6. **Launch the Lobby with Host Settings**

![Launch the Lobby with Host Settings](https://user-images.githubusercontent.com/67138369/85400279-cb9bae00-b575-11ea-8741-0c408cbc64fb.png)

### 7. **Join Server - Called from Server Menu**

![Join Server - Called from Server Menu](https://user-images.githubusercontent.com/67138369/85400461-0ef61c80-b576-11ea-8839-2941ed8befcf.png)

### 8. **Handle Network Error and Display Message**

![Handle Network Error and Display Message](https://user-images.githubusercontent.com/67138369/85400606-4f559a80-b576-11ea-9182-5b058601fb04.png)

### 9. **Handle Travel and Display Message**

![Handle Travel and Display Message](https://user-images.githubusercontent.com/67138369/85400754-8deb5500-b576-11ea-8066-3580c402c4c8.png)

### 10. **Destroy Session When Called**

![Destroy Session When Called](https://user-images.githubusercontent.com/67138369/85400918-c9861f00-b576-11ea-8b0a-1b79d7a6461e.png)
