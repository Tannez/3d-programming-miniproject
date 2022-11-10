# 3d-programming-miniproject
Miniproject made by Markus Nielsen for Programmering af interaktive 3D verdener

Overview of the Game:

This project is a first-person shooter heavily inspired by the Star Wars Dark Forces games, which have used the same engine as DOOM. The player is put in a closed off arena, where the player must shoot incoming enemies to get the highest score possible.  The player uses both keyboard and mouse controls to move around the field and shoot enemies.  The goal of the game can be two things, depending on who is playing. Either to get the highest score possible, by killing enemies or to survive as long as possible, by not getting hit by the enemies. The game becomes progressively harder with time as enemies keep spawning and you only have a limited amount of health, which cannot be regained. The game also becomes harder as the player has a certain number of bullets and can only regain bullets from killing enemies and collecting magazines. Therefore, the player must manage how they use their bullets.  

The main parts of the game are:

•	Player – First-person character moved with the WASD and SPACE keys. Hold SHIFT key to sprint
•	Camera – Follow the player and can be rotated with the mouse.
•	Gun – Shoots instantiated bullets when pressing the left mouse button. The player can switch between single fire and rapid fire by pressing R.
•	Magazines – Magazine objects are spawned on the field when enemies are killed. Each magazine gives 20 bullets to the player’s bullet meter.
•	Enemies – Tough, Normal, and Weak enemies, are spawned in random places set in the inspector and move toward the position of the player using a NavMeshAgent. Every enemy has a different amount of health and range of damage, with Tough being the strongest and weak being the weakest. Enemies damage the player through collision and are destroyed if hit by enough bullets to take down their health. Killing an enemy spawns a magazine object and add points to the score.
•	Score – Counts a score based on enemies killed. Each enemy type grants different points.
•	Play field – Close-off space where the player can freely move. The player cannot go out of the field.
•	Player Health – The player starts with 100 health. Once all lives are removed the game ends.
•	Bullet meter- Shows the player how many bullets they have left. Meter can only be filled from collecting magazines.
•	Timer – Shows how long you have survived.


Game features:

•	Positions and types of enemies are randomly selected each time helping with replay-ability.
•	The difficulty of the game becomes harder with time, as 
  o	Enemies keep spawning,
  o	Player never regains health. 
  o	Player must manage their bullets and always make sure they have enough to kill incoming enemies.
•	The game keeps track of the score and time.

Project Parts:

•	Scripts:

  o	Enemy1, Enemy2, Enemy3 – Scripts for the different types of enemies. 
    	Scripts don’t have much difference, but the original intent was to give each enemy a different attribute, but it was never implemented.

  o	EnemySpawn – Spawns enemies in random positions, set in the inspector. 

  o	Gun – Allows shooting and manages bullets.

  o	HealthBar – Manages health.

  o	ScoreManager – Manages score.

  o	Timer – A timer.

  o	MagazinePickUp – Used to add bullets to gun when player collides with magazine object.

  o	EndGameUi – Manages Game state, displays final time and score, as well as when to display the end game screen.

  o	FirstPersonController – Controls the player (from unity starter assets).

  o	BasicRigidBodyPush – Rigidbody (from unity starter assets).
  

•	Models & Prefabs:

  o	Enemy models, bullets and magazine object made with Unity primitives

•	Materials:

  o	Basic Unity materials for highlighting different enemy types, bullets, gun, walls.

•	Scenes:

  o	Game consists of one scene

•	Testing:

  o	Game was tested on Windows, game cannot be currently played on a mobile platform


Used Resources:

•	Inspiration to spawn enemies at random positions: https://answers.unity.com/questions/810806/spawn-random-enemy.html.

•	Unity Starter Asset: https://assetstore.unity.com/packages/essentials/starter-assets-third-person-character-controller-196526 

•	Inspiration for making gun: https://www.youtube.com/watch?v=wZ2UUOC17AY    
