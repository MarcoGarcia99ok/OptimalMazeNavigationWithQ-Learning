# Maze Navigation with Q-Learning

## Description
This project implements a reinforcement learning agent that learns to navigate a 2D maze using the Q-Learning algorithm. The maze is represented as a grid where each cell can be:

1) A free path (0)
2) An obstacle (1)
3) The objective (9)

The agent starts at a predefined position and learns to reach the goal while avoiding obstacles through trial and error. The learning process is guided by rewards and    penalties.

## Features
- Generates a customizable 2D maze with obstacles and a goal position.
- Uses the Q-Learning algorithm to train an agent to navigate the maze.
- Balances exploration and exploitation with an epsilon-greedy strategy.
- Implements visualization of the maze and the learned path.
- Demonstrates reinforcement learning concepts such as reward shaping and policy improvement.

## Getting Started

### Prerequisites
Ensure you have the following installed:
- Python 3.x
- Required Python libraries:
- numpy
- matplotlib
- random (built-in)

## Installation

1. Clone this repository or download the files.

2. Install the required Python libraries if not already installed:
   pip install numpy matplotlib

## Usage
### Running the Project
1. Import the required libraries and functions.
2. Define the maze parameters such as size, wall percentage, start, and goal positions.
3. Generate the maze using the maze_creation function.
4. Train the agent using Q-learning.
5. Visualize the maze and the learned path with show_agents_learning.

## Example
### Define maze parameters
size = 10
start_position = (0,0)
goal_position = (9,9)

#### Generate maze
maze = maze_creation(size, 20, start=start_position, goal=goal_position)

#### Convert positions to index
start = index_position(start_position, size)
goal = index_position(goal_position, size)

#### Train agent
Q_values = q_learning(maze, size, start, goal)

#### Show learned path
show_agents_learning(maze, Q_values, start, goal, size)

#### Define maze parameters
size = 10
start_position = (0,0)
goal_position = (9,9)

#### Generate maze
maze = maze_creation(size, 20, start=start_position, goal=goal_position)

#### Convert positions to index
start = index_position(start_position, size)
goal = index_position(goal_position, size)

#### Train agent
Q_values = q_learning(maze, size, start, goal)

#### Show learned path
show_agents_learning(maze, Q_values, start, goal, size)

## Q-Learning Algorithm
1. Initialize a Q-table with zeros for all possible state-action pairs.
2. For a given number of episodes:
   - Start at the initial position.
   - Select an action based on the epsilon-greedy policy.
   - Move according to the action and receive a reward or penalty.
   - Update the Q-table using the Bellman equation:
     "Q[state, action] += alpha * (reward + gamma * max(Q[next_state, :]) - Q[state, action])"
   - Repeat until reaching the goal.

## Visualization
- The maze is displayed using Matplotlib.
- The learned path is overlaid on the maze with markers indicating the agent’s trajectory.

## Contributing
Contributions are welcome. If you have improvements or suggestions, feel free to open an issue or submit a pull request.

## License
This project is licensed under the MIT License.

## Acknowledgments
Thank you for exploring reinforcement learning with Q-Learning! Thanks Fede for your support!

