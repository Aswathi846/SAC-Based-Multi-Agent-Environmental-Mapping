# SAC-Based-Multi-Agent-Environmental-Mapping
This project applies the Soft Actor-Critic (SAC) algorithm to multi-agent environmental mapping. Agents explore simulated environments, build occupancy grid maps, and are assessed on coverage, accuracy, and robustness, offering insights into cooperative exploration and reinforcement learning.

# Abstract
This research addresses a critical gap in autonomous environmental monitoring: the need for a sample-efficient and robust Deep Reinforcement Learning (DRL) framework for multi-agent mapping in continuous environments. The project models the problem as a Multi-Agent Markov Decision Process (MDP) and implements a system based on the Soft Actor-Critic (SAC) algorithm. A key contribution is a novel dual-mode simulation environment, developed using the Gymnasium API, which supports both static, real-world maps for benchmarking and dynamic, procedurally generated maps for testing generalization. The system is systematically optimized using the Optuna framework and benchmarked against a DQL-based approach from a foundational study by Barrionuevo, et al. (2024) . The results demonstrate that the proposed SAC agent significantly outperforms the baseline in mapping accuracy (MSE), successfully generalizes to smooth dynamic environments, and provides critical insights into the challenges of DRL for "hard exploration" problems and the importance of aligning reward signals with true task objectives.

# Key Features
Continuous Control: Implements the Soft Actor-Critic (SAC) algorithm to enable agents with fluid and precise movements in a continuous action space.

Multi-Agent System: A centralized training, decentralized execution (CTDE) paradigm is used to train multiple agents to perform cooperative mapping.

Dual-Mode Environment: A custom Gymnasium environment that can operate in two modes:

Dataset-Based: Utilizes static, real-world maps for reproducible benchmarking.

Ground-Truth-Based: Procedurally generates dynamic maps using AlgaeBloom (Gaussian) and Shekel (peaky) models to test policy generalization.

Hyperparameter Optimization: Integrates the Optuna framework for systematic and efficient hyperparameter tuning.

Comprehensive Evaluation: Measures performance using a suite of metrics, including Mean Squared Error (MSE), Mean Absolute Error (MAE), and R² Score, to assess map reconstruction quality.
