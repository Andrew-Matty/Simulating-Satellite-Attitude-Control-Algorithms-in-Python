# Simulating-Satellite-Attitude-Control-Algorithms-in-Python
MSc Dissertation Project investigating PID and MPC attitude controller performance

## Overview

This repository contains Python-based simulations of satellite attitude control algorithms, specifically Proportional-Integral-Derivative (PID) and Model Predictive Control (MPC). These simulations were designed to model the Lunar Reconnaissance Orbiter (LRO) satellite dynamics, testing the performance of these control algorithms under various conditions.

## Project Structure

- **`src/`**: Contains the Python scripts implementing the PID and MPC controllers, along with the simulation scenarios.
- **`results/`**: Stores output data from the simulations, including plots and performance metrics.
- **`docs/`**: Includes the report and any additional documentation.

## Simulation Scenarios

The simulations assess the performance of the controllers in the following scenarios:

1. **Attitude Maneuver**: Simulating an undisturbed rotation to model the satellite pointing its instruments in a new direction.
2. **External Disturbance**: A stationary maneuver with an external disturbance torque applied to test the controllers' disturbance rejection capabilities.
3. **Spacecraft Tumbling**: Evaluating the stabilizing abilities of the controllers on a tumbling satellite.

## Key Findings

- **MPC Controller**: Demonstrated the fastest response in achieving the desired satellite orientation. However, it struggled with external disturbances and is more computationally intensive.
- **PID Controller**: Showed better performance in handling external disturbances and is computationally less demanding.

## How to Run

1. Clone the repository:
    ```bash
    git clone https://github.com/Andrew-Matty/satellite-attitude-control-algorithms-in-python.git
    ```
2. Navigate to the `src/` directory:
    ```bash
    cd satellite-attitude-control/src
    ```
3. Run the desired simulation script:
    ```bash
    python simulate_pid.py
    ```
    or
    ```bash
    python simulate_mpc.py
    ```

## Dependencies

Ensure you have the following Python packages installed:

- `numpy`
- `scipy`
- `matplotlib`
- `cvxpy` (for MPC simulations)

Install the dependencies via pip:

```bash
pip install -r requirements.txt
