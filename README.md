# Minesweeper-ai
Minebuster algorithm that picks the most optimal tile to sweep. Compile Runner.py to run the game

## Logic
This algorithm relies on a knowledge base full of sentences. Each sentence contains data about a set of tiles and a count of how many of those tiles are mines. Each time a tile is clicked, the knowledge base is updated with a sentence about its surrounding tiles. Whenever a sentence has a count of 0, we know that all of its tiles are safe. Whenever any sentence has a count equal to the length of its set of tiles, we know all of the tiles are mines. Each time we can deduce if any tiles are mines or safe, sentences in the knowledge base are updated if they share these tiles. The ai picks from a list of safe mines and only picks at random when this list is empty. We may also combined sentences to create new sentences. IF we have 2 sentences where one the set if tiles in sentence 1 is a subset of the tiles in sentence 2, we may create a new sentence where new_set= set2- set1, and new_count= count2 - count1.

## Template
This was an assignment in which I built upon a template from the Harvard CS50 online course. It can be found at https://cs50.harvard.edu/ai/2020/projects/1/minesweeper/ 

![Minesweeper](https://github.com/chenalan02/Minesweeper-ai-Harvard-cs50ai/blob/master/Minesweeper.JPG)
![Minesweeper Start Screen](https://github.com/chenalan02/Minesweeper-ai-Harvard-cs50ai/blob/master/Minesweeper%20start%20screen.JPG)
