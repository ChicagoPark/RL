# Reinforcement_Learning
reinforcement_learning, deep learning, rl, deepmind 

# Contents
```bash
1. Markov Decision Processes (MDPs)
2. Policies and Value Functions
3. Q-Learning
4. Exploration VS Exploitation
5. Deep Q-Learning
```
## 1. Markov Decision Processes (MDPs)
agent: Maximize the cumulative reward

value function: 1. generates expected return / 2. suggests the background that agent consider to act / 3. Policy

State-value function: v(s)

Action-value function: q(s, a) # q means "QUALITY". It is the same notation from Q-table. We can understand it to estimate the quality of (state, action)

Optimal action-value function: q*(s, a) # find the maximum value from all the policies in the state.


## 4. Exploration VS Exploitation
[epsilon greedy strategy]: epsilon means rate for exploration
when epsilon is near 0: exploitation
when epsilon is near 1: exploration

## 5. Deep Q-learning


![3 DQN-edited](https://user-images.githubusercontent.com/73331241/158344207-2813e827-77bc-480e-897e-3bf773a88f95.jpeg)

Image can be the representation of state, but it could be difficult to recognize the situation easily. That's why most cases we put image sequence as an input.

There are output nodes as much as possible actions from the state.

Experience replay: At time t, the agent's experience et is defined as this tuple
![4  Experience Replay](https://user-images.githubusercontent.com/73331241/158344957-e8d958b4-5ebf-414b-9de8-8e11c89a8324.PNG)

Two Types of Neural Network: 1. Policy Network(get s as an input) 2. Target Network(get s' as an input)

replay memory



<!--
next lecture(written 3/14): Exploration vs. Exploitation - Learning the Optimal Reinforcement Learning Policy(https://www.youtube.com/watch?v=mo96Nqlo1L8&list=PLZbbT5o_s2xoWNVdDudn51XM8lOuZ_Njv&index=7)

study material
0. beginner: https://www.youtube.com/watch?v=nyjbcRQ-uQ8

1. intuition: Reinforcement Learning Series by YouTuber deeplizard.

2. Handson: https://www.youtube.com/watch?v=NP8pXZdU-5U&list=PLZeihsNsdQdRdhni8U5KIdxsRIicW498s&index=1
-->
