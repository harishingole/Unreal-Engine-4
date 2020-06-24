**Date : 23-June-2020 ||
Day :Tuesday**
****
****
## Lesson 4 :

**What we are gonna do in this Tutorial**
1. Play Info Enumeration with the information we want to track
2. PlayerSaveGame
2. Create thumbnails for the characters in our character select screen.
3. Intro and player variables
4. Map thumbnails
5. Character thumbnails
6. Lobby Map
7. Adding Blocking Volumes
8. Inside the MainMenu Map

Now lets do the thing 

### 1. Player Info Structure
>go to Blueprint -> AllLevels ->Double click on PlayerInfo, now we are in playerifo tab.

We need to create some variable in here that are going to pertain to our players. Create one variable name that ***MyPlayerName*** and the variable is gonna hold text value so data type should be text. Create One more another variable this one will be called ***MyPlayerImage*** and its gonna hold avatar that we allow them to select from so data type should be Texture2D Reference.Create third variable ***MyPlayerCharacter*** the type of thi svariable its going to be the character class. Another New variable this one will be called ***MyPlayerCharacterImage*** This is the image of the character that i have selected to play. And its gonna hold avatar so type will be texture2D. And the Last variable name is ***MyPlayerStatus*** and it will be text.

![PlayerInfo](https://user-images.githubusercontent.com/67138369/85403287-b8d7a800-b57a-11ea-8c0b-a28639461b65.png)

### 2. PlayerSaveGame

>go to Blueprint -> AllLevels ->Double click on PlayerSaveGame, now we are in playerifo tab

Inside of this, its going to be very short. for this we are gonna do is create variable to hold our PlayerInfoStructure locally. Create variable and its going to be called ***S_Playerinfo***. We need to change it to the Player infor Structure type.This variable does need to be replicated. just save this and close it

**Now lets go into Maps folder Open the Arena_01**

Inside theArena_01 go to World Settings, we are going to specify to use our Game mode - select GameplayGM and expand Selected GameMode, Select GameplayPlayerController just save it. Now Create Some Photo Session for all our characters because we need some thumnails to represent the characters and Maps. *Look at the following thumbnails*


### Maps 
**1. Arena 01**
![Arena 1](https://user-images.githubusercontent.com/67138369/85405032-72d01380-b57d-11ea-91b7-a8c3b54ab286.jpg)

**2. Arena 02**

![Arena 2](https://user-images.githubusercontent.com/67138369/85405107-8c715b00-b57d-11ea-91ac-f6454a6ab918.jpg)

### Characters

**1. Barbarous**
![Barbarous](https://user-images.githubusercontent.com/67138369/85405186-a4e17580-b57d-11ea-8e66-93bb49c9ce34.png)

**2. Forge**
![Forge](https://user-images.githubusercontent.com/67138369/85405513-276a3500-b57e-11ea-9f12-b38ab392b940.png)

**3. Frosty**
![Frosty](https://user-images.githubusercontent.com/67138369/85405526-2afdbc00-b57e-11ea-9d6c-f6b023330ea5.png)

**4. Natural**
![Natural](https://user-images.githubusercontent.com/67138369/85405530-2cc77f80-b57e-11ea-9a92-b6b8e3f44d41.png)

**5. Pit**
![Pit](https://user-images.githubusercontent.com/67138369/85405535-2fc27000-b57e-11ea-8580-77109709bd42.png)

**6. Robo**
![Robo](https://user-images.githubusercontent.com/67138369/85405541-318c3380-b57e-11ea-8f93-adcab0ae3219.png)

**7. Tusk**
![Tusk](https://user-images.githubusercontent.com/67138369/85405547-32bd6080-b57e-11ea-9450-6659849dbe78.png)


**8. Warrior**
![Warrior](https://user-images.githubusercontent.com/67138369/85405550-34872400-b57e-11ea-887d-884e3d114c9f.png)


We have taken all the thumbnails. so we have 8 characters and our 2 maps now just import thos thumbnails inside our texture folder. *Double - click* to open up **Lobby** - Inside the lobby Players can run and hang out before they jump into tha actual gameplay. Player can chat select their character and perform actions with thier characters.Eventually, we will turn this into something much cooler than this empty lab of block. Create 8 players in Lobby.

The other Things to do we go to World settings assign the lobbyGameMode here and its going to use the lobby player controller, so select Lobby player controller so to use LobbyPC.Default Pawn Class to 0_Base.The last Thing is add some Collision Boxes around the side so Players can't fall off the level into the world.

![Lobby](https://user-images.githubusercontent.com/67138369/85407069-5a152d00-b580-11ea-8797-43a027a8a574.png)







