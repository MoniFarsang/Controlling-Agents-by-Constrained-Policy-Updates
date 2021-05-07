# Deep Reinforcement Learning in Robotics

This repository is based on my project [Decaying Clipping Range in Proximal Policy Optimization](https://github.com/MoniFarsang/ppo-clipping-approaches), which is the fork from [Stable Baselines3](https://github.com/DLR-RM/stable-baselines3). 

This code can be used for the Proximal Policy Optimization (PPO) algorithm analysis of the linearly, exponentially and Z-shaped decaying clipping and applying moving average clipping ranges.

The following environments are examined:

OpenAI Gym:
- Classical control:
  - CartPole
  - Pendulum
  - Acrobot
- Box2D:
  - Lunar Lander
  - Bipedal Walker
  - Car Racing

PyBullet:
- Hopper
- Walker
- Half-Cheetah


## Enjoy the trained  PPO agent

The trained agents are added to the repo. The exp-id refers to the different clipping strategies (1: constant, 2: linearly decaying, 3: exponentially decaying, 4: Z-shaped decaying, 5: using moving average). If the trained agent exists, then you can see it in action using:
```
python enjoy.py --algo ppo --env env_id --exp-id number
```

For example, enjoy PPO with linearly decaying clipping range on CartPole during 5000 timesteps:
```
python enjoy.py --algo ppo --env CartPole-v1 --exp-id 2 -n 5000
```

## Train the PPO agent

For training the agent, use the following command:
```
python train.py --algo ppo --env env_id
```

For example:
```
python train.py --algo ppo --env CartPole-v1 --tensorboard-log /tmp/stable-baselines/
```



