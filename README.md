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
├── initial_terminal.ipynb                              # "terminal file" I used to clone the github to google colab (not part of github)
├── MECE689_RL_Bowling_Atari/                           # The cloned github
│   ├── .git
│   ├── github_terminal.ipynb                           # The "terminal file" I use to add, commit, and push to github
│   ├── .gitignore
│   ├── code/                                           # Folder with files for baseline, 3 RL algorithms, 4 Ablation Studies, and 7 Hyperparameter Tuning files.
│   │   ├─ a2c_bowling_tensorboard                          # Folder with training curves for A2C
│   │   ├─ dqn_bowling_tensorboard/DQN_1                   # Folder with training curves for DQN
│   │   ├─ ppo_bowling_tensorboard                         # Folder with training curves for PPO
│   │   ├─ qr_dqn_bowling_tensorboard/QRDQN_1                # Folder with training curves for QRDQN
│   │   ├─ A2C.ipynb                            # trains the baseline A2C model
│   │   ├─ A2C_Ablation_Study_1.ipynb
│   │   ├─ A2C_Ablation_Study_2.ipynb
│   │   ├─ A2C_Ablation_Study_3.ipynb
│   │   ├─ A2C_Ablation_Study_4.ipynb
│   │   ├─ PPO.ipynb                            # trains the baseline PPO model
│   │   ├─ PPO_Hyperparameter_Tuning_1.ipynb
│   │   ├─ PPO_Hyperparameter_Tuning_2.ipynb
│   │   ├─ PPO_Hyperparameter_Tuning_3.ipynb
│   │   ├─ PPO_Hyperparameter_Tuning_4.ipynb
│   │   ├─ PPO_Hyperparameter_Tuning_5.ipynb
│   │   ├─ PPO_Hyperparameter_Tuning_6.ipynb
│   │   ├─ PPO_Hyperparameter_Tuning_7.ipynb
│   │   ├─ QR_dqn.ipynb                            # trains the baseline QRDQN model
│   │   ├─ dqn_baseline.ipynb                            # trains the baseline DQN model
│   │   ├─ eval_A2C.ipynb                            # evaluates the A2C model
│   │   ├─ eval_A2C_Ablation_Study_1.ipynb            
│   │   ├─ eval_A2C_Ablation_Study_2.ipynb
│   │   ├─ eval_A2C_Ablation_Study_3.ipynb
│   │   ├─ eval_A2C_Ablation_Study_4.ipynb
│   │   ├─ eval_PPO.ipynb                      # evaluates the PPO model
│   │   ├─ eval_PPO_HP_Tuning_1.ipynb
│   │   ├─ eval_PPO_HP_Tuning_2.ipynb
│   │   ├─ eval_PPO_HP_Tuning_3.ipynb
│   │   ├─ eval_PPO_HP_Tuning_4.ipynb
│   │   ├─ eval_PPO_HP_Tuning_5.ipynb
│   │   ├─ eval_PPO_HP_Tuning_6.ipynb
│   │   ├─ eval_PPO_HP_Tuning_7.ipynb
│   │   ├─ eval_QR_dqn.ipynb                     # evaluates the QRDQN model
│   │   ├─ eval_dqn_baseline.ipynb                    # evaluates the baseline DQN model
│   │   ├─ histograms_and_boxplots.ipynb                      # Plots histograms and box plots of all trained models
│   │   ├─ random_agent_for_eval.ipynb                                       # evaluates a random agent to help me calculate HNS and HWRNS
│   │   ├─ xxx_playing_around_with_eval_A2C_Ablation_Study_3.ipynb                        # Extra analysis for the A2C Ablation Study 3 model
│   │   ├─ yyy_playing_around_with_eval_dqn_baseline.ipynb                                 # Extra analysis for the DQN model
│   │   └─ zzz_playing_around_with_trained_PPO.ipynb                       # Extra analysis for the PPO model
│   ├── results/                                    # Folder with all .npy files containing data created by the "Eval" files
│   ├── models/
│   │   ├─ a2c_10000000.zip                    # Trained A2C Model for 10M time steps
│   │   ├─ a2c_10000000_Ablation_Study_1.zip
│   │   ├─ a2c_10000000_Ablation_Study_3.zip
│   │   ├─ a2c_10000000_Ablation_Study_4.zip
│   │   ├─ a2c_20000000_Ablation_Study_2.zip    # Trained A2C Ablation Study 2 Model for 20M time steps
│   │   ├─ dqn_baseline_10000000.zip            # Trained DQN Model for 10M time steps
│   │   ├─ ppo_10000000.zip                      # Trained PPO Model for 10M time steps
│   │   ├─ ppo_10000000_HP_Tuning_1.zip
│   │   ├─ ppo_10000000_HP_Tuning_2.zip
│   │   ├─ ppo_10000000_HP_Tuning_3.zip
│   │   ├─ ppo_10000000_HP_Tuning_4.zip
│   │   ├─ ppo_10000000_HP_Tuning_5.zip
│   │   ├─ ppo_10000000_HP_Tuning_6.zip
│   │   ├─ ppo_10000000_HP_Tuning_7.zip
│   │   └─  qr_dqn_10000000.zip                  # Trained QRDQN Model for 10M time steps
│   ├── videos/                                        # Folder with all .mp4 files created by the "Eval" files
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
2. Run non "Eval" .ipynb files
3. Once it is done running, it will also have saved the trained model to /models
4. Run the corresponding "Eval" .ipynb file
# Evaluation
1. Open /code
2. Run eval_dqn_baseline.ipynb


