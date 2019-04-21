# Continuous Control
- My learning algorithm is a Deep Deterministic Policy Gradient.
- DDPG is an actor-critic algorithm and primarily uses two neural networks.
- DDPG uses a stochastic(OUNoise) behavioral policy for good exploration and a deterministic target policy for estimating.
- The critic's output is simply the estimated Q-value of the current state and the action given by the actor. The critic network is updated from the gradients obtained from the TD error signal.
- In my implementation the Actor network contains two hidden layers of (400,300) units with ReLU activation applied to both layers and a tanh on the end.
- In addition, a batch normalization is applied to the input and between the hidden layers.
- The Critical network also has two hidden layers with (400,300) units and ReLU Activation on both layers.
## Hyperparameters

|Parameter|value|
| --|--|
replay buffer size|100000
minibatch size|128
discount factor|0.99
learning rate of the actor |0.0001
learning rate of the critic |0.001

## Rewards of episodes
![](https://github.com/ShamCondor/double-jointed_arm_continuous/blob/master/image/Rewards.png)

## Future Work
Trying other algorithms like PPO, A3C or D4PG
