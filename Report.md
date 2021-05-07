# Report on description of implementation

## Learning Algorithm
DDPG algorithm is employed to solve the environment. The algorithm was customized to work with 2 agents, namely the 2 players. Both players are thereby modeled as instances of the class `Agent`. While they have seperate actors implemented as instance variables, they share the same critic and replay buffer implemented as class variables.

#### Chosen hyperparameters
* replay buffer size: 1e6
* minibatch size: 256
* discount factor (gamma): 0.99
* tau for soft update of target parameters: 1e-2
* learning rate actor: 1e-3
* learning rate critic: 1e-3
* L2 weight decay: 0
* maximum number of timesteps per episode: 100000
* update interval: 2 timesteps

#### Selected neural network architecture
For actor:
* Network input: state-size -> 24 x 1 vector
* Number of nodes in first hidden fully-connected layer with ReLU applied: 256
* Number of nodes in second hidden fully-connected layer with ReLU applied: 128
* Number of nodes in output layer with tanh applied representing the potential actions: 2

For critic:
* Network input: state-size -> 24 x 1 vector
* Number of nodes in first hidden fully-connected layer with leaky ReLU applied: 256
* Number of nodes in second hidden fully-connected layer with leaky ReLU applied: 128
* Number of nodes in output layer applied representing the potential actions: 2

## Plot of Rewards
The environment was solved within **1872 episodes**.
As described in `README.md` the environment was considered to be solved, when the agents got an average score of +0.5 (over 100 consecutive episodes, after taking the maximum over both agents). Specifically,
* After each episode, rewards that each agent received are added up (without discounting), to get a score for each agent. This yields 2 (potentially different) scores. Then the maximum of these 2 scores is taken.
* This yields a single score for each episode.

#### The following plot of rewards was obtained during training:
![Alt text](plots/plot_of_rewards.png?raw=true "Title")

## Ideas for future work
Potential future work to be done:
Evaluate... 
* alternative Neural Network architectures
* alternative reinforcement learning algorithms
