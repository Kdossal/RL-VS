# Reinforcement Learning for Best Subset Variable Selection
This repository contains all code, datasets, and documentation developed for the thesis "Reinforcement Learning for Best Subset Variable Selection", undertaken by **Kameel Dossal** under the guidance of Professor **Alice Paul** at Brown University. The project delves into how Reinforcement Learning (RL) can be leveraged to enhance the Branch and Bound (B&B) algorithm's performance in Best Subset Selection problems for sparse linear regression.

Our work is built off research conducted by Tobias DeKara, which combined RL with Mixed Integer Quadratic Optimization (MIQO) for a refined approach to the variable selection problem. We extended this foundation by fine-tuning RL's application to optimize the B&B algorithm further, focusing on computational efficiency and variable selection accuracy in high-dimensional data analysis.


## Repository Structure
- `Models/`: Stored Trained Models
- `Results/`: Experiment results, `results.md` gives an overview for each file
- `Synthetic_Data/`: 
    - `gen_syn_data.py`: Script for generating synthetic data for variable selection.
    - `label/`: Batch of Synthetic Data Generated Labled with Setting
- `Explore.ipynb`: Jupyter Notebook for model tuning, exploring the B&B algorithm, and evaluating results.
- `Main.py`: Main script to run B&B Algorithm on synthetic data. Outputs are stored in Results/ and models in Models/.
- `Model`: Code for creating our DQN Agent
- `Node.py`: Code for the Node class/data structure within the tree.
- `Settings.py`: Configuration file for specifying hyperparameters, dataset selection, and storage options for running `Main.py`.
- `Tree.py`: Contains the problem and tree classes used for the variable selection task.

## Getting Started
1. Clone the repository.
2. Install required dependencies.
3. Run gen_syn_data.py to generate synthetic data.
4. Tune settings in setting.py.
5. Use main.py to execute the algorithms and generate results.
6. See Explore.ipynb to explore results and a guide to our code.
