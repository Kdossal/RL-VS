# Results Documentation
## Developing Model Architecture

### Round 0 -- Using Retrobranching and Binary rewards
Defualt hyperparams:
- 32 -> 32 -> 16 -> 1 
- BATCH_SIZE 32 
- GAMMA 0.99
- 128 Iterations of Learning after each episode

results 0: p10, 100 episodes

results 1: p50, 100 epsiodes

results 2: p50, 100 epsiodes (TARGET_UPDATE 10)

results 3: p50, 250 episodes (TARGET_UPDATE 10)

### Round 1 -- Updated 34 total states, same model is trained during all results
**Optimal m value is now being set for each batch, ensuring algo. efficiency**
Defualt hyperparams: 
- 34 -> 32 -> 16 -> 1
- BATCH_SIZE 32
- GAMMA 0.99
- 128 Iterations of Learning after each episode
- TARGET_UPDATE 2

results 4: p50, 250 episodes 

results 5: p50, 500 episodes

results 6: p50, 500 episodes

results 7: p50, 500 episodes 
- Comparing against randomly selected algorithm


### Round 2
Defualt hyperparams: 
- 34 -> 64 -> 16 -> 1
- BATCH_SIZE 32
- GAMMA 0.99
- 128 Iterations of Learning after each episode
- TARGET_UPDATE 2

results 8: p50, 500 episodes

results 9: p10, 250 episodes 
- Eliminated Relu on last hidden layer of DQN, was leading to the dying relu problem

results 10: p50, 500 episodes 

results 11: p50, 500 episodes 
- Recreate previous

results 12: p10, 500 episodes 
- Comparing to Strong Branching 


### Round 3 -- Using Offline Learning
- 34 -> 64 -> 16 -> 1
- BATCH_SIZE 32
- GAMMA 0.99
- 128 Iterations of Learning after each episode
- TARGET_UPDATE 2

results 13: p10, Offline Learning ~200 Episodes
- Comparing Offline Max Frac Branch and Strong Branching Experieneces

results 14: p50, Offline Learning ~100 Episodes
- Comparing Offline Max Frac Branch and Strong Branching Experieneces

### Round 4 -- Using Updated Continuous Rewards
- 34 -> 64 -> 16 -> 1
- BATCH_SIZE 64
- GAMMA 0.99
- 16 Iterations of Learning after each episode
- TARGET_UPDATE 1

results 15: p10, 100 Episodes

results 16: p50, 500 Episodes

results 17: p50, 500 Episodes 

### Round 5 -- Only Adding Sample of 128 State Pairs to Memory after each Episode
- 34 -> 64 -> 16 -> 1
- BATCH_SIZE 64
- GAMMA 0.9
- 16 Iterations of Learning after each episode
- TARGET_UPDATE 1

results 18: p10, 100 Episodes

results 19: p50, 250 Episodes

results 20: p50, 100 Episodes (8 iters)

results 21: Mixed Settings, 100 Episodes (8 iters)

### Round 6
- 34 -> 64 -> 16 -> 1
- BATCH_SIZE 64
- GAMMA 0.8
- 8 Iterations of Learning after each episode
- TARGET_UPDATE 1

results 22: p10, 100 Episodes

results 23: p50, 100 Episodes

results 24: p100, 100 Episodes
- Training stopped at Episode 87, model training post episode limit saw a decrease in performance

results 25: Mixed Settings, 100 Episodes
- Training stopped at Episode 91, model training post episode limit saw a decrease in performance

### Round 6 -- Updated default methods to always select node with global lowest bound
- 34 -> 128 -> 32 -> 16 -> 1
- BATCH_SIZE 64
- GAMMA 0.8
- 8 Iterations of Learning after each episode
- TARGET_UPDATE 1

results 26: Mixed Settings, 100 Episodes
- Training stopped at Episode 60, model training post episode limit saw a decrease in performance

### Validation 
Comparing P10, P50, P100 and Mixed Models against Max Fraction Branch and Strong Branching 

- p10_val: Validation p10, 25 Episodes

- p50_val: Validation p50, 25 Episodes

- p100_val: Validation p100, 25 Episodes

### Testing
Comparing Mixed Model against Max Fraction Branch and Strong Branching 

- testing: Randomly Generated Data, 25 Episodes, p:10-150

- testing_final: Randomly Generated Data, 25 Episodes, p:50-200