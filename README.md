# in-class-activities
## Devlogs
### W1
Hello World!

### W2
Create future Devlog sub-headers with the three # symbols, then write your Devlogs below them.
1. The reason why the variables r, g, and b are considered as float variables, instead of int, bool, or string variables is because these numbers contain decimal points. 

2. The _bounce variable is considered an int because we are given a whole number, rather than a decimal.

3. The only error I've gotten was not including the float variable.

### W3 

Table 6: Rythem Game Project
   A boolean method is very necessary for to achieve this goal to decide whether or not the player successfully hit a beat. It allows the game to return either true or false based of the timing of the players input, which is critical for scoring and feedback in the rhythm game. By comparing the player's key press time to the expected beat time, the method helps decides if the input is accurate enough to interact with the beat.
2. Writing a metaphor Cooking: Recipe

   The relationship between the classes and components can be compared to cooking a recipe. A class function like the recipe itself is basically a representation of a normal blueprint that outlines the ingredients and steps to create a dish. When you attatch a script GameObject, it becomes a component, much like preparing a specific meal using that recipe. Member variables can be used to adjust the setting of several objects that comes with the recipe and the ingredients it contains, such as the spice level or cooking time, which in unity turned through the inspector. Methods represents the step by step process of the cooking recipe that brings the dish to life, like mixing or baking. This metaphor gives our group a good understanding on how scripts becomes functional parts of a GameObject, and how each instance that we create can be customized with different values to produce behaviors, just like cooking the same dish with different flavors. 

4. The Ball Brightness??

The ball gets extremely bright after repeating bounces because their velocity increases each time, and that velocity is directly tied to brightness. Apparently I heard that the colors values in unity tends to not clamp when the ball bounces almost consistently in which the brightness can exceed the normal range, causing the balls to appear overly bright. This shows how small changes in physics like increasing velocity can quickly have a big impact on how things look in the game.

### W4 
Table #6
1. Lines 5 and 22 are declaring the member variables movement for the cat object, while lines 22-25 are declaring the direction for the cat.

Table #6 

2. For our scene, we added Rigidbody components to the Cat and SoccerBall because both objects need to interact with physics. The cat kicks the ball, and the ball bounces off walls and moves. We did not add a Rigidbody to the Goal, since it’s a static object that doesn’t need to move.

3. We checked Is Trigger on the Goal’s Collider so it could detect when the ball enters without physically blocking it. This allowed us to trigger goal-scoring logic without interfering with the ball’s movement. We left Is Trigger unchecked on the Cat and SoccerBall because they need real collisions for bouncing and kicking.

### W5 
1. How can we use GameObjects and Components to use vectors?

By effectivly using GameObjects and Components with vectors, you can create dynamic and interactive game environments that enhances the player's experiences. 

2. Planning the DeerW5 Script:
   1. We determine where the deer should go by using the _destination variable. 
   2. In the Start() method, we use GetComponent<NavMeshAgent>() to access the NavMeshAgent component attached to the Deer GameObject.
   3. Once we have access to the NavMeshAgent, we call SetDestination(_destination.position).
   
### W6
Activity 1: https://docs.google.com/document/d/1IZFJUcFgjnf2ph_xvqjTaqAltUuFe4KMaDIYs-4cPV8/edit?usp=sharing

Activitiy 2: 
Steps for BatW6:
Member Variables: 
_speed (float) - controls how fast the bat moves toward the player. 
_playerTransform - Stores the players position so the bat knows where to chase
_messages - hold possible reaction messages the bat can say

Methods:
Update();

DisableChase(); - stops chasing 
SayMessage(); - Picks a random message from _messages and displays it

CreateReactions(BatW6 bat) - called when a bat is very close to the player

SpawnReactionUI(BatW6 bat, string message) - spawns a text object near the bat. 

What should the methods do:
EnableChase() turn on chasing and store the players position

DisableChase() - Stop chasing by disablings the script. 

Update() - move the bat towards the player every frame.

sayMessages() - randomly select and display a message.

CreateReactions() - check cooldown timer, then spawn a message.

SpawnReactionUI() - Instantitate a UI text. 

### W7
1. Google docs: https://docs.google.com/document/d/1ACCBYMqYrHTf6bSU9TNPsHK5OQnuA3CH1FFEp9_a9kQ/edit?tab=t.0

2. The original code used transform.position += to move the muskrat, which  directly changes its position in the world. This caused problems because it bypasses Unity's physics systen and ignores the Rigidbody component. Since the muskrat uses a Rigidbody for movement and jumping, it's important to move it in a way that works with physics. I fixed it by using transform.Translate(), which still moves the Muskrat smoothly but respects its Rigidbody and keeps the movement consistent with the rest of the game. 



## Open-Source Assets
### W3
1. Table 6: Rythem Game Project
   A boolean method is necessary 
   KeyPress and time 

2. 
- Animals: https://assetstore.unity.com/packages/3d/characters/animals/animals-free-animated-low-poly-3d-models-260727 
- Low-poly environment: https://assetstore.unity.com/packages/3d/environments/landscapes/low-poly-simple-nature-pack-162153 
