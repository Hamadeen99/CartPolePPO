# CartPolePPO

## Overview
This project implements a reinforcement learning solution for the CartPole environment using the **Proximal Policy Optimization (PPO)** algorithm. PPO is a powerful on-policy algorithm that ensures stable learning by limiting policy updates with a clipping mechanism.

---

## Features
- **Proximal Policy Optimization (PPO)**:
  - Uses a clipping-based objective function for stable and efficient policy updates.
  - Performs multiple optimization steps per collected batch.
- **Custom Neural Networks**:
  - Includes separate actor and critic networks implemented in PyTorch.
  - Incorporates dropout for regularization.
- **Training and Testing**:
  - Train the agent to balance the pole for extended durations.
  - Evaluate and visualize the agent's performance.
- **Reward Visualization**:
  - Plots training and testing rewards across episodes.
- **Checkpointing**:
  - Saves trained model weights for future use.

---

## Requirements
- PyTorch
- Gymnasium
- Matplotlib
- NumPy

Install requirements using:
```bash
pip install torch gymnasium matplotlib numpy
```


---

## Key Components

### **ActorCritic**
- Combines two networks:
  - **Actor**: Predicts the probability distribution of actions.
  - **Critic**: Estimates the value of states.

### **Network**
- A three-layer fully connected neural network.
- Used as the backbone for both actor and critic.
- Employs dropout for regularization.

### **PPO Algorithm**
- **Clipping Objective**:
  - Limits the change in policy updates to ensure stability.
- **Advantage Estimation**:
  - Guides policy updates by comparing discounted rewards to predicted values.
- **Multiple Steps**:
  - Allows several policy updates per batch of collected trajectories.

---

## Results
1. **Training**:
   - Trained the agent to achieve a mean test reward exceeding the threshold of 400 within ~500 episodes.
2. **Visualization**:
   - Plots training and test rewards over episodes.
   - Highlights the reward threshold.

---

## Repository Structure
```
├── ActorCritic.py          # Defines the Actor-Critic architecture
├── Network.py              # Defines the neural network for actor and critic
├── CartPolePPO.py          # Main script for training and testing
├── checkpoint/             # Directory for storing model checkpoints
├── README.md               # Project documentation
```

---

## Future Enhancements
- Deploy the trained agent on a physical robot using a simulation-to-reality transfer.

---
