Created by Aram Galarza Roca ([@WittIsHere](https://github.com/WittIsHere)) for Project II
Video Game Design and Development, under the supervision of Ramon Santamaría ([@raysan5](https://github.com/raysan5))

# Introduction
Turn based combat (TBC for abbreviation) is how everything started. This simple way of resolving combats, due to hardware limitations, was seen everywhere, especially in RPG games.
Nowadays it may be seen as an outdated combat, only played by nostalgics, but I still think it is one of the most satisfactory and pleasant experiences. Having time to think, developing original strategies and expanding the world. 
The main feature of this combat are the turns, just like chess, where the game flow is partitioned into defined parts. It allows a period of analysis before commiting to a game action. Every choice has to be thought carefully and thoroughly, and any mistake can be fatal.
It is also a battle of resources and knowledge that must be used in the most proper way, in order to achieve victory.

# Index
1. Brief history about RPG TBC
2. Polemic: Turn based combat is boring
3. Some examples and styles of TBC
4. What makes a TBC BAD?
5. What makes a TBC GOOD?
6. Elements of the TBC
7. Loops
8. Designing a simple TBC
9. Case studies
10. Tips

# Early history
The first turn based combat game is Tanktics (1973) by Chris Crawford, a game about tanks and fights, where the player has to choose an objective and then fight it.
But I also would like you to think if Rogue (1971) is also a Turn Based Combat game. Because the flow of the game are turns, or better said, the game doesn't advance until the player does an action, that translates in having the game flow divided in two states (after player action and pause) and those could be considered turns.
After this beginning, many and many games started thriving, using this original combat style in many and unique ways. We have the Final Fantasy games at the end of the 80s, They combined powerful narrative, a party based combat and other improvements. And then, in the 90s, this genre had a boom. We have Chrono Trigger, more and better Final Fantasy games, Pokemon, Light Crusader and hundreds of titles that moved the genre (and of course the combat) to a next level.


# Polemic
Not gonna talk a lot about this subject. But the polemy is here. 
The main two points of view are:
1. Turn based combat is enjoyable. It is an interesting puzzle and since you are not limited by time, you can enjoy a more slow pace. Decisions have real weight, and a mistake can lead to failure. It is easy to learn, and for all publics. 
2. Turn based combat is boring. It is an outdated and therefore obsolete type of combat, it was great in the begining, when games were limited by technology, but no longer enjoyable in the new generations. TBC is a type of combat that must be avoided.

![Poll](https://github.com/WittIsHere/RPG-Turn-Based-Combat/blob/main/docs/images/Poll.PNG?raw=true)

What do you think?

# Examples and types of turn based combat
I have seen three main approaches, all under the category of RPG turn based combat. I am not using the pioneers of these styles, but well-known examples so you all can get the main idea.
Since in this subject we are using the classic, I will only mention the other two here.

### Classic.
Pokemon, Octopath traveler, Final Fantasy (first games), Chrono Trigger and many many others.
I believe that this style has two main variants. Where **positioning** matters or not.

Example: Chrono Trigger

![ChronoTrigger](https://github.com/WittIsHere/RPG-Turn-Based-Combat/blob/main/docs/images/ChronoTrigger.png?raw=true)

Here we can see that the pillars exist. There are turns, attacks, resources, players and parties, and enemies and bosses.
But the initial positioning and approach to the fight will have an impact on the development of it. For example, maybe you have a rogue that gets a bonus if it attacks an enemy from the back. This leads to a new level of mastery, where not only the decisions inside matter, but also proper preparation. There are other examples that will use positioning as an extra layer of complexity.

Second Style, positioning doesn't matter. Example: Sinjid: Shadow of the warrior (Browser game)

![Sinjid](https://github.com/WittIsHere/RPG-Turn-Based-Combat/blob/main/docs/images/Sinjid.png?raw=true)

The battle is like a different space, separated of anything else. Here you only have to focus on the fight. You have to manage carefully your resources, and understand how each battle is supposed to be played.

There exist many variations, but all share the same idea. We will talk about this later.


### Simple and Limited Grid System. Example: Pit People

![PitPeople](https://github.com/WittIsHere/RPG-Turn-Based-Combat/blob/main/docs/images/PitPeople.png?raw=true)


This is a bit more sophisticated. Using a grid system, you also have to think about formations and tactics. Maybe you want the mages and archers in the backline, protected by warriors and tanks. You also have to move your units through the battlefield. But the space is limited, there is a set number of tiles where you can go, and no more. All the necessary information is on the screen. It is usually seen in 2D or 2.5D style, and it is more approachable than the next system.


### Complex Grid System. Example: Xcom 2

![Xcom2](https://github.com/WittIsHere/RPG-Turn-Based-Combat/blob/main/docs/images/Xcom2.png?raw=true)

This one is more complex. It is also grid based, but on a much larger scale. You do not know what is out there, the information that you have is very limited, and you need to advance into an unknown space. Actually the mechanics are very very similar to the style mentioned before, but its complexity is usually much higher. Fights will take a lot of time.

# What makes a turn based combat BAD?
 - Boring
 - You have to grind many and many fights that you know the result even before starting
 - There is always a best choice, no room for taking meaningful decisions or approaches to the combat
 - Animations are long.
 - Lack of variety
 - You always have to do the same strategy
 - Broken attacks

# What makes a turn based combat GOOD?
- Balanced
- Good design
- Meaningful choices
- Rewarding
- Easy to learn. Hard to master
- For all ages
- You have all the time that you want
- It innovates in some way

# Elements
Here we will count and analyze every standard element in a turn based combat. Maybe we will not use all of them, or will create something new. But having them as a basis will probably be useful when making other choices. Like someone said, you need to know the rules first if you want to break any of them.

Lets differentiate between two types: What we see, and what we don't:

**What we see:**
This is the information that we have at all times in the screen. We could consider most of it UI.

 - Player's characters and enemies (entities)
Of course we need those, it is the main visual tool that we have. We can identify the types of enemies, how many etc. And for the allies, which one is currently playing.
 - For each ally, it's current stats (health, mana and usually experience)
Vital information, that lets us know what should we do every turn.
 - Turn bar
Not all games will have one, but it's use has been quite popular. It lets us to determine the order of entities.
 - Options panel
What can you do in your turn? The planel has all the options, and often brings extra information.
 - Some extra information about the enemies (maybe state, or weakness)
Maybe one of them is dazed, or sleeping. Maybe because it is a fire type, you prefer attacking with water...

**What we do not see:**
What else is there?

 - Entities stats (speed, damage, resistances, etc...)
There are many variables that we do not have access in the combat, but that affect it. 
 - Escape chance
You do not know it, it is a risk.
 - For the skills, you will only have the name, but should remember them how they work.
 - Attached items

# Loops
This is another layer of the turn based combat, and especially useful for programmers.

The turn based combat has several loops. Let's see for example Pokemon. 
*(This is not totally accurate, and only a sketch to show the main ideas).*

**External loop.** It is triggered when you encounter a combat.

{

Before the next loop, several events will occur: First, if it is a wild encounter, choose the enemy pokemon from a pool. Second, check which pokemon do you have on the first position, it will be the one fighting first. And third, compare the speed of both pokemon and determine who starts.

**Inner loop**: It will be active while certain conditions are not met: Win, Lose, Escape or Capture the pokemon if wild encounter.

{

In your turn: choose an action to do: Attack, Item, Tun or swap Pokemon.
Enemy turn: Select an action based on the AI intelligence

}

**End of Inner loop** After the battle, give rewards if you won the battle. If you lost send the player to a medical center, etc...

}

**End of External loop.**


# Designing a simple turn based combat.

I divided the creation of a turn based combat into a few steps.

**1 - Understand what role does the combat take into your game. Probably for this assignment it will be one of the game pillars, since its the main challenge that the player will have.**

This is very important, because maybe you prefer fast combats to let the history move forward and don't tire the player too much. Or maybe you want a super complex combat, where the player will spend a lot of time thinking. It is up to you. How do you want the bosses? How challenging? Do you allow the player to farm? 


**2 - Mechanics.**

This is probably the most important step. Because it will set the basis of everything else. You should consider spending a large amount of time in this one.

- What are the core mechanics of the combat?
- How many resources do you play with, only Mana and Health? or maybe you want to introduce more variables to have extra depth? We will see examples of this later.
- Think about the stats of the entities.
- How important are items?
- How can you innovate?
- Do you have classes for you characters? or are they fixed? or dependent on items and skill trees? 
- Do you have a weakness system (such as types in pokemon)?

**3 - Understand the different loops inside the game**
As we saw before, creating the loop is one of the first things you should do, it helps understanding the bigger picture.

**4 - Develop the entities: Playable characters and Enemies (mobs and bosses)**
You have to define how you want the player to approach the challenge, do you have classes? Do you have to form a party?                                                    
Also, what stats do they have, and which ones can the player interact with.                                                                                              
- What attacks do they have?
- Levels and experience
- When you encounter combat, are there determined sets of enemies? (for example, a group of four small mobs. Or a tank and a healer, or 3 dps that focus your mage, etc)
- Create memorable bosses and mobs
- Do you have an rpg Item system? 

There are a lot of possible questions, but you are the only one who will answer them.

**5 - Create the Options That those entities will have available. Attacks, Magic, Consumable items etc...**

This is core. You not only need to create those, but also think about how to balance them.
Between the 4 and 5, it will be a continuous loop until you have a satisfactory system.
The combat should feel satisfying and difficult. 


**6 - Design AI intelligence**

How hard and punishing do you want your enemies to be? 
You should consider things like:
Prioritizing targets, if a player's unit is very low, killing it first, using long term attacks (debuffs, poison...) first, etc...


**7 - Design the UI and the art style**
You should already have a list of the UI and what elements are visible to the player and which not.
Think about the style, will you do detailed animations for the attacks? etc...


# Case studies
### Pokemon

![Pokemon1](https://github.com/WittIsHere/RPG-Turn-Based-Combat/blob/main/docs/images/Pokemon2.png?raw=true)

Pokemon is a very interesting game. I think that the exit of its combat is due to three factors: First, every wild encounter is thrilling, because you might want to capture it. Second, the types system is awesome! It also makes you think about building a party of balanced pokemons. And third, being able to swap between pokemons, it is probably the most rewarding mechanic when mastered, because it has infinite combinations with it.

### Octopath traveler

![Octopath](https://github.com/WittIsHere/RPG-Turn-Based-Combat/blob/main/docs/images/Octopath1.png?raw=true)

Probably already a classic. Not only because its beautiful graphics, but also because of the depth of his world and characters. I find that there have been many interesting choices, and will talk about three of them. First, each character is unique in its own way, and this is seen in the combat, because each character will have a special skill (summon NPCs, capturing enemies...), this leads to variety and more depth when building the party. Second, not being able to see the enemies health or weakness is very tough. You will need to learn it, and that means practice and error. Overextending when the enemy is still in the safe zone can be devastating, or retiring when the opposite. The third factor are the Impulse Points, each turn your characters will gain an extra point, and when using them will empower the next attack, it is a cool mechanic that adds another layer of epicness and complexity to the combat.

### Darkest Dungeon

![Darkest](https://github.com/WittIsHere/RPG-Turn-Based-Combat/blob/main/docs/images/DarkestDungeon.png?raw=true)

I want to mention two variables of this game. First is the stress value. It is a great example of how an idea (making a game as dark and horrific as possible) leads to creating a new mechanic (so, step 1 and 2). Second, the party's movement and positioning. Certain attacks will only be available from certain positions, and those positions also influence the roles (usually tanks and fighters will go first, and supports and dps back).

### Undertale

![Undertale2](https://github.com/WittIsHere/RPG-Turn-Based-Combat/blob/main/docs/images/Undertale2.png?raw=true)

Ah, Undertale. Very unique and charismatic game. I want to analyze two features. First, the introduction of many extra options in the combat. You are not only able to attack, defend, run and use items. But also you can talk with your enemy, or even pet it, or give it a hug, or compliment it. This is super refreshing, and feels very rewarding sometimes.
Second, the Quick time events that happen in the encounters. Usually when an enemy attacks you, one of those quick time events will appear (that is, you in a mini bullet hell). They are divided into two categories. Mobs and Bosses. For mobs you will have to train the basics, and improvise because everything will be randomized. But bosses will usually have a set of patterns, you will not know which one they will use, but you will be able to learn them and adapt, more like a skill puzzle.

# Final Tips

Please, make sure to have at least **one original mechanic.**

There should not always be a best option, this just puts the player into auto-mode, and there is nothing more boring than that.

I really like the term  **Meaningful choices.**

Bosses can be just a hard encounter, or a puzzle.

The game flow should be balanced, not a lot of fights, but also not too few. Keep the player alert, but avoid farming and grinding.

## Extra resources

Presentation.

# Bibliography

*Videos*

[Abstraction and Turn-based Combat](https://www.youtube.com/watch?v=fCPAmwbzylc)

[Turn Based RPG's are Boring](https://www.youtube.com/watch?v=9nOAnY3YYrA)

[Turn-Based Combat Doesn't Suck](https://www.youtube.com/watch?v=5cTNDFxBSdk)

[More Engaging Turn-Based Combat in RPGs](https://www.youtube.com/watch?v=0Rebci_7ABQ)

[Top 10 Innovative Turn Based Battle Systems in RPGs](https://www.youtube.com/watch?v=wQbI_rtYNrk)

*Forums*

[What makes a good turn based combat system?](https://www.reddit.com/r/gamedev/comments/99cnmq/what_makes_a_good_turn_based_combat_system/)

[What are some good ways to make turn-based combat more compelling?](https://www.reddit.com/r/truegaming/comments/ji8m8m/what_are_some_good_ways_to_make_turnbased_combat/)

*Articles:*

[Turn-Based Combat Is The Best Kind Of Combat](https://kotaku.com/turn-based-combat-is-the-best-kind-of-combat-5990831)

[Turn-based strategy](https://en.wikipedia.org/wiki/Turn-based_strategy)

[Redesigning Turn-Based RPGs](https://medium.com/orangeandjuicy/redesigning-turn-based-rpgs-b8577f93a48f)

[12 ways to improve turn-based RPG combat systems](https://www.gamasutra.com/blogs/CraigStern/20130411/190332/12_ways_to_improve_turnbased_RPG_combat_systems.php)



*Thank you very much for your attention!!*


*Witt*

