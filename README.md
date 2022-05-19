# cs4811-su22-w2
Code and notebook for answering Q1 on W2. 

This code investigates using genetic algorithms to solve a problem. 

The problem considered is to generate a target phrase from a population of random strings (problem and code selected from [aima-python code repository](https://github.com/aimacode/aima-python) and examples).

## Problem 

For this problem, the phrase to be generated is `4811 + AI +GAs = fun!`.  

We will define the gene pool to consist of any string consisting of the upper and lower case English alphabet, digits 0-9, and a few puctuation characters - $\{$ space ! . + - , ?$\}$. 

Several parameters must be given for the genetic algorithm: 

* `ngen` - maximum number of generations the algorithm will run 
* `max_population` - the size of the population in each generation 
* `mutation_rate` - rate of mutation (value between 0 and 1) 
* `f_thres` - the fitness threshold use to determine if the target phrase is found, thus terminating the method. 

For this problem, the fitness function evaluates strings by the number of characters matching the target phrase: 

```
def fitness_fn(sample): 
	fitness = 0
    for i in range(len(sample)):
        if sample[i] == target[i]:
            fitness += 1
    return fitness
```

## Instructions 

1. Review the code in `ga.py`.
2. Open the w2_ga.ibynb notebook and run the GA with the default parameters.  
The GA reports out for each generation, the best individual (highest fitness), and the fitness function. 
[![Binder](https://mybinder.org/badge_logo.svg)](https://mybinder.org/v2/gh/lebrown/cs4811-su22-w2/HEAD?filepath=w2_ga.ipynb)
3. Explore the parameter space and answer the questions in **w2**.  

The solution to Q1(a) is provided to help get you started on how to answer Q1(b) and Q1(c). 
