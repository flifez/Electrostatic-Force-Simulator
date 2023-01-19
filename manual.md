# Simulator
_Graph version: Jan. 19, 2023_  
_The information might be outdated._

## Introduction
This is a Desmos graph that simulates the motion of a charged particle in an electric field.  
Some of the parameters could be confusing, so here is a manual explaining them.  

## Point and Control
There are few types of points in the simulator.  
1. Automonous particle (**red**)  
As its name suggests, this point is the main focus of this simulator. Upon starting the simulation, the point will move in the XY plane and leave a trace (trajectory) after it.  
The point _can be clicked_ to reset the simulation. Or, "R_{all}" action can also reset everything at once.  
Please notice that these points cannot be dragged.  
2. Non-autonomous Points (**blue, purple, black**)  
Blue points are _control points_. Currently there are 2 blue points, one of which controls the initial velocity vector "I_V", another controls the initial position of the only automonous particle now (the charged particle).
After moving the blue points, it is required to reset the graph using either "R_{all}" or clicking the red point.  
Purple and black points are electric charges. They cannot move by themselves, and have the main function to generate electric field for the red particle to interact with.  
Purple charges can attract the red particle, while black ones cannot. This is because in the simulator, if the charges are not charged (please excuse this imprecise expression), they automatically turn black.  
When the simulation is ongoing, the purple charges can be moved anywhere to interact with the red particle.  

Also, there are something to control the simulation.
1. Timescale  
To match the elapsed time of the simulation with real life situations, a variable "o" is introduced to scale the time.  
2. Definition and resolution of the trajectory  
Variables "d" and "t" controls the definition and resolution of the trajectory, which have a great impact on the performance.  
The larger the value of "t", the closer two adjacent sampling points (distance = 10^{-t}).  
The larger the value of "d", the more accurate the location of the sampling point (taking d decimal places).  
3. Trajectory length  
To prevent lagging, the parameter "l_{im}" is introduced with a default value of 1000. If the trajectory length (i.e. the number of sampled points) reached this value, the first half of the sampled points will be removed, causing the first half of the trajectory to disappear.  
This allows more sample points (again, half of the set value) to enter the trajectory.  
4. Experimental features  
They are highly experimental features and may be removed at any time. To use them, set the value of "E_{xp}" to 1.  
Currently, the experimental feature _"Adaptive velocity color"_ is being tested and improved.

## Usage
1. Open the graph, set the initial values for the points, and set parameters.  
2. Enable the ticker.  
3. After the simulation, reset the graph.
