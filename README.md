# em-simulation

Simple Electromagnetic Field Simulation
This repository contains a simple C++ program to simulate electromagnetic fields using the finite difference time domain (FDTD) method. The program initializes an electric field pulse in the middle of a one-dimensional grid and updates the electric (E) and magnetic (H) fields over time.

Overview
The code simulates the propagation of an electromagnetic wave in a one-dimensional space. It uses a simple finite difference scheme to update the E and H fields over a specified number of time steps.

Code Explanation
The main components of the code are:

Constants:

dt: Time step (in seconds)
dx: Space step (in meters)
grid_size: Number of grid points
steps: Number of time steps to simulate
Functions:

updateFields: Updates the E and H fields using finite difference equations.
Main Function:

Initializes the E and H fields.
Sets up an initial pulse in the E field.
Iterates over the specified number of time steps to update and print the fields.
Usage
To compile and run the code, use the following commands in your terminal:

sh
Copy code
g++ -o em_simulation main.cpp
./em_simulation
Example Output
The program prints the E and H fields at each time step. Here is an example of the output for 10 time steps:

yaml
Copy code
Time step 0:
E field: 0 0 0 ... 1.0 ... 0 0 0 
H field: 0 0 0 ... 0 0 0 

Time step 1:
E field: 0 0 0 ... 0.999 ... 0 0 0 
H field: 0 0 0 ... 0.001 ... 0 0 0 

...

Time step 9:
E field: 0 0 0 ... 0.91 ... 0 0 0 
H field: 0 0 0 ... 0.089 ... 0 0 0 
Future Improvements
Extend the simulation to two or three dimensions.
Implement absorbing boundary conditions.
Add visualization of the fields over time.
Optimize performance for larger grid sizes and more time steps.
