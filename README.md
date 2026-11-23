# Physics-Informed Neural Networks (PINNs)

**02456 Deep Learning – DTU, Fall 2026**

**Group 55**

This repository contains our implementation of Physics-Informed Neural Networks (PINNs) for Project 1 in the course 02456 Deep Learning at the Technical University of Denmark (DTU).

The project explores how neural networks can learn solutions to differential equations by combining training data with known physical laws.

## Project Overview

The project consists of three tasks:

- **Task 1 – Analytical Derivatives:** Derivation of first- and second-order derivatives for a feedforward neural network with one hidden layer and tanh activation.

- **Task 2 – Damped Harmonic Oscillator:** Implementation of a PINN to solve the damped harmonic oscillator equation. We compare manually derived gradients with PyTorch autograd, investigate different physics weights, and compare soft and hard enforcement of initial conditions.

- **Task 3 – Heat Equation:** Application of a PINN to the one-dimensional heat equation, comparing its predictions with the analytical solution.

## Requirements

The project uses Python with NumPy, PyTorch, SciPy, Matplotlib, and Jupyter Notebook.

We have included a `dlenv.yml` file that can be used to set up the environment with all the required packages.

## Running the Code

First, clone the repository:

```bash
git clone https://github.com/oscarlomborg/02456_PINN-Project_Group55.git
cd 02456_PINN-Project_Group55
```

If you use Conda, you can set up the environment using the provided file:

```bash
conda env create -f dlenv.yml
```

Then activate the environment using the name specified in `dlenv.yml` and start Jupyter:

```bash
jupyter notebook
```

Alternatively, you can install the main packages manually:

```bash
pip install numpy torch scipy matplotlib jupyter
```

Once Jupyter is running, open the notebooks and run the cells in order. Some experiments take longer to train, and a few cells use saved model parameters to avoid repeating the training.