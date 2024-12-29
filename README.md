# EnemyThatFollowsPlayer
This tutorial will demonstrate how to program an enemy that follows the player in Unity 3D using C#. This will also cover how to set up the Unity 3D environment, as well as common practices when writing scripts.

1. Create a new Unity project using the Universal 3D pipeline and name it "EnemyThatFollowsPlayerTut".

    ![image](https://github.com/user-attachments/assets/fba486e4-525e-44af-8a24-823b3dff1f12)

3. Once the Unity project has loaded, start by creating a terrain for our game objects to be on as we will be adding gravity to our game objects through rigidbody components.

   ![image](https://github.com/user-attachments/assets/56c6fe36-2a2e-407d-80c8-adcaba55e7a9)

   From here we can also create a 3D capsule that we will use as our player in this scene. Once the capsule game object is created, change the value of it's Y position to 0 in the inspector on the right.

   ![image](https://github.com/user-attachments/assets/8b5d2489-f241-4021-95f5-a15fd508bafe)

    Rename the capsule to "player" by right clicking the capsule in the hierarchy and renaming it and then move the terrain so that it is centred on the player and then create another capsule called "Enemy" and move it away from the Player.

   ![image](https://github.com/user-attachments/assets/7e5f081e-6d17-43ab-bb17-b5aece255fe2)

5. Right click in an empty space in the assets window at the bottom and create a new MonoBehaviour Script and name it "enemyFollow". Once it is created, open the script in to Visual Code or Visual Studio Code.

6. We can delete the start method as we will not be using it in this script and it is also good practice to not have unused methods in your code, making it neater and easier for others to read.

7. Next, we shall define our variables. We will need a float variable to store our enemies speed and a transform to store our targets position, rotation and scale. See syntax below.

    ![image](https://github.com/user-attachments/assets/ebc1274a-e215-48e4-b14d-d4b531aed97b)

8. Once you have defined your variables, we will simply be using one line of code in the update method to change the position of our enemy in accordance to the position of the target (player). We are doing this in the update method so that our enemy is
   constantly moving towards our player. See syntax below.

   ![image](https://github.com/user-attachments/assets/2c9d5636-9c93-481d-bab2-ed459c81790e)

Vector3.MoveTowards calculates the position between the two points we have specified which are: transform.position (position of the enemy) and target.position (position of the player or target) moving no further than the distance that we have specified in our enemySpeed variable multiplied by Time.DeltaTime. This then returns the new position which is our transform.position and the function repeats again as it is inside of the update method.

9. Go back in to unity and assign your player gameobject to the target box in the script in the inspector.

   ![image](https://github.com/user-attachments/assets/2df18cf3-e5a6-4e49-a3d5-47c1658daacc)




