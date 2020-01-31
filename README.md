# Project 1 - Udacity DRL: Navigation

## Project Details

For this project, I will train an agent to navigate in an environment, that was developed by [Unity]( https://unity3d.com/es) for the Unity Machine Learning Agents Toolkit https://unity3d.ai.

### Environment Description
A reward of +1 is provided for collecting a yellow banana, and a reward of -1 is provided for collecting a blue banana.  Thus, the goal of the agent is to collect as many yellow bananas as possible while avoiding blue bananas.  

The state space has 37 dimensions and contains the agent's velocity, along with ray-based perception of objects around agent's forward direction.  Given this information, the agent has to learn how to best select actions.  Four discrete actions are available, corresponding to:
- **`0`** - move forward.
- **`1`** - move backward.
- **`2`** - turn left.
- **`3`** - turn right.

The task is episodic, and in order to solve the environment, the agent must get an average score of +13 over 100 consecutive episodes.

## Getting Started

For this project, you are going to need some basic libraries like _numpy_ and _matplotlib_. For the neural network of the agent, we are going to use PyTorch. In order to be able to interact with the Unity Toolkit we have to install the following version of torch and torchvision.

* __torch=0.4.0__
* __torchvision=0.2.1__

You can see instructions for installation these old libraries directly on the PyTorch [website](https://pytorch.org/get-started/previous-versions/)

### Download the environment

1. You can download the environment from one of the links below.  You need only select the environment that matches your operating system:
    - Linux: [click here](https://s3-us-west-1.amazonaws.com/udacity-drlnd/P1/Banana/Banana_Linux.zip)
    - Mac OSX: [click here](https://s3-us-west-1.amazonaws.com/udacity-drlnd/P1/Banana/Banana.app.zip)
    - Windows (32-bit): [click here](https://s3-us-west-1.amazonaws.com/udacity-drlnd/P1/Banana/Banana_Windows_x86.zip)
    - Windows (64-bit): [click here](https://s3-us-west-1.amazonaws.com/udacity-drlnd/P1/Banana/Banana_Windows_x86_64.zip)
    
2. Place the file in the `root/` folder of the project, and unzip (or decompress) the file.


## Instructions

This repository contains the following scripts
- __dqn_agent.py__
    - This script manages the internal variables of the agent as well as the training phase. The Q-Network is located here and all the interaction with the environment. It also manages the replay memory buffer.
- __model.py__
    - Here is where the architecture of the model is initialized. 
- __environment.py__
    - It is a simplified script to interact with the Unity environment. It has two main methods:
        - __reset:__ resets the environment and returns the state of the env.
        - __execute:__ receives an action and returns the next state, the reward and a bool value indicating if the env is in a termnal state.
- __train_agent.ipynb__
    - This script allows you to see step by step the training phase.

Open the __train_agent.ipynb__ and execute the cells to see how to interact with the environment. After you will have the opportunity to see an untrained agent acting. Finally, you will train the agent.