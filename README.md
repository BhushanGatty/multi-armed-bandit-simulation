# Epsilon-Greedy Multi-Armed Bandit Simulation

## Overview

This repository contains a Python script that simulates the performance of the epsilon-greedy reinforcement learning algorithm on a multi-armed bandit problem. The simulation is designed to demonstrate the trade-off between exploration and exploitation in decision-making, showcasing how different epsilon values (the probability of exploration) impact the agent's cumulative reward over time.

![Epsilon-Greedy Performance Plot]: <img width="846" height="472" alt="epsilon-greedy performance on 10-Armed Bandit Tasks" src="https://github.com/user-attachments/assets/12e72a7c-6045-4b84-bca2-d771bc765bc5" />

## What is a Multi-Armed Bandit?

A multi-armed bandit is a classic problem in reinforcement learning. Imagine you're in a casino, faced with several slot machines (one-armed bandits), each with an unknown probability distribution of rewards. Your goal is to maximize your total winnings over a series of pulls. The challenge is to figure out which machine is best (exploitation) while also trying out other machines to ensure you haven't missed an even better one (exploration).

## Epsilon-Greedy Strategy

The epsilon-greedy strategy is a simple yet effective approach to solving the multi-armed bandit problem. At each step, the agent:

*   **Explores (with probability \$\epsilon\$):** Randomly chooses an arm to pull.
*   **Exploits (with probability 1 - \$\epsilon\$):** Chooses the arm with the highest estimated average reward so far.

This simulation compares three different epsilon values: 0 (pure greedy, always exploiting), 0.01 (small exploration), and 0.1 (moderate exploration).

## Code Structure

The main script is organized into three parts:

1.  **`run_epsilon_greedy_simulation` function**: Encapsulates the core simulation logic. It runs multiple bandit tasks for a given set of epsilon values and records the rewards.
2.  **`plot_results` function**: Handles the visualization of the simulation results, generating a line plot showing average rewards over steps for each epsilon strategy.
3.  **Main Execution Block (`if __name__ == "__main__":`)**: Defines simulation parameters, calls the simulation function, and then plots the outcomes.

## How to Run the Code

To run this simulation, you will need Python 3 and the following libraries:

*   `numpy`
*   `matplotlib`

You can install them using pip:

```bash
pip install numpy matplotlib
