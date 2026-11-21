# B2030-9---K-CS3-Project
# B2030-9---K-CS3-Project
Project Proposal Template

Project Title or 
Name of the Application	: The Crimson Court of Caerwick 
Section			   	: 9 - Potassium
Group Members			: Gabriel Alfonso Ascano, Nathan Ray Gabito, and Venyceson Reyes 	
Date (Proposal Date)		: November 21, 2026

Project Description:
The Crimson Court of Caerwick is a low fantasy medieval RPG game set in the fictional Kingdom of Caerwick following the death of King Edric “the Just” III and the subsequent succession crisis. Players assume the role of an adventurer whose decisions, alliances, and actions influence the kingdom's political landscape. They can select a character class, acquire equipment, complete quests, interact with non-player characters (NPCs), engage in turn-based combat, and explore the kingdom's diverse regions. The game primarily takes place in Aurecourt, the kingdom's capital and center of political power, where competing noble houses struggle for influence over the vacant throne.

The project aims to provide an fun, engaging, and interactive entertainment experience through exploration, character progression, and consequential decision-making. It will also serve as an application of Python object-oriented programming (OOP) with the use of classes, attributes, methods, inheritance, encapsulation, inheritance, polymorphism, and more to create and build the game.

Classes:
Character Class:
  This is the class the people that interact will have. They have 7 attributes and 2 methods:
    Attributes: Their name as a string, their health points and rawattack points as integers, their x position and y position as integers to track their movement, their specialAbility as a string, and their Allied_House       as a string.
Methods: 
  move(): This is used for them to move around the kingdom and interact with the NPCs. 
  faint(): When a player gets 0 HP, they will be transported to a clinic, and will have to wait for a bit until they play again.

Two classes inherit from Character: Player and NPC
  Player Class:
    This is the class the user will control. Player inherits all attributes from the Character, with addition to an inventory full of the weapons they use. All methods are also inherited, with addition to two new methods.     The first one is an encounter method, which is executed when the Player goes near an Enemy. This makes the Player dependent on an NPC. There is also a flee method, allowing the player to run away from these                encounters. 
  NPC Class: 
    NPC inherits all methods and attributes from Character. However, the move method is now at random because no one controls the NPC. 
    The NPC is very important because it interacts with many other classes for both game and story progression:
  Offensive and Miscellaneous inherit from NPC:
    The Offensive class is a class that can deal damage and make a player faint whenever the two interact:
      Its attributes and methods are all inherited from NPC, with addition to a “damage” attribute which is an integer that adds on to the rawattack attribute at random. This determines how many health points the Player         loses when it attacks. 
      One more class inherits from the Offensive Class: Soldiers
        The Soldiers class inherit everything from the offensive class, but there is an extraEncounter()  method that makes it easier to encounter compared to other NPCs.
        Soldiers can also be Knights, which inherit everything from the soldiers, but have better stats (health and damage) overall

The Miscellaneous Class on the other hand: 
  Are those that are incapable of doing damage to the player character. Rather, they serve as support characters, or peons for the plot of the story, but still help with its progression. However, they still inherit every    attribute and method from NPC except for “rawattack.” and move().
  In our shown class diagram, 3 other classes inherit from this, namely: 
    Quest Giver: This will serve as the main class for characters in our game that will give quests through the method assignQuest(). It doesn’t move and forms a multilevel inheritance with Character, through NPC, and         then Miscellaneous, inheriting its attributes such as health, x and y position, name and joined kingdom. In addition, quest giver has a Composition relationship with Class Quest.
        Class Quest:
          This class contains all key properties and attributes of an ideal quest in our game, which includes the quest string or statement. And to reward players, upon completion, a reward may be given by completing the            quest.
    Thief: This class also undergoes a multilevel inheritance with Character, through NPC and Miscellaneous to inherit name, x and y position, joined kingdom, and health attributes. In order to make this character more        unique, we gave it the ability to steal/plunder, move and faint through the methods plunder(), faint() and move().
    Trader: The Trader class brings life to a new character as it inherits all its attributes from Character, giving it health, an x and y position and which house it belongs to. It allows the player to trade with it          through method trade(), and doesn’t move places for convenience. 

