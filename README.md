# CI2025_lab2

## Key Operations

### Selection:  
   Roulette selection (converts “shorter is better” into probability; uniform sampling when lengths are equal).
### Crossover: 
Copy segment [a,b] from parent 1 to the corresponding position in the offspring;
Fill in missing cities sequentially from parent 2, starting from the right cutpoint and filling in a circular manner.
### Mutation: 
Randomly swap two positions.

--------

## Iteration (maxSteps rounds total):

### 1.Select two parents using roulette selection;
### 2.Perform OX crossover to generate offspring, applying swap mutation probabilistically;
### 3.Calculate offspring length; if better than the “worst individual” in the current population, replace it immediately (steady-state replacement, no whole-generation reordering).
### Restart: If no improvement occurs for consecutive patience rounds, replace several worst individuals with entirely new random ones at restart_frac (like, 30%), reset the stagnation counter, and continue evolution.
