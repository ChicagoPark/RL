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

<img width="450" alt="IMG" src="https://user-images.githubusercontent.com/73331241/158747811-1898ac27-5b67-4a52-807c-d0e1d39dcab2.PNG">

* Agent: Decision Maker by interacting with the environment sequentially over time.
  * Agent goal in MDP: Maximize the expected culmulative rewards based on the policy.
* Environment: According to the MDP model, it decides the next state(s') and reward(r).
* State: Represent the situation from environment
* Action: Based on the policy
* Reward: Get from corresponding action about the state

### Probability to be next state and reward

### [1-1] Episodic VS Continuing Tasks

* Episodic Tasks: Each new round of the game can be thought of as an episode, and the final time step of an episode occurs when a player scores a point.
  * The next episode then begins independently from how the previous episode ended.

  * [Cumulative Reward: G - Episodic]

    <img width="450" alt="IMG" src="https://user-images.githubusercontent.com/73331241/158753554-dcc2f7f1-fbeb-4382-8c46-a09539c9f5da.PNG">

*  Continuing Tasks: There is no limit. That's why it needs Discount Variable

    * [Cumulative Reward: G - Continuing]

     <img width="450" alt="IMG" src="https://user-images.githubusercontent.com/73331241/158753558-03ea5572-6a5e-4528-b02f-78c7f38d8310.PNG">

### [1-2] Policies and Value Functions

* Policy: what is the `probability` that an agent will select a specific action from a specific state

* Value: how good a given action or a given state is for the agent

value function: 1. generates expected return / 2. suggests the background that agent consider to act / 3. Policy

State-value function: v(s)

Action-value function: q(s, a) # q means "QUALITY". It is the same notation from Q-table. We can understand it to estimate the quality of (state, action)

Optimal action-value function: q*(s, a) # find the maximum value from all the policies in the state.


## 4. Exploration VS Exploitation
[epsilon greedy strategy]: epsilon means rate for exploration
when epsilon is near 0: exploitation
when epsilon is near 1: exploration

## 5. Deep Q-learning

<img width="450" alt="IMG" src="https://user-images.githubusercontent.com/73331241/158344207-2813e827-77bc-480e-897e-3bf773a88f95.jpeg">

Image can be the representation of state, but it could be difficult to recognize the situation easily. That's why most cases we put image sequence as an input.

There are output nodes as much as possible actions from the state.

Experience replay: At time t, the agent's experience et is defined as this tuple

<img width="450" alt="IMG" src="https://user-images.githubusercontent.com/73331241/158344957-e8d958b4-5ebf-414b-9de8-8e11c89a8324.PNG">

Two Types of Neural Network: 1. Policy Network(get s as an input) 2. Target Network(get s' as an input)

replay memory



<!--
Blog Spot: https://deeplizard.com/learn/video/nyjbcRQ-uQ8

next lecture(written 3/14): Exploration vs. Exploitation - Learning the Optimal Reinforcement Learning Policy(https://www.youtube.com/watch?v=mo96Nqlo1L8&list=PLZbbT5o_s2xoWNVdDudn51XM8lOuZ_Njv&index=7)

study material
0. beginner: https://www.youtube.com/watch?v=nyjbcRQ-uQ8

1. intuition: Reinforcement Learning Series by YouTuber deeplizard.

2. Handson: https://www.youtube.com/watch?v=NP8pXZdU-5U&list=PLZeihsNsdQdRdhni8U5KIdxsRIicW498s&index=1

3. RL for trading: https://www.youtube.com/watch?v=3Kqy7HIJiiY&list=PLRoQmvSf6MgwTuiZ8BDVCf8GBQ_Szt6Ci&index=1
-->
