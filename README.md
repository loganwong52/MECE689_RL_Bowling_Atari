# MECE689_RL_Bowling_Atari README

**Author:** Logan Wong
<br>
**Date:** September 24, 2025
<br>
**Course:** MECE 689: Reinforcement Learning
<br>
**Instructor:** Professor Ali Baheri

# Overview
This repository contains implementations of reinforcement learning algorithms, DQN, PPO, A2C, and QR-DQN, applied to the Atari 2600 game, Bowling, using OpenAI Gymnasium and Stable-Baselines3.

## File structure
```
MECE689_Bowling/                                        # Parent folder (not part of github)
├── initial_terminal.ipynb                              # "terminal file" I used to clone the github to google drive/google colab
├── MECE689_RL_Bowling_Atari/                           # The cloned github
│   ├── .git
│   ├── github_terminal.ipynb                           # The "terminal file" I use to add, commit, and push to github
│   ├── .gitignore
│   ├── code/                                           # Folder with files for baseline & 3 RL algorithms
│   │   ├─ attempt_1.ipynb                              # My first file where I was playing around with OpenAI Gymnasium & ALE
│   │   ├─ dqn_baseline.ipynb                           # trains the baseline DQN model
│   │   └─ eval_dqn_baseline.ipynb                      # evaluates the baseline DQN model
│   ├── checkpoints/                                    # Folder with all checkpoints, saved every 10K steps
│   │   ├─ dqn_baseline_10000000_10000000_steps.zip
│   │   ├─ ...
│   │   └─ dqn_baseline_10M_10000_steps.zip
│   ├── models/
│   │   └─ dqn_baseline_10000000.zip                    # Trained DQN Model for 10M time steps
│   ├── results/
│   └── README.md
```
# Installation

1. Create a .ipynb file that will act as your terminal
2. Mount google drive
3. change directory to your folder
4. git clone https://github.com/loganwong52/MECE689_RL_Bowling_Atari.git
5. cd MECE689_RL_Bowling_Atari

Exit this .ipynb and go into the newly cloned MECE689_RL_Bowling_Atari folder

# Training
1. Open /code
2. Run dqn_baseline.ipynb
3. Once it is done running, it will have saved many checkpoints to /checkpoint
4. And it will also have saved the trained model to /models

# Evaluation
1. Open /code
2. Run eval_dqn_baseline.ipynb


