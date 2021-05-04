# Report on description of implementation

## Learning Algorithm

#### Chosen hyperparameters

#### Selected neural network architecture

## Plot of Rewards
The environment was solved within **581 episodes**.
As described in `README.md` the environment was considered to be solved, when the agents got an average score of +0.5 (over 100 consecutive episodes, after taking the maximum over both agents). Specifically,
* After each episode, rewards that each agent received are added up (without discounting), to get a score for each agent. This yields 2 (potentially different) scores. Then the maximum of these 2 scores is taken.
* This yields a single score for each episode.

#### The following plot of rewards was obtained during training:
![Alt text](plots/plot_of_rewards.png?raw=true "Title")

## Ideas for future work
Potential future work to be done:
Evaluate... 
* xxxx
