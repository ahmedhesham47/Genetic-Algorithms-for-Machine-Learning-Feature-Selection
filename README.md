# Genetic-Algorithms-for-Machine-Learning-Feature-Selection

## Project Description:

- This project implements a genetic algorithm (GA) to select a subset of features from a labeled gene expression dataframe. 
- The GA optimizes feature selection to enhance the performance of a logistic regression classifier used to predict a binary outcome. 
- The project allows varying hyperparameters such as population size, number of selected parents, crossover probability, crossover type, mutation probability, mutation type, maximum selected features, type of fitness function, and the number of generations.

## Customizable Features:

- Various hyperparameters: User can control many hyperparameters, which adds flexibility to the algorithm.
- Multiple fitness functions: User can evaluate accuracy with two different fitness evaluations, which may be data dependent. If there are many DEGs in the data, the difference of means function may be better. If the pattern is more complicated, the ML function may be more accurate.
- Parameter testing: User can run experiments with different combinations of parameters using itertools.product.

## Prerequisites
- Python 3.8+ recommended, along with the following Python libraries:
- Pandas
- NumPy
- Matplotlib (for visualization)
- Scikit-learn (for logistic regression fitness function and evaluation)

## Usage
- Prepare Your Data: Ensure the gene expression data is in a CSV/TSV file with samples as rows and genes as columns. The last column should be the binary label for the classification and the first column should be the sample identifier.
- Run a simple trial using this line >> GA = genetic_algorithm(your_data, population_size=50, num_generations=25, max_selected_features=120, crossover_prob=0.1, mutation_prob=0.1, multiple_mutations=False, crossover_type='s', fitness_function="mean")
- Visualize the fitness vs generation curve.
- Run multible combinations using the run_experiments() function and prepring a list of the desired parameters to try beforehand.
- Compare accuracies vs standard Recursive Feature Elimination and Mutual Information feature selection methods.

## Author:
Ahmed H. Saadawy
