# quadsim
Beihang University's "Comprehensive Experiment on Modeling and Simulation of Quadcopter Aircraft" provides two ways of MATLAB APP operation and script operation to realize quadcopter control simulation. Simulation functions: fixed-point hover, en-route tracking, formation flight.

Three-plane "one" formation route tracking:

![exp3](https://raw.githubusercontent.com/Amos-Chen98/Image_bed/main/2022/20220425165553.gif)

Three-machine circular formation around points of interest:


![exp4](https://raw.githubusercontent.com/Amos-Chen98/Image_bed/main/2022/20220425165640.gif)

## Experimental content

1. Quadcopter modeling: Establish a quadcopter flight model in Simulink, which can correctly simulate the linear motion and angular motion of the aircraft under the action of force and torque in 6DOF;
2. Fixed-point hover control experiment: based on the quadcopter model, hover control of specified 3D space points is realized; Establish a GUI interface, which can input parameters for the quadcopter and observe the simulated flight trajectory; Analysis of control errors; Improve the control algorithm and improve the control accuracy when possible;
3. En-route tracking control experiment: based on the quadcopter model, the specified 3D space route is tracked arbitrarily; Realize GUI interface, can interactively input a set of waypoints, and draw 3D flight trajectory analysis control error; Improve the control algorithm and improve the control accuracy when possible
4. Formation tracking control experiment: based on the quadcopter model, establish a three-plane linear and circular formation, and fly in formation along the specified path; It is required to implement the GUI interface, draw the formation flight trajectory, and analyze the control error; Improve the control algorithm and improve the control accuracy when possible.

## How to run

There are two ways to run simulations:

1.APP Operation mode: Run QuadSim.mlapp to open the GUI interface, and then you can enter the simulation parameters and obtain the output in the GUI interface. The GUI interface is relatively beautiful, but it is limited by the interface format and the output information is limited.
2. Script operation mode: There are four parallel .m script files, corresponding to four experiments, the function is to load parameters into the workspace, run Simulink simulation, and output detailed simulation results.

![image-20220425170230834](https://raw.githubusercontent.com/Amos-Chen98/Image_bed/main/2022/20220425170230.png)

In the 3Dplot_fcns folder are functions for drawing 3D animations (below), which are called when the app is running (in Experiments 1 and 2). Since this function runs slowly, the dynamic renderings of Experiments 3 and 4 are implemented by the dynamic drawing code written by me.

![image-20220424233237792](https://raw.githubusercontent.com/Amos-Chen98/Image_bed/main/2022/20220424233237.png)

Due to the large number of controller parameters, all parameters are not listed in the experimental report, and the specific values of all parameters can be viewed in the script file. Unless otherwise specified, all position coordinates are in the north-east-geo coordinate system.



