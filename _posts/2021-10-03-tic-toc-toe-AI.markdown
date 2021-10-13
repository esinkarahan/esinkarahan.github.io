---
layout: archive
title:  "Tic-Tac-Toe with AI"
date:   2021-10-03
categories: jekyll update
author_profile: true
comments: true
classes: wide
---

Keywords: python, minimax algorithm, minimax with alpha beta pruning

In this project, I created tic-tac-toe game with different player strategies by using Python. 

In the first version, two human players are playing against each other. In the second version, opponent is computer and making random legal moves. An improved version makes winning moves if one exists and returns a random move otherwise. The fourth generation player makes a move that wins if possible, a move that block a loss, and a random move otherwise.

Finally, the most advanced version of the opponent is based on minimax algorithm. This algorithm is based on minimizing the maximum outcomes of the opponent. The algorithm works by assigning scores to 2 positions that are terminal and non-terminal states. If a terminal state is a win for the agent, its score is +10, if it is a loss it is -10 and if it is a draw it is 0. In this algorithm, the agent assumes every player plays perfectly and calculates scores all the way down the terminal states and choses the best move. A nice graphical description is from this [article](https://www.freecodecamp.org/news/how-to-make-your-tic-tac-toe-game-unbeatable-by-using-the-minimax-algorithm-9d690bad4b37/).

![minimax](/assets/images/minimax.png) 

I also implemented minimax algorithm with alpha-beta pruning which speeds up the minimax algorithm substantially. 

To play, run `python tictactoe.py` and choose first and second players from the list of players.

`repeated_battle_all.py` compares 4 agents across 50 games. 

Minimax-AI never loses a game against themselves or any other AI!

In this figure, 
* Game 1 is random_ai vs find_winning_moves_ai
* Game 2 is random_ai vs find_winning_and_losing_moves_ai
* Game 3 is random_ai vs minimax_ai
* Game 4 is find_winning_moves_ai vs find_winning_and_losing_moves_ai
* Game 5 is find_winning_moves_ai vs minimax_ai
* Game 6 is find_winning_and_losing_moves_ai vs minimax_ai
 
![Stats](/assets/images/stats_ai_with_minimax.png)

This figure shows when minimax_ai is implemented with pruning.

![Stats](/assets/images/stats_ai_with_pruning.png)

The code is available in [Github](https://github.com/esinkarahan/python_projects/tree/main/tictactoe_ai).


