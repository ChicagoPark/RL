# Reinforcement_Learning
reinforcement_learning, deep learning, rl, deepmind 

# Contents
```bash
1. Markov Decision Processes (MDPs)
2. Policies and Value Functions
3. Optimality
4. Q-Learning
5. Exploration VS Exploitation
6. Deep Q-Learning
```
## 1. Markov Decision Processes (MDPs)

<img width="450" alt="IMG" src="https://user-images.githubusercontent.com/73331241/158747811-1898ac27-5b67-4a52-807c-d0e1d39dcab2.PNG">

* Agent: Decision Maker interacting with the environment sequentially over time.
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

    <img width="290" alt="IMG" src="https://user-images.githubusercontent.com/73331241/158753554-dcc2f7f1-fbeb-4382-8c46-a09539c9f5da.PNG">

*  Continuing Tasks: There is no limit. That's why it needs Discount Variable

    * [Cumulative Reward: G - Continuing]

      <img width="290" alt="IMG" src="https://user-images.githubusercontent.com/73331241/158753558-03ea5572-6a5e-4528-b02f-78c7f38d8310.PNG">

## [2] Policies and Value Functions

* Policy: a function that maps a given state to probabilities of selecting each possible action from that state. We will use the symbol `π` to denote a policy.
  * Policy Background: How probable is it for an agent to select any action from a given state?
  
     <img width="450" alt="IMG" src="https://user-images.githubusercontent.com/73331241/158756151-13b03c32-9632-41e2-8d4e-77e2dd8f69a7.PNG">


* Value Functions: Value functions are `functions of states`, or of `state-action pairs`, that estimate how good it is for an agent to be in a given state, or how good it is for the agent to perform a given action in a given state.

  * Value Functions Background: How good a given action or a given state is for the agent?
  * `Since the way an agent acts is influenced by the policy it's following, then we can see that value functions are defined with respect to policies.`

  ### [2-1] State-Value Function

  <img width="550" alt="IMG" src="https://user-images.githubusercontent.com/73331241/158764669-0326af5a-a8bf-4bb4-9f19-79bdad1f5b9d.png">

  
  ### [2-2] Action-Value Function

  <img width="550" alt="IMG" src="https://user-images.githubusercontent.com/73331241/158764704-52ab3fbf-9acb-4be4-b5a2-c65f7092db9f.png">

## [3] Optimality

> It is the goal of reinforcement learning algorithms to find a policy that will yield a lot of rewards for the agent if the agent indeed follows that policy. Specifically, reinforcement learning algorithms seek to find a policy that will yield more return to the agent than all other policies.

  ### [3-1] Optimal Policy
  
  <img width="550" alt="IMG" src="https://user-images.githubusercontent.com/73331241/158766715-2ec7b6a0-0eae-4046-8955-a01b29b195c0.PNG">
  
  ### [3-2] Optimal State-Value Function
  
  <img width="550" alt="IMG" src="https://user-images.githubusercontent.com/73331241/158766725-929b3981-2107-4936-8b28-157dde36de0a.PNG">
  
  ### [3-3] Optimal Action-Value Function

  <img width="550" alt="IMG" src="https://user-images.githubusercontent.com/73331241/158766745-27380551-383f-45ce-b16a-d2b758c23acd.PNG">
  
  ### `[3-4] Bellman Optimality Equation`

  <img width="550" alt="IMG" src="https://user-images.githubusercontent.com/73331241/158766756-1556a306-cc26-4c89-9473-ceaa0b54d49a.PNG">
  
  <img width="550" alt="IMG" src="https://user-images.githubusercontent.com/73331241/158768714-bd580855-e0bc-46d8-b005-15f0759646d0.PNG">
 
 `once we have our optimal Q-function q* we can determine the optimal policy by applying a reinforcement learning algorithm to find the action that maximizes q* for each state.`
 
 
## [4] Q-learning
> * What is Q-learning?
>   * Q-learning is to find the optimal policy by learning the optimal Q-values for each state-action pair `in a Markov Decision Process`.

```bash
Chicago's guess in Q-learning flow: Overall policy -> Q-learning -> Find the optimal policy
```

### [4-1] Value Iteration
> The `Q-learning algorithm iteratively updates the Q-values` for each state-action pair `using the Bellman equation` `until the Q-function converges` to the `optimal Q-function, q*`. This approach is called value iteration. To see exactly how this happens, let's set up an example, appropriately called The Lizard Game.



## -4. Exploration VS Exploitation
[epsilon greedy strategy]: epsilon means rate for exploration
when epsilon is near 0: exploitation
when epsilon is near 1: exploration

## -5. Deep Q-learning

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
