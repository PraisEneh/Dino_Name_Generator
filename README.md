# Dinosaur Name Generator RNN

## Description

This project implements a Recurrent Neural Network (RNN) to generate dinosaur names. The RNN is trained on a dataset of existing dinosaur names and learns to generate new, plausible-sounding names.

## Files

- `run_dino.py`: Main script to run the dinosaur name generator
- `utils.py`: Utility functions for RNN operations
- `dinos.txt`: Dataset containing dinosaur names

## Features

- Character-level RNN for text generation
- Customizable hyperparameters (hidden state size, number of iterations, etc.)
- Periodic sampling to check learning progress
- Gradient clipping to prevent exploding gradients

## Requirements

- Python 3.x
- NumPy

## Usage

1. Ensure you have a `dinos.txt` file with one dinosaur name per line in the same directory as the scripts.
2. Run the main script:

```
python run_dino.py
```

3. The script will train the RNN and periodically output generated dinosaur names.

## Key Functions

- `sample()`: Generates a new dinosaur name
- `optimize()`: Performs one step of optimization (forward prop, backward prop, parameter update)
- `model()`: Trains the RNN model and generates names

## Customization

You can adjust the following parameters in the `model()` function call:

- `num_iterations`: Number of training iterations
- `n_a`: Size of the RNN hidden state
- `dino_names`: Number of names to generate at each sampling step

## Output

The script will print:
- Training loss every 2000 iterations
- A set of generated dinosaur names every 2000 iterations
- The final generated name after training

## Note

This implementation uses a basic RNN architecture. For better results, consider using more advanced architectures like LSTM or GRU.
