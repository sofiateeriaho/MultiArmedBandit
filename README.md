## University assignment for Reinforcement Learning course

Two different implementations of the multi-armed bandit problem using reinforcement learning in combination with various exploration/exploitation methods.

The file [`normal.py`](normal.py) models the multi-armed bandit problem in which the reward obtained from each action is sampled from a Gaussian distribution. 

The file [`bernoulli.py`](bernoulli.py) models the multi-armed bandit problem in which the reward obtained from each action is sampled from a Bernoulli distribution.

The following exploration methods were compared:
- greedy
- epsilon-greedy
- optimistic initial values
- softmax policy
- UCB (Upper-Confidence-Bound)

When running the files, both produce the average reward value per time step plot and also print the percentages the best action (per experiment) is chosen given each method.

One thing to point out is that, we ran into an error concerning floating point numbers which results in the plot producing one or more single horizontal lines. For reference, the plots provided in our report are the correct ones. If the plot doesn't look similar to the ones in the report then we recommend running the code a second or third time.

In addition, for the bernoulli distribution the average rewards (avg_rewards) exceed a reward value of 1 in the y-axis of the plot if this line `print(avg_rewards)` is not included in front of `plt.plot(avg_rewards, label=algorithm_names[idx])`. 
