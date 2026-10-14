# AI-Based Autonomous Navigation System

A beginner-friendly virtual robotics project built with Python and Pygame. A virtual robot navigates a 2D grid from a start point to a destination while avoiding obstacles. The A* path-planning algorithm calculates a route, and the simulation visualizes the route and robot movement.

> **Scope:** This is a learning simulation, not a real self-driving system. It does not currently use a camera, trained neural network, real sensors, or physical motors.

## Features
- 2D virtual environment with obstacles
- A* path planning using Manhattan distance
- Animated robot movement along the planned route
- Recalculate route and add an obstacle while running
- On-screen status, path length, and step counter

## Tech stack
- Python 3.10 or newer
- Pygame
- A* search algorithm

## Project structure
```text
AI-Based-Autonomous-Navigation-System/
├── main.py
├── requirements.txt
├── README.md
├── .gitignore
├── src/
│   ├── __init__.py
│   ├── path_planning.py
│   └── simulation.py
├── outputs/
└── screenshots/
```

## Setup on Windows
1. Install Python 3.10+ from https://www.python.org/downloads/ and select **Add Python to PATH** during setup.
2. Extract this ZIP file.
3. Open Command Prompt or the VS Code terminal inside the extracted project folder.
4. Create a virtual environment:
   ```bat
   py -m venv .venv
   ```
5. Activate it:
   ```bat
   .venv\Scripts\activate
   ```
6. Install dependencies:
   ```bat
   python -m pip install --upgrade pip
   pip install -r requirements.txt
   ```
7. Run the project:
   ```bat
   python main.py
   ```

## Setup on macOS / Linux
```bash
python3 -m venv .venv
source .venv/bin/activate
python -m pip install --upgrade pip
pip install -r requirements.txt
python main.py
```

## Controls
- **SPACE** — pause/resume the robot
- **R** — calculate the route again
- **N** — add an obstacle and re-plan the route
- **ESC** — exit

## How it works
1. The environment is represented as a grid.
2. Dark cells are blocked obstacles.
3. A* searches for a low-cost route from the green start to the red destination.
4. The route is drawn in blue.
5. The yellow virtual robot moves along the route.
6. Press **N** to add an obstacle and see the route being recalculated.

## Algorithm
A* chooses the next cell using:

`f(n) = g(n) + h(n)`

- `g(n)` is the cost from the start to the current cell.
- `h(n)` is the Manhattan-distance estimate from the current cell to the goal.
- Movement is allowed up, down, left, and right; diagonal movement is not included.
- <img width="1270" height="700" alt="Screenshot 2026-10-13 152011" src="https://github.com/user-attachments/assets/8dfaaa2a-232b-4ea0-8763-84a1146bd1dd" />

## Troubleshooting
- **`python` is not recognized:** reinstall Python and enable **Add Python to PATH**, or try `py main.py`.
- **`No module named pygame`:** activate `.venv` and run `pip install -r requirements.txt`.
- **Window closes immediately:** launch it from a terminal using `python main.py` so any error remains visible.
- **No route found:** check that the start, destination, and corridors are not blocked.

## Future improvements
- Add OpenCV camera input and computer-vision perception
- Integrate a lightweight object detector
- Add Dijkstra or BFS for algorithm comparison
- Connect to ROS, Webots, Gazebo, or CARLA
- Add logging, automated tests, and performance metrics

## Learning outcomes
- Python modules and functions
- Grid-based environment modelling
- A* search and heuristic functions
- Event loops and visualization with Pygame
- Documenting and publishing a project on GitHub

## Author
Student project — AI-Based Autonomous Navigation System
Github:https://github.com/yaseenkhaleel16-tech/AI-Based-Autonomous-Navigation-System
Linkedin:https://www.linkedin.com/in/yaseen-khaleel-6a535a432/
