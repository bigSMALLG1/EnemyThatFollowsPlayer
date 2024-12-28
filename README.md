# EnemyThatFollowsPlayer
This tutorial will demonstrate how to program an enemy that follows the player in Unity 3D using C#. This will also cover how to set up the Unity 3D environment, as well as common practices when writing scripts.

1. Create a new Unity project using the Universal 3D pipeline and name it "EnemyThatFollowsPlayerTut".
   ![image](https://github.com/user-attachments/assets/fba486e4-525e-44af-8a24-823b3dff1f12)

2. Once the Unity project has loaded, start by creating a terrain for our game objects to be on as we will be adding gravity to our game objects through rigidbody components.
   ![image](https://github.com/user-attachments/assets/56c6fe36-2a2e-407d-80c8-adcaba55e7a9)

   From here we can also create a 3D capsule that we will use as our player in this scene. Once the capsule game object is created, change the value of it's Y position to 0 in the inspector on the right.

   ![image](https://github.com/user-attachments/assets/8b5d2489-f241-4021-95f5-a15fd508bafe)

    Rename the capsule to "player" by right clicking the capsule in the hierarchy and renaming it and then move the terrain so that it is centred on the player and then create another capsule called "Enemy" and move it away from the Player.

   ![image](https://github.com/user-attachments/assets/7e5f081e-6d17-43ab-bb17-b5aece255fe2)

4. Right click in an empty space in the assets window at the bottom and create a new MonoBehaviour Script and name it "enemyFollow". Once it is created, open the script in to Visual Code or Visual Studio Code.

