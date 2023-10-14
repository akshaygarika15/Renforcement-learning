## Solving a simple 4*4 Gridworld almost similar to openAI gym frozenlake using Monte-Carlo method Reinforcement Learning

WRITTEN BY Garika Akshay
# Solving a 4x4 Gridworld with Monte-Carlo Reinforcement Learning

## Introduction

This program utilizes reinforcement learning to solve a 4x4 gridworld environment, similar to OpenAI Gym's FrozenLake. The chosen method is policy iteration, a fundamental approach in dynamic programming.

## Environment Description

The gridworld consists of the following elements:

- `S`: Start cell
- `O`: Normal cells
- `*`: Penalized cells
- `T`: Terminate cell

## Rewards

Positive and negative rewards for each cell are stored in the `Rewards` dictionary, which can be modified by the user. For example:

- `(3, 3)` (Goal): +5
- `(1, 3)` (Hole): -2
- `(2, 1)` (Penalized): -2
- `(3, 1)` (Penalized): -2

## Algorithm Flow

1. **Initialization**:
   - A random policy is created to indicate preferred moves in each cell.
   - Q-table is initialized with zeros.

2. **Policy Iteration**:
   - The program iteratively refines the policy using Monte-Carlo method.

## Sample Output

After a certain number of steps, the program displays the updated policy:

- Step 0
   ```plaintext
   Policy:  
   | D |  | D |  | L |  | L |   
   | U |  | L |  | L |  | U |   
   | D |  | D |  | D |  | D |   
   | U |  | R |  | R |   
## Results

### Step 25
```plaintext
Policy:  
| R |  | D |  | L |  | L |   
| R |  | R |  | D |  | U |   
| D |  | D |  | D |  | D |   
| R |  | R |  | R |   

### Step 200
```plaintext
Policy:  
| R |  | D |  | L |  | L |   
| R |  | R |  | D |  | U |    
| D |  | D |  | D |  | D |   
| R |  | R |  | R |

##Q-Table
#Here's a snippet of the Q-table:

(0, 0): {'D': 1.42, 'R': 2.78},
(0, 1): {'L': 1.20, 'D': 2.77, 'R': 1.25},
...
(3, 2): {'U': 1.06, 'L': -2.28, 'R': 4.50}      
  
