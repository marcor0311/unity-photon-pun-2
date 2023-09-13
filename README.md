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

# Objects
## 1. Plane
- You will need a basic plane in the scene (also known as ground, it is where the players will walk)
- Right-click "3D Object" > "Plane".

## 2. SpawnPoint
- This has to be placed a little above the ground. (That way no player has a chance of falling into the void)

## 3. RoomManager
- This will manage the players that will spawn in the spawn point (it will make sense a bit ahead)
- It is an empty object and it doesnt matter where it is placed.

## 4. Player
- Create a capsule and add a camera to the hierarchy (this is how the player will see)
- Then create a folder in Assets and name it "Resources". Grab the player from the scene and drop it in this folder. This will make the player a prefab

# Scripts
## RoomManager
Insider RoomManager add the script from "Code" > "RoomManager". 
In Player add the player prefab
In Spawn Point add the SpawnPoint object

## Player Prefab
Inside the player prefab include this exact configuration (Movement and Player Setup are inside the folder "Code" in this repository, the other scripts are from Photon)

Now you should be able to do multiplayer activities, congrats :)

Return to the main repository: [Unity Essentials Repository](https://github.com/marcor0311/Unity-Essentials)