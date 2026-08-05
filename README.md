# RT2 Assignment 2 – Jupyter Notebook Package

This package contains a **Jupyter Notebook** interface used to control the robot in the Gazebo environment.  
In the action package, the user interface is only a command-line interface, where the user can start or stop the robot.  
In this package, however, the interface is graphical and is implemented using Jupyter Notebook. It allows the user to start and stop the robot, control its movement in different directions, and analyze different plots related to the robot’s state.

## Jupyter Notebook Description

The Jupyter Notebook consists of several buttons and plots for controlling the robot and displaying analysis data of the robot’s state. The available controls and visualizations are described below.

### Start, Stop, Forward, Backward, Left, Right Buttons

<img src="https://github.com/mbugti/RT2_Assignment2/blob/main/imgs/154955314-6963db8c-23d2-49e4-811a-2452e962a76c.jpg" >

These buttons are used to manually start and stop the robot. The robot can also be controlled in different directions using the **Forward**, **Backward**, **Left**, and **Right** buttons. These buttons act as a client service, sending requests to the state machine through the `/user_interface` node.

### Robot’s Moving Position in Real Time

<img src="https://github.com/mbugti/RT2_Assignment2/blob/main/imgs/154955780-9474e2e9-7205-48a8-a9d6-31f4c7c4ab6a.jpg" >

This is a live plot that shows the real-time state of the robot. It is an **x-y** plot used to visualize the position of the robot and the path it follows in the Gazebo environment. A diamond-shaped black line shows the movement of the robot.

### Velocity Visualization Plot

<img src="https://github.com/mbugti/RT2_Assignment2/blob/main/imgs/154956187-c5c24725-6045-499d-8544-8cb020882c2d.jpg" >
<img src="https://github.com/mbugti/RT2_Assignment2/blob/main/imgs/154957806-3044a32b-0ba2-490a-8863-b9f7fdbf1c4c.jpg" >
<img src="https://github.com/mbugti/RT2_Assignment2/blob/main/imgs/154956251-a9522580-93a5-4e4a-8cb1-444f4b790fdc.jpg" >

This plot helps visualize **cmd_vel** against **odom** (actual velocity). It shows both linear and angular components.

### Bar Plot

<img src="https://github.com/mbugti/RT2_Assignment2/blob/main/imgs/154956539-3706afeb-484f-4db5-8399-a2c252391a55.jpg" >

The bar plot shows the number of targets reached and the number of targets cancelled by the user.

### Histogram Plot

<img src="https://github.com/mbugti/RT2_Assignment2/blob/main/imgs/154956810-0b0ae5db-65ec-4cbd-af07-1082146131b8.jpg" >

The histogram plot shows the time taken by the robot to reach the target after the goal is achieved.

## Running the Package

### 1. Launch the simulation
In the first terminal tab, run the command below to launch the simulation and all the required nodes:

```bash
roslaunch rt2_assignment1 sim.launch
```

### 2. Open Jupyter Notebook
In the second terminal tab, run the command below to open Jupyter Notebook:

```bash
jupyter notebook --allow-root
```

### 3. Open the notebook
Open the notebook named:

```bash
jupyter_4904540.ipynb
```

### 4. Run the notebook
Execute the notebook cells to start the interface and control the robot.

## Simulation

<img src="https://github.com/mbugti/RT2_Assignment2/blob/main/imgs/Screenshot_2023-06-22_18-02-40.png ">
<img src="https://github.com/mbugti/RT2_Assignment2/blob/main/imgs/Screenshot_2023-06-22_18-04-09.png ">

## Notes

- Make sure the ROS workspace is built before running the package.
- Source the workspace before launching the simulation or opening Jupyter Notebook.
- The notebook interface should be used after the simulation is running.
