# Ball-and-Plate
![image](https://user-images.githubusercontent.com/83930919/119288861-4c3bb200-bbfe-11eb-9b98-8bc29e5067f3.png)

California State University of Chico-MECA 482-Spring 2021

## Team Members 
Timothy Bowersox,
Anthony Condos,
Cat De Vito,
Paige Kim,
Frank Silva,

### I. Introduction
A ball and plate system is an example that allows for testing, and control of artificial intelligence algorithms. Two stepper motors control the angle of a plate. Each stepper motor will control the x axis, and y axis of plate motion. Adjustment of the plate position in order to control ball orientation, keeping it balanced on top of the plate is the goal. A controller for the ball and plate system will be designed, mathematical model analysis performed, and a simulation using MATLAB/Simulink for the ball and plate system. 

### II. Modeling
The figure below shows a simplified model of the the ball and plate system parameters:

m=mass of the ball

h=height of the motor arm

r_arm=radius of the motor arm

r=radius of the ball

L=length of the plate

𝛼=angle of the plate

θ=angle of the motor arm

J=moment of inertia of the ball
![image](https://user-images.githubusercontent.com/83930164/119275780-d7e81b00-bbcb-11eb-8777-ae1a42d760dd.png)

  Fig. 1: Ball and Plate Model 

A nonlinear equation of motion is derived from Fig. 1: Ball and Plate Model, above. The equation, seen below uses the geometry of the motor, and the plate. Equation 2, and 3 are derrived to find 𝛼 and θ. Substituting equations 2, and 3 into equation 1 yields equation 4. Taking a small angle approximation, seen in equation 5, and the taking the laplace transform, seen in equation 6, the final transfer function of one motor is found, below in equation 7. 

![eq](https://user-images.githubusercontent.com/83930164/119277033-34e6cf80-bbd2-11eb-9917-9041d22ea9aa.JPG)

### III. Sensor Calibration

### IV. Controller Design and Simulation
Control system block diagram model can be seen below in Fig. 2: Block Diagram. Two system models show each controlling x-axis, and y-axis. 
![image](https://user-images.githubusercontent.com/83930919/119284179-eba77780-bbf3-11eb-980b-37c9ee95ed39.png)

  Fig. 2: Block Diagram.


### V. Simulation Results

### VI. Appendix A: Simulation Code

