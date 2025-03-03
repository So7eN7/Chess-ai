# Chess AI with Reinforcement Learning

## Overview
This project fine-tunes reinforcement learning (RL) models to play chess using Stable-Baselines3 (SB3) and OpenSpiel(WIP). It targets a 2–3 hour training window on an NVIDIA RTX 4070 SUPER GPU, focusing on DQN, PPO, A2C, and an AlphaZero-inspired approach(WIP). The framework includes a custom chess environment, neural network policies, RL training, and an interactive play interface with visual board display.

## Table of Contents

### 1. Project Setup
- **Purpose**: Installs dependencies and configures the GPU environment.
- **File**: `Cell 1` in Jupyter notebook.
- **Key Tools**: Python libraries, PyTorch, SB3.

### 2. Chess Environment
- **Purpose**: Defines the chess game as a Gymnasium environment for RL.
- **File**: `Cell 2` in Jupyter notebook.
- **Key Features**: Board state representation, actions, rewards.

### 3. Neural Network Policy
- **Purpose**: Sets up neural network architectures for SB3 models.
- **File**: `Cell 3` in Jupyter notebook.
- **Key Features**: Feature extractor, DQN vs. actor-critic policies.

### 4. Fine-Tuning with RL
- **Purpose**: Trains models via self-play in ~2–3 hours.
- **File**: `Cell 4` in Jupyter notebook.
- **Key Features**: SB3 (DQN, PPO, A2C).

### 5. Interactive Play
- **Purpose**: Loads models and enables human vs. AI play with visual display.
- **File**: `Cell 5` in Jupyter notebook.
- **Key Features**: SVG board, move input, debugging output.

## Prerequisites
- **Hardware**: Single NVIDIA RTX 4070 SUPER GPU.
- **Software**: 
  - Python 3.8+
  - Dependencies: Install via `pip install torch==2.0.1 stable-baselines3==2.0.0 gymnasium==0.29.1 python-chess cairosvg IPython`
- **Environment**: Jupyter Notebook for interactive execution.

## Quick Start
1. **Setup**: Run Cell 1 to install libraries and check GPU.
2. **Environment**: Run Cell 2 to define the chess environment.
3. **Policy**: Run Cell 3 to configure neural networks.
4. **Train**: Run Cell 4 to fine-tune models (~2–3 hours). (Not needed, load the models instantly).
5. **Play**: Run Cell 5 to test against the AI (e.g., `play_against_agent("PPO", human_color=chess.WHITE)`).

## Project Structure
- **Notebook**: Single Jupyter file with 5 cells.
- **Models**: Saved as `.zip` files in `./chess_models_sb3/` (SB3 only).
- **No PGN Pre-training**: Focuses on RL self-play; extendable with PGN data.

## Notes
- **Training Time**: ~2–2.5 hours for SB3 models (~400 games).
- **Performance**: Basic tactical play after fine-tuning; not grandmaster-level.
- **Customization**: Adjust `num_timesteps` (SB3) for time/performance trade-offs.

## License
MIT License—feel free to use, modify, and share.
