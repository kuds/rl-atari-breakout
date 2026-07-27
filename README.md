# Beginner's Guide to Model-Based Reinforcement Learning (MBRL) with Atari's Breakout

## Simulated Policy Learning (SimPLe)

_Gameplay capture pending a full `Config.full_training()` run — drop the
resulting `videos/` or `rollouts/*.gif` artifact in at
`Images/atari_breakout_simple.gif` and restore the embed below._

<!-- ![](Images/atari_breakout_simple.gif) -->

## Deep Q Learning (DQN)

![](/Images/atari_breakout_dqn.gif)

## Proximal Policy Optimization (PPO)

![](/Images/atari_breakout_ppo.gif)

## Results
Hardware: Google Colab L4

| Environment            | Model Type | Average Reward    | Total Training Steps | HuggingFace                                                     |
|------------------------|------------|-------------------|----------------------|-----------------------------------------------------------------|
| BreakoutNoFrameskip-v4 | PPO        | 187.80 +/- 114.62 | 5,000,000            | [Link](https://huggingface.co/kuds/atari-breakout-v4-ppo)       |
| BreakoutNoFrameskip-v4 | DQN        | 239.20 +/- 73.63  | 5,000,000            | [Link](https://huggingface.co/kuds/atari-breakout-v4-dqn)       |
| ALE/Breakout-v5        | PPO        | 398.30 +/- 19.09  | 7,500,000            |                                                                 |
| ALE/Breakout-v5        | DQN        | 298.70 +/- 33.81  | 7,500,000            |                                                                 |
| ALE/Breakout-v5        | SimPLe     | _run pending_     | 97,500 real env steps (`Config.full_training()`) |                             |

Note on the SimPLe row: model-based training is measured in **real environment
steps**, and the notebook's `Config.full_training()` preset budgets 97,500 of
them (15 SimPLe iterations x 6,500 steps) in the spirit of Kaiser et al.'s
100k-step setting. That is not comparable to the millions of steps in the
model-free rows — sample efficiency is the entire point of the comparison. The
policy additionally sees ~96 million *imagined* transitions inside the learned
world model (15 iterations x 2,000 PPO updates x 50-step horizon x batch 64),
which cost no environment interaction.

## Finding Theta Blog Posts: 
- [Beginner's Guide to Model-Based Reinforcement Learning (MBRL) with Atari's Breakout](https://www.findingtheta.com/blog/beginners-guide-to-model-based-reinforcement-learning-mbrl-with-ataris-breakout)
