Created by Aram Galarza Roca ([@WittIsHere](https://github.com/WittIsHere)) for Project II
Video Game Design and Development, under the supervisition of Ramon Santamaría ([@raysan5](https://github.com/raysan5))

# Introduction
Turn based combat (TBC for abreviature) is how everything started. This simple way of resolving combats, due to hardware limtations, was seen everywhere, specially in RPG games.
Nowdays it may be seen as an outdated combat, only played by nostalgics, but I still think it is one of the most satisfactory and pleasant experiences. Having time to think, developing original strategies and expanding the world. 
The main plar of this combat are the turns, just like chess, where the fame flow is partitioned into defined parts. it allows a period of analysis before commiting to a game action. Every choice has to be thought carefully and thoroughtly, and any mistake can be fatal.
It is also a battle of resources and knowledge, that must be used in the most proper way, in order to achieve victory.

# Index
1. Brief history about RPOG TBC
2. Polemic: Turn based combat is boring
3. Some examples and kinds of TBC
4. What makes a TBC BAD?
5. What makes a TBC GOOD?
6. Elements of the TBC
   - UI 
   - Elements
7. Loops
8. Designing a simple TBC
9. Case studies
10. Tips

# Early history
The first turn based combat game is Tanktics (1973) by Chris Crawford a game about tanks and fights, where the played had to choose an objective and then fight it.
But I also would like you to think if Rogue (1971) is also a Turn Based Combat game. BEcause the flow of the game are turns, or better said, the game doesn't advance until the player does an action, that translates in having the game flow divided intosegments (after player action and pause) and those could be considered turns.
After this beginning, many and many games started thriving, using this original combat style in many and unique ways. We have the Final Fantasy games at the end of the 80s. And then, in the 90s, this genre had a boom. We have Chrono Trigger, more and better Final Fantasy games, Pokemon, Light Crusader and hundreds of titles, that moved the genre (and of course the combat) to a next level.


# Polemic
Not gonna talk a lot about this subject. But the polemy is here. 
The main two points of view are:
1. Turn based combat is enjoyable. It is an interesting puzzle and since you are not limited by time, you can enjoy a more slow pace. Decisions have real combat, and a mistake can lead to failure. It is easy to learn, and for all publics. 
2. Turn based combat is boring. It is an outdated and therefore obsolete type of combat, it was great in the beggining, when games where limited by technology, but no longer enjoyable in the new generations. TBC is a type of combat that must be avoided.
3. 
![Poll](https://github.com/WittIsHere/RPG-Turn-Based-Combat/blob/main/docs/images/Poll.png?raw=true)

What do you think?

# Examples and types of turn based combat
I have seen three main approaches, all under the category of RPG turn based combat. I am not using the pioneers of these styles, but well-known examples so you all can get the main idea.
Since in this subject we are using the classic, I will only mention the other two here.

### Classic.
Pokemon, Octopath traveler, Final Fantasy (first games), Chrono Trigger and many many others.
I believe that this style has to main variants. Where **positioning** matters or not.

Example: Chrono Trigger
![ChronoTrigger](https://github.com/WittIsHere/RPG-Turn-Based-Combat/blob/main/docs/images/ChronoTrigger.png?raw=true)
Here we can see that the pilars exist. There are turns, attacks, resources, players and parties, and enemies and bosses.
But The initial positioning and approach to the fight will have impact of the fight. For example, maybe you have a rogue that gets a bonus if it attacks an enemy from the back. this leads to a new level of mastery, where not only the ecisions inside matter, but also a proper preparation.

Second Style, positioning doesn't matter. Example: Sinjid: Shadow of the warrior (Browser game)
![Sinjid](https://github.com/WittIsHere/RPG-Turn-Based-Combat/blob/main/docs/images/Sinjid.png?raw=true)

The battle is like a different space, spearated of anything else. Here you only have to focus on the fight.


There exist many variations, but all share the same idea. We will talk about this later.


### Simple and Limited Grid System. Example: Pit People
![PitPeople](https://github.com/WittIsHere/RPG-Turn-Based-Combat/blob/main/docs/images/PitPeople.png?raw=true)


This is a bit more sofisticated. Using a grid system, you also have to hiunk about formations and tactics. Maybe you want the mages and archers in the backline, protected by warriors and tanks. You also have to move your units throguh the battlefield. But the space is limited, there is a set number of tiles where you can go, and no more. All the necessary information i on the screen. It is usually seen in 2D or 2.5D style, and it is more approachable than the next system.


### Complex Grid System. Example: Xcom
![Xcom2](https://github.com/WittIsHere/RPG-Turn-Based-Combat/blob/main/docs/images/Xcom2.png?raw=true)

This one is more complex. It is also grid based, but in a much larger scale. You do not know what is out there, the information that you have is very lmited, and you need to advance into an unknown space. Actually the mechanics are very very similar to the style mentioned before, but its complexity is usually much higher. Fights will take a lot of time.

# What makes a turn based combat BAD?
 - Boring
 - You have to grind many and many fights that you know the result even before starting
 - There is always a best choice, no room for taking meaningful decisions or approaches to the combat
 - Animations are long.
 - Lack of variety
 - You always have to do the same strategy
 - Broken attacks

# What makes a turn based combat GOOD?
- There is a phylosophy why this game has this type of combat. There is a reason why it is the best option for the game
- Balanced
- Good design
- Meaningful choices
- Rewarding
- Easy to learn. Hard to master
- For all ages
- You have all the time that you want
- It innovates in some way

# Elements
First, I would like to talk about a dichotomy. We will first analyze the elements that we see (all that is related with the graphics and the UI)
And then, about the hidden elements
I will just mention and explain them briefly here, when designing our game we will learn how to use them.

### UI
- Turn's bar
- Entities (Players and enemies)
- Options menu
- Stats of the characters (HP, Mana...)

### Hidden
All that is related to the fight, but that is under the knowledge of the player. It can be prepared in advance (like what attacks, or what party are you using) or you will have to discover it yourself (monster attacks, weakness, stats, how to approach the fight...)

- Entities stats (not HP and MP, but damage, dodge, speed, weakness, types of attacks...)
- How is it supposed to play? Do you have different strategies?


# Loops
This is another layer to the combat, and specially usefull for programmers.

The turn based combat has several loops. Let's see for example Pokemon. (This is not totally accurate, and only an sketch to show the main ideas).

External Loop. It is triggered when you encounter a combat.
{
Before the next loop, several events will occur: First, if it is a wild encounter, choose a pokemon from a pool. Second, check which pokemon do you have on the first position, it will be the one fighting first. And third, compare the speed of both pokemon and determine who starts.

Second Loop **Combat loop**: It will be active while certain conditions are not meet: Win, Lose, Escape or Capture the pokemon if wild encounter.
{
In your turn: choose an action to do: Attack, Item, Tun or swap Pokemon.
Enemy turn: Select an action based on the AI intelligence
}
After the battle, give rewards if you won the battle. If you lost send the player to a medical center, etc...
}
End of External Loop. 


# Designing a simple turn based combat.

I divided the creation of a turn based combat into a few steps
This is a draft, but you will find more detailed explanation in the adjunct pdf.

**1 - Understand what rol does the combat take into your game. Probably for this asignment it will be one of the game pilars, since its the main challenge that the player will have.**

This is very important, because maybe you prefer fast combats to let the history move foward and don't tire the player too much. Or maybe you want a super complex combat, where the player will spend a lot of time thinking. It is up to you.


**2 - Mechanics.**

This is probably the most important step. BEcause it will set the basis of everything else. You should consider spending a large amount of time in this one.

What are the pilars of the combat?
How many resources do you play with, only Mana and Health? or maybe you want to introduce more variables to have extra depth? We will see examples of this later.
Think about the stats of the entities.
How important are items?
How can you innovate?
Do you have classes for you characters? or ae they fixed? or dependent on items and skill trees? 
Do you have a weakness sytem (such as types in pokemon)?

**3 - Understand the different loops inside the game**
As we saw before, creating the loop is one of the first things you should do, it helps understanding the bigger picture.

**4 - Develop the entities: Playable characters and Enemies (mobs and bosses)**
You have to define how do you want the player to approach the challenge, do you have classes? do you have to form a party?
Also, what stats o they have, and wich ones can the player interact with.
What attacks do they have?
Levels and experience
When you encounter a combat, are determined sets of enemies? (for example, a group of four small mobs. Or a tank and a healer, or 3 dps that focus your mage, etc)

**5 - Create the Options That those entities will have available. Attacks, Magic, Consumable items etc...**

This is core. You not only need to create those, but also think about how to balance them.
Between the 4 and 5, it will be a continuous loop until you have a satisfactory system.
The combat should feel satisfying and difficult. 


**6 - Design AI intelligence**

How hard and punishing do you want your enemies to be? 
You should consider things like:
Prioritizing targets, if a player's unit is very low, killing it first, using long term attacks (ebuffs, poison...) first, etc...


**7 - Design the UI and the art style**
You should already have a list of the UI and what elements are visible to the player and wich not.
Think about the style, will you do detailed animations for the attacks? etc...


# Case studies
### Pokemon
![Pokemon1](https://github.com/WittIsHere/RPG-Turn-Based-Combat/blob/main/docs/images/Pokemon2.png?raw=true)

Pokemon Is a very interesting game. I think that the exit of its combat is due fo three factors: First, every wild encounter is thrilling, because you might want to capture him. Second, the types system is awesome! It also makes you think about building a party of balanced pokemons. And third, being able to swap between pokemons, it is probably the most rewarding mechanic when mastered, because it has infinite combinations with it.

### Octopath traveler
![Octopath](https://github.com/WittIsHere/RPG-Turn-Based-Combat/blob/main/docs/images/Octopath1.png?raw=true)

Probably already a classic. Not only because its beautiful graphics, but also because the depth of his world and characters. I find that there has been many interesting choces, and will talk about thee of them. First, each character is unique in its own way, and this is seen in the combat, because each character will have an special combat, only avaulabee to him (summon NPCs, capturing enemies...), this leads to variety and more depth when bulding the party. Second, not being able to see the enemies health or weakness is very thought. You will need to learn it, and that means practice and error. Overextending when the enemy is still in safe zone can be devastating, or retiring when the opposite. The third factor are the Impulse Points, each turn your characters will gain an extra point, and when using them those will empower the next attack, it is a cool mechanic that adds another layer of epicness and complexity to the combat.

### Darkest Dungeon
![Darkest](https://github.com/WittIsHere/RPG-Turn-Based-Combat/blob/main/docs/images/DarkestDungeon.png?raw=true)

I want to mention two variables of this game. First is STRESS. It is a great example of how an idea (making a game as dark and horrorific as possible) leads to creating a new mechanic (so, step 1 and 2). Second, the pary's movement and positioning. Certain attacks will only be available from certain positions, and those positions also influence the roles (ususally tanks and fighters will go first, and supports and dps back).

### Undertale
![Undertale2](https://github.com/WittIsHere/RPG-Turn-Based-Combat/blob/main/docs/images/Undertale2.png?raw=true)

Ah, Undertale. Very unique and carismatic game. I want to analyze two thing. First, the introduction of many extra options in the combat. You are not only able to attack, efent, trun and use item. But also you can talk with your enemy, or even pet it, or give it a hug, or compliment it. This is super refreshing, and feels very rewarding sometimes.
Second, the Quick time events that happen in the encunters. Usually when an enemy attacks you, one of thosequick time events will apear (that is you in a mini bullet hell). They are divided into two categories. Mobs and Bosses. For mobs you will have to train the basics, and improvise because everything will be randomized.  But bosses will usually have a set of patters, you will not know wich one they will use, but you will be able to learn them and adapt.

# Final Tips

Please, make sure to have at least **one original mechanic.**
There should not be always a best option, this just puts the player into auto-mode, and there is nothing more boring thant that. I Really like the term  **Meaningful choices.**
Bosses can be just a hard encounter, or a puzzle.
The game flow should be balanced, not a lot of fights, but also not too few. Keep the player alert, but avoid farming and grinding.


## Extra resources

Presentation.

Downloable helper.

# Bibliography

Videos

[Abstraction and Turn-based Combat](https://www.youtube.com/watch?v=fCPAmwbzylc)

[Turn Based RPG's are Boring](https://www.youtube.com/watch?v=9nOAnY3YYrA)

[Turn-Based Combat Doesn't Suck](https://www.youtube.com/watch?v=5cTNDFxBSdk)

[More Engaging Turn-Based Combat in RPGs](https://www.youtube.com/watch?v=0Rebci_7ABQ)

[Top 10 Innovative Turn Based Battle Systems in RPGs](https://www.youtube.com/watch?v=wQbI_rtYNrk)

Forums

[What makes a good turn based combat system?](https://www.reddit.com/r/gamedev/comments/99cnmq/what_makes_a_good_turn_based_combat_system/)

[What are some good ways to make turn-based combat more compelling?](https://www.reddit.com/r/truegaming/comments/ji8m8m/what_are_some_good_ways_to_make_turnbased_combat/)

Articles:

[Turn-Based Combat Is The Best Kind Of Combat](https://kotaku.com/turn-based-combat-is-the-best-kind-of-combat-5990831)

[Turn-based strategy](https://en.wikipedia.org/wiki/Turn-based_strategy)

[Redesigning Turn-Based RPGs](https://medium.com/orangeandjuicy/redesigning-turn-based-rpgs-b8577f93a48f)

[12 ways to improve turn-based RPG combat systems](https://www.gamasutra.com/blogs/CraigStern/20130411/190332/12_ways_to_improve_turnbased_RPG_combat_systems.php)



*Thank you very much for your attention!!*

*Witt*

