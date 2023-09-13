# Unity Photon Pun 2

This tutorial will guide you through integrating Photon Pun 2, which is used for multiplayer games and networking features. This guide assumes you are using Unity version 2021.3.5f1 and Agora Video SDK for Unity version 2.42.

## Prerequisites

Before getting started, make sure you have the following:

- Unity 2021.3.5f1 installed.
- Photon Pun 2 version 2.42
- Photon Account

## Project Setup

### 1. Create a Unity Project:

- Open Unity Hub, select "Projects," and click "New Project."
- Choose the 3D template and click "Create Project."
- Open your newly created project in Unity.

### 2. Integrate Photon Pun 2:

- Add to your assets the latest Agora Video SDK for Unity from the [Unity Asset Store](https://assetstore.unity.com/packages/tools/network/pun-2-free-119922).
- In Unity, go to "Window" > "Package Manager" > "My Assets."
- Find the PUN 2, click "Download," and then "Import."
- After importing the package it will ask for an app id, you have to generate it in the [Photon Pun 2 dashboard](https://www.photonengine.com/pun)
- App id is the connection between the project and the server. So it is important that it is added.
- You can also add it this way: "Window" > "Photon Unity Networking" > "PUN Wizard"

# Objects
## 1. Plane
- You will need a basic plane in the scene (also known as ground, it is where the players will walk)
- Right-click "3D Object" > "Plane".
![image](https://github.com/marcor0311/unity-photon-pun-2/assets/110083517/8e1b6b1f-6711-44b6-8cbe-712b853ce205)

## 2. SpawnPoint
- This has to be placed a little above the ground. (That way no player has a chance of falling into the void)
![image](https://github.com/marcor0311/unity-photon-pun-2/assets/110083517/4ddf0d27-44e8-4211-8650-47bb5ba8eca1)

## 3. RoomManager
- This will manage the players that will spawn in the spawn point (it will make sense a bit ahead)
- It is an empty object and it doesnt matter where it is placed.
![image](https://github.com/marcor0311/unity-photon-pun-2/assets/110083517/bc9eca8a-5716-4343-a1a7-0a423f831411)

## 4. Player
- Create a capsule and add a camera to the hierarchy (this is how the player will see)
- Then create a folder in Assets and name it "Resources". Grab the player from the scene and drop it in this folder. This will make the player a prefab
![image](https://github.com/marcor0311/unity-photon-pun-2/assets/110083517/9a77b35f-1db1-4779-b3ec-97ce836193ba)
![image](https://github.com/marcor0311/unity-photon-pun-2/assets/110083517/b9310f8f-b8e0-479c-8b66-ec2b63733282)

# Scripts
## RoomManager
Insider RoomManager add the script from "Code" > "RoomManager". 
In Player add the player prefab
In Spawn Point add the SpawnPoint object
![image](https://github.com/marcor0311/unity-photon-pun-2/assets/110083517/7e0288a2-9962-4538-b506-b8dbefad9541)

## Player Prefab
Inside the player prefab include this exact configuration (Movement and Player Setup are inside the folder "Code" in this repository, the other scripts are from Photon)
Double-click the prefab, that way you will be able to access the inspector of the player
![image](https://github.com/marcor0311/unity-photon-pun-2/assets/110083517/6257f968-d455-4dfd-be62-2ce3b310da60)
![image](https://github.com/marcor0311/unity-photon-pun-2/assets/110083517/d5990720-ee7b-47ec-9eb7-a1acc6ace185)
![image](https://github.com/marcor0311/unity-photon-pun-2/assets/110083517/5e3a2a05-d73c-4da6-b1c8-676ebe227a16)

Now you should be able to do multiplayer activities, congrats :)

Return to the main repository: [Unity Essentials Repository](https://github.com/marcor0311/Unity-Essentials)
