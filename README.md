# Emergency Response Simulator and Reinforcement using PPO

## Overview
The Emergency Response Simulator is a sophisticated project that models and optimizes emergency response strategies within a 30x30 urban grid. It employs Proximal Policy Optimization (PPO) in a reinforcement learning framework to enhance response efficiency to dynamically generated emergency incidents.

## Environment Setup

### Grid-Based Urban Model (`EmergencyResponseEnv`)
- **Structure**: 
  - A 30x30 grid representing an urban landscape.
  - Each grid cell can simulate different types of emergency incidents.
- **Resource Deployment**:
  - Multiple types of emergency response units are modeled, each with unique characteristics and capabilities.
  - Units are initially positioned at designated stations and can move across the grid.

### Incident Generation
- **Data-Driven Approach**:
  - Incidents are generated based on real-world statistical data (`combined_incidents.csv`).
  - Probabilistic models determine the frequency, type, and severity of incidents in different grid cells.
- **Dynamic Simulation**:
  - Each simulation step can introduce new incidents, mimicking real-time emergency scenarios.
  - Incident characteristics include severity levels, required resources, and resolution timeframes.

### State and Action Space
- **State Space**: 
  - Encapsulates the current status of all grid cells, emergency units, and active incidents.
  - Includes time-dependent factors to simulate varying conditions throughout the day.
- **Action Space**:
  - Defined by possible moves and actions of the emergency units.
  - Includes dispatching, moving units, and managing resources at incident locations.

### Reward System
- **Design**: Tailored to incentivize quick and effective resolution of incidents.
- **Positive Rewards**: Granted for efficiently addressing and resolving emergencies.
- **Negative Penalties**: Imposed for delays, resource mismanagement, or unaddressed incidents.

## PPO Implementation
- **Algorithm**: Proximal Policy Optimization, a policy gradient method for reinforcement learning.
- **Networks**: Separate policy and value networks to estimate optimal actions and value functions.
- **Training Loop**:
  - Interacts with the environment, collecting state, action, and reward data.
  - Periodically updates the policy based on the collected experiences.

## Data Processing and Analysis
- **Dataset Handling**: Utilizes `pandas` and `numpy` for data preprocessing and analysis.
- **Visualization Tools**: `matplotlib` and `seaborn` for insightful visual representations of data and simulation outcomes.

## Technologies and Libraries
- Python, Gymnasium (Gym)
- TensorFlow, Keras (for PPO models)
- Pandas, NumPy, Matplotlib, Seaborn

## Setup & Installation
1. Install dependencies: `pip install gymnasium tensorflow keras pandas numpy matplotlib seaborn`.
2. Clone the repository and set up the environment.

## Usage
- Run the Jupyter notebook for model training and simulation.
- Analyze and refine emergency response strategies based on simulation results.
