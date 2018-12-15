# multi_agent_rl
multi agent deep RL


## System Dependencies

python 3.6+
torch 0.4.1
unityagents 0.4.0

The linux version of the environment can be found in this repo (Tennis_Linux folder)

## Project Details

The goal is to train two agents to play tennis with each other. Each agent controls a paddle, which is used to hit the ball over the net.

The agents are given a reward of 0.1 if the hit the ball over the net. if the agent lets the ball hit the ground or go out of bounds, it gets a reward of -0.01. This reward function incentivizes the agents to keep the ball in play for as long as possible. The environment space contains information about the position of the ball and the each racket. There are two actions available to the agent (continuous values), that correspond to movement of the paddle, and direction (up or down).

The environment is considered solved when the max score (over both agents) is greater than 0.5 for the past 100 episodes. 

## Running the Code
The code is compiled in the report.ipynb file. The model and agent architecture are stored in python files (model.py and ddpg_multiagent.py). 

The network is imported in the ddpg agent script, and the ddpg agent is imported in the unity environment in the report.ipynb file. The code to step the agent through the environment is found in the ipynbs. 

The solved model weights are saved in the repo as checkpoint_actor.pth and checkpoint_critic.pth.  