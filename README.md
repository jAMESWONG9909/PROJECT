# PROJECT
Introduction:
Ionia is an one-player adventure game(AVG) based on a fusion of the theme of typical Japanese brave adventure light novels and the playing method of Dungeons & Dragons (DND) background.We make reference to some books and novels for designing characters . Technically, the game runs as a linear narrative text adventure game with randomly generated events.
Game rules:
You were reincarnated as a warrior in Another world called  Ionia, and the people of the village saw you as the savior of the evil Lord.Embark on the journey! Read the following instructions before choosing any of the path in front of you:

*only one player can enter Ionia in each game,each game you have 2 lives, meaning that the second death implies game over
*start from the beginning or the last saved session
*Your adventure will start in a main route event, followed by a random event. This pattern will run through the whole process unless a random event generates another random event. Eventually you will end up with the battle with the demon lord, which is the last main route event.
*use keyboard to control your decision (select a/b/c/d by typing the characters a,b,c, or d), so that your story can proceed
*your selection of a,b,c or d will determine the chance of winning, or game over
*The game is saved in data.txt. The game checks if it has the past save when running the game. If you're entering a game for the first time,data.txt will be made to record the game.Otherwise, the game will continue from the last checkpoint.


How to win:
You have fulfilled at least two of the conditions 1~3 (should be confidential to player)::
1.main route part:
	*Companion:you succeed to have magician/knight as companion from several Heros system provided;
*Armor:you succeed to get Heimerdinger’s appreciation and equipped by Hextech Armor;
2. random events part:
	*sacred sword;
*sacred potion;
3. hidden quest (choose math course in the Ionia Academy)
*the recognition of the sacred dragon (successfully answer two questions about calculus)

Features plan to implement:
-Pictures related to the random events by inserting a library <graphics.h>



Coding requirements 1 to 5:
1.Generation of random game sets or events

We use rand() function in the library #<cstdlib> for generating random numbers. 
In addition, to confirm it is nearly a random number, we #include <ctime> . To initialize the random seed, the srand(time(NULL)) function is used.

2. Data structures for storing game status
This game is operated by a,b,c,d on the keyboard. So there is a data structure whose members are characters. Each letter(character) in a,b,c,d corresponds to a command line.

3. Dynamic memory management
The game uses classes to store and access the game status of the player, ie, the number of lives, items currently have, names of companions. Also, we will use vectors to store the events encountered in a game set.


4. File input/output (e.g., for loading/saving game status)
We use the file stream module to get it. Include the library #<fstream>,open the file “data.txt” appended by “ios::app. The choices in the game will be recorded to the archive using the >> and << operators.The command line file.close() executes when the player exits this game. 

5.Program codes in multiple files
Since the game is made up of events and this is a group project, we can split the task into different files for work distribution in terms of events.
