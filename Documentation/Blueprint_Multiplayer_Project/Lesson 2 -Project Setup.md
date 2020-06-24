**Date      : 22-June-2020 ||
Day         : Monday**
****
****

## Lesson 2

## Project Setup

**In this tutorial create project with any template, I have create with thrid Person**

The First thing i did is import character. just go to the Marketplace and search infinity blades. I used Infiniy blades : Warriors pack just click on that its total free of cost. it will download, After finishing download it will add in vault. just click on add project, Select your Project which you created before.

**Lets go and set up folder structure and get that out of the way**

* Go to Root folder i.e Content folder - Right-Click and select New Folder Rename this folder as "Blueprint" because its going to hold all of our Blueprints.
* Again create one more folder Called Map which is used to hold our maps
* Next is Textures Folder, Its going to hold our thumbnails of our maps and our character for select screen.
* create folder called as UI, it will hold our UI content. 

**Now Within the Blueprints and UI i created some sub-folders in there**
# Blueprints
* AllLevels
* Characters
* Lobby
* Gameplay

# UI
* AllLevels
* Lobby
* MainMenu

Thats i have setup our folder now i had gone inside of each folder and create some of this assets that we are gonna need.

Inside the **AllLevels folder** of Blueprint create a blueprint classes.
* GameInstance - GameInstance object for an instance of the running game. "its is kind of like the king of the blueprint"  select Game instance and rename it with GameinfoInstance

* Next assets that we gonna need is, Right-Click go to Blueprint select Structure remane it with Playerinfo - its gonna hold all the information about our player, such as their character, their avatar, their name etc
* Now e are gonna looking for a SaveGame go to Blueprint class search SaveGame select it rename with PlayerSaveGame -  that will sav our player name avatar and a lot of information Basically, It is going to save a version of our playerInfo locally and then upload that information to our server, who will distribute to all of our clients. then, our clients will know our names, our character etc , then Save All


Now go to ThirdPersonBP -> Blueprints -> in that copy ThirdPersonCharacter and paste it in Character Folder of BluePrint and rename that character to 0_Base and open it. It has all the script in there for moving around, so we will hav a character that can move and jump etc 

Now create child of this blueprint (0_Base Character) so it will inherit all of that movement functionality as well as any changes we make to this will be passed on to its children. So the inhrited functionality will make it a lot easier to have different character later

**Now Lets Create Child Blueprint Class**
**Following are the nine characters one of which is base character.**
* Barbarous - Its going to be one of the characters that we are gonna use
* Forge - 
* Frosty -
* Natural -
* Pit -
* Robo -
* Tusk -
* Warrior -


**Now Select Gameplay folder we are going to create two Blueprints in here**

1. GameMode
2. PlayerController

**Both the assets paste in lobby folder AND rename both of this LobbyGameMode and Lobby PlayerController**

**Now creates some maps**

* Select Map Folder and clone the existing map that i created while creating project That is ThirdPersonTemplate
* On the basis of ThirdPersonTemplate create two more map rename it with Arena 1 and Arena 2 with multiple Player Start save as Arena_1 and Arena_2 in Maps Folder.

**Now lets create New Level**

* Select Default level as our lobby Map save it as **Lobby.**
* Now create Empty level and save as **TravelMap**
* Now create Empty level and save as **MainMenu**

**Lets create some widgets in UI folder like Widgets Blueprint**

**AllLevels**
1. ChatText 
2. ChatWindow  
3. GamePlayChat  
4. LoadingScreen  

**Lobby**

1. **CharacterSelect** -This is our character Select Screen 
2. **Connected Player** - we are gonna use this for player card. it represent the lobby
3. **GameSettings** - Server can define
4. **LobbyMenu** - its a lobby mainu
5. **PlayerButtons** - which is gonna be used for the server only, it will allow the server to kick somebody


**MainMenu**

1. **ErrorDialogue** - all th eerror messages put here
2. **HostMenu** - player choose to host a game on the MainMenu
3. **MainMenu** - 
4. **OptionsMenu**
5. **ServerMenu** - when you click find a game, you will be present with this menu

**All the Assets setup.**

**Lets go the Project Settings -> Maps & Modes -> Set all defaults now**
* For Editor Startup Maps select MainMenu
* For Game Default Map select MainMenu
* For Transition Map select travelMap for transitioning from one map to another 
* For Server Default Map select MainMenu.
* For GameInstance select our GameInfoInstance

**All our Project Settings Setup.**

The Last thing in this tutorial we need to do is set up the Animation Blueprint for our  characters because our infinity blade warriors do not have any animations with them, They are just the Skeletal Meshes. The animations that come with Manequin here as the animations for our character. Actully we are working on getting clients connected to a server.

**Now Lets go to the Maniquin -> Character -> Mesh -> Open the Skeleton by double-Click to open up skeleton** 


Now just click on Retarget Manager it's going to pop up new window

>Go to Set up Rig -> Select Humanoid Rig -> close -> save
>Like this we have to do for all skeleton

Now go to Manequin folder in that Animations - Right-Click on ThirdPersonAnimBP - Duplicate Anim Blueprints and Retarget. it will open a window and Retarget it - Select all of those animations which it did. Move all the animations and paste it with new folder[Animations] inside the **infinityBladesWarriors**. Rename all the animations.


