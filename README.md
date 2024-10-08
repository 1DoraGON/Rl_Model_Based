﻿# Model-Based vs. Model-Free Reinforcement Learning on MuJoCo Environments

## Overview
This repository contains the implementation and analysis of a project comparing Model-Based and Model-Free Reinforcement Learning (RL) approaches using various MuJoCo environments. The project focuses on exploring the fundamental differences, benefits, and trade-offs between these two approaches within the context of simulated environments.

## Environments Used
- Walker2d
- Hopper
- Humanoid
- HumanoidStandup
- InvertedDoublePendulum

## Key Features
- **Model-Based RL**:
  - Planning and predicting outcomes before taking actions.
  - Efficient data usage by simulating interactions with the environment.
  - Suitable for static or predictable environments.

- **Model-Free RL**:
  - Learning through trial-and-error.
  - Better suited for dynamic and uncertain environments.
  - Directly learns from interactions with the environment without building an internal model.

## Approach
1. **Data Collection**:
   - Random actions and trajectories were generated in MuJoCo environments, logging states, actions, rewards, and subsequent states.
   
2. **Model-Based Approach**:
   - A neural network was used to predict the next state, expected reward, and trajectory completion.
   - Losses were computed using mean squared error and binary cross-entropy, with the model optimized via gradient descent.
   
3. **Actor-Critic A2C Policy**:
   - Implemented an Actor-Critic A2C policy to train the agent using a combination of policy gradient methods and value function estimation.

## Results
- The project demonstrated that Model-Based RL is more sample-efficient and can perform better in environments where planning and simulation are feasible.
- Model-Free RL proved to be more adaptable to dynamic environments but required more data to achieve comparable performance.

## Dependencies
- Python 3.x
- PyTorch
- MuJoCo Physics Engine

## Installation
Clone the repository:
```bash
git clone https://github.com/1DoraGON/Rl_Model_Based.git
cd Rl_Model_Based
```