House Classes contain NPCs in an aggregation relationship:
  It has 3 attributes and 2 methods:
    Attributes: An NPC house_ruler, a house_members list filled with NPCs and the Player, and the house name as a string.
    Methods: There is one method to join an alliance with another House to form a bigger list of Houses, or declare war on a house. Depending on where the player joins, these declarations could be random because other       Houses could declare war on the player’s house.
    Houses could be “Allied Houses” or “Opposing Houses depending on the alliance you have with them:
        AlliedHouse Classes inherit everything from the normal house, but it also includes the x and y positions of the house as integers. In addition, it also has the method recruitAllies(), which allows you to recruit           more members for the houses.
        Opposing House Classes are Houses that your alliance houses have declared war on. They inherit everything from the House, and it also contains x and y positions as integer attributes.

The intended users are players interested in medieval fantasy, RPGs, exploration, and narrative-driven experiences or just anyone who enjoys interactive storytelling and strategic decision-making.

<img width="419" height="366" alt="image" src="https://github.com/user-attachments/assets/65c9a3ed-ea1c-4d10-962d-2bb97370a3b1" />


Goals:
Objective 1: By the end of project development period, we want to make a playable 2D top down low fantasy medieval RPG European-inspired setting with at least three explorable and interactive settings, five interactive non-playable characters (NPCs), and two distinct main factions, each with its own identity and interests, showing the application of python object-oriented programming (OOP) and worldbuilding.

Objective 2: By the end of project development period, we want to make at least four main gameplay systems, namely, character progression, inventory management, quest management, and turn-based combat, showing the application of python object-oriented programming (OOP) and worldbuilding.


Objective 3: By the end of project development period, we want to make at least three conquestial player decisions that 
	affect the storyline, faction relationships, and quest outcomes. We also want to make at least two distinct possible endings. 
	We will validate the game’s functionality through systematic play testing.









Signatures:





Gabriel Alfonso Ascano 
Nathan Ray Gabito
Venyceson Reyes





Roy Vincent Canseco 


Hi Sir. Roy! We hope you like this project proposal because we’re actually quite passionate about it! All of us in our group are quite interested in these types of “interactive RPGs” and the worldbuilding behind them, so it would be REALLLLLLY cool if you liked it too po!!! Thank you!!!

Google Document Project Proposal Link: https://docs.google.com/document/d/1OYx6tYv5j-dMb8ukUuVH995kG_sb6tQgWylzicBD3i0/edit?tab=t.0

Mode of Submission: through KHUB with a link to your README.MD inside your github account  (GitHub or https://github.com/) NOTE: Create an account for your project (one is the owner two will be collaborators)










Project Proposal Rubric (20 Points)
Criteria
4 - Exemplary
3 - Proficient
2 - Developing
1 - Beginning
Points
Project Description & Need
Clearly explains the application's purpose, the problem it addresses, and why it is needed.
Explains the purpose and need with minor gaps.
Purpose or need is somewhat unclear.
Description is incomplete or unclear.
/4
System Features & OOP Design (6
Clearly describes all classes, attributes, methods, features, expected outputs, and interactions among classes.
Most classes, attributes, methods, and features are described accurately.
Some OOP elements are described but lack detail or accuracy.
OOP design is largely missing or incorrect.
/6
Target Users (2 pts)
Clearly identifies target users and explains their needs.
Identifies target users with some explanation.
Mentions target users but explanation is limited.
Target users are unclear or missing.
/2
Class Diagram (4 pts)
The diagram accurately represents classes, attributes, methods, and relationships described in the proposal.
The diagram is mostly accurate with minor inconsistencies.
The diagram contains several omissions or inaccuracies.
The diagram is missing or does not match the description.
/4
Goals & Objectives (4 pts)
Goals are meaningful and objectives are clear, specific, and aligned with the project.
Goals and objectives are generally clear and aligned.
Goals or objectives lack clarity or alignment.
Goals and objectives are incomplete or missing.
/4




