Be sure to install numpy, pytorch, and tensorboardX before running.
Due to the short time, we can only submit the compressed file version first, and then we will try to update it.

The structure of the project is as follows:

--run.py\
 \# Main program entry of this project, sample running method:

            $python3 run.py --p1 human --p2 alphabeta --d 1 --n 10 --show True

            --d is the search depth of alpha-bet-prunning,--n is the number of rounds of the game, --show represents whether the game screen is displayed.
            # make the human player compete with the agent implemented by alpha-beta-prunning

--agents\
 \# This directory contains all implemented agents

----**init**.py\
 \# init

----agent.py\
 \# The agent base class, all subclasses of agent should implement
choose\_action function \# This function accepts a game-type parameter
representing the current state of the Game, and then returns an action
(that is, the drop coordinates in chess)

----alpha\_beta.py\
 \# Minimax + alpha-beta-prunning + heuristic implemented by an agent

----dqn.py\
 \# DQN implements agent, but does not converge during training

----human\_player.py\
 \# An agent implemented for human players whose choose\_action function
takes the action of the drop from the mouse position of the chessboard

----random\_agent.py\
 \# A completely random agent that randomly selects a return action from
the idle coordinates of the checkerboard

--env\
 \# This directory contains the implementation of the game base
environment

----**init**py\
 \# init

----graphics.py\
 \# is a small GUI library cite form
https://github.com/colingogogo/gobang\_AI/blob/master/graphics.py

----game.py\
 \# Gobang basic game environment implementation

----environment.py\
 \# The game environment used to train DQN, in which the GoBangEnv class
inherits from GoBangGame in game.py

--experience\_replay.py \# A simple experience playback pool
implementation can refer to the instructions in the original DQN paper

--network.py\
 \# Based on the DQN network realized by PyTorch, the network
architecture is consistent with the original paper of DQN (Nature 2015)

--train\_dqn.py\
 \# Training code for DQN
