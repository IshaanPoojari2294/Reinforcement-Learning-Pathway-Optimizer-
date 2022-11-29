# Reinforcement-Learning-Pathway-Optimizer-

# Problem

My project intended to develop Reinforcement learning pathway optimizer algorithms to find the shortest route between two points for an object traveling on a two-dimensional grid, where the object can take 3 steps either forward, left, or right. I wanted to compare the relative efficiencies of various Reinforcement Learning approaches in solving the problem and compare the advantages of each approach.

# Pathway Optimizer - Policy Gradient Approach

The Pathway Optimizer file contains the Policy Gradient approach to the problem, where each action state is fed into a 3-layer neural network, which outputs the model's predicted probabilities for the object to perform each of the 3 possible actions: moving forward, turning left, or turning right. Based on the neural network's output, the model decides on one of the actions.

The model is fed many episodes, where each episode was a new grid with a different start and end point, and each step in the episode was assigned a positive reward if it led to the object reaching the endpoint and was assigned a negative reward if it led to the object failing to reach the endpoint. These rewards will shift the probability weights in the neural network to help train it to take the most optimal decision based on a given input state.

A discount factor is implemented so that steps closer to the end of the path have a greater influence on the weights in the neural net while steps further from the end of the path have a diminished impact on the weight corrections. 


# TF Agent Pathway Optimizer - Deep Q-Learning Approach

The TF Agent Pathway Optimizer file contains the Deep Q-Learning approach which trains a Deep Q-Network using the Tensorflow Agents library. The Deep Q-Learning approach uses a neural network to approximate the Q-function, which uses the Bellman equation to calculate the expected return based on an action state pair input. 

One of the advantages of this approach is the use of a replay buffer, which stores all of the past experiences and randomly selects a training set to train the algorithm. This helps reduce correlations between successive experiences, which improves the efficiency of training.

# Grid Model

The Grid model code is proprietary according to my internship administrators, so I am not able to commit it to this repo publicly. I used Jupyter notebooks to help visualize how the grid model is structured.
![image](https://user-images.githubusercontent.com/114254060/204448927-4710b6f4-8281-4688-9ef4-39bfdba80138.png)

