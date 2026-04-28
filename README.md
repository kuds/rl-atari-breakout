# Beginner's Guide to Model-Based Reinforcement Learning (MBRL) with Atari's Breakout

## Simulated Policy Learning (SimPLe)

![](/Images/atari_breakout_simple.gif)

## Deep Q Learning (DQN)

![](/Images/atari_breakout_dqn.gif)

## Proximal Policy Optimization (PPO)

![](/Images/atari_breakout_ppo.gif)

## Results
Hardware: Google Colab L4

| Environment            | Model Type | Average Reward    | Total Training Steps | HuggingFace                                                     |
|------------------------|------------|-------------------|----------------------|-----------------------------------------------------------------|
| BreakoutNoFrameskip-v4 | SimPLe     |                   | 5,000,000            |                                                                 |
| BreakoutNoFrameskip-v4 | PPO        | 187.80 +/- 114.62 | 5,000,000            | [Link](https://huggingface.co/kuds/atari-breakout-v4-ppo)       |
| BreakoutNoFrameskip-v4 | DQN        | 239.20 +/- 73.63  | 5,000,000            | [Link](https://huggingface.co/kuds/atari-breakout-v4-dqn)       |
| ALE/Breakout-v5        | PPO        | 398.30 +/- 19.09  | 7,500,000            |                                                                 |
| ALE/Breakout-v5        | DQN        | 298.70 +/- 33.81  | 7,500,000            |                                                                 |

## Finding Theta Blog Posts: 
- [Beginner's Guide to Model-Based Reinforcement Learning (MBRL) with Atari's Breakout](https://www.findingtheta.com/blog/beginners-guide-to-model-based-reinforcement-learning-mbrl-with-ataris-breakout)
