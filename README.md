# Ball-and-Plate
![image](https://user-images.githubusercontent.com/83930164/119294730-f79e3400-bc09-11eb-9b45-9e19955e32ee.png)


California State University of Chico-MECA 482-Spring 2021

## Team Members 
Timothy Bowersox,
Anthony Condos,
Cat De Vito,
Paige Kim,
Frank Silva,

### I. Introduction
A ball and plate system is one example in control theory that allows for testing and control of artificial intelligence algorithms. Two stepper or servo motors control the angle of a plate. Each stepper motor will control the x-axis and y-axis of the plates motion. The goal of this system is to keep the ball balanced on the plate by detecting the balls position and sending signals to the motors in order for them to adjust the plates angle. A controller for the ball and plate system will be designed, along with a mathematical model and a simulation using MATLAB/Simulink and coppeliasim. 

### II. Modeling
The figure below shows a simplified model of the the ball and plate system where:

m=mass of the ball

g=gravity

h=height of the motor arm

r_arm=radius of the motor arm

r=radius of the ball

L=length of the plate

𝛼=angle of the plate

θ=angle of the motor arm

J=moment of inertia of the ball

![image](https://user-images.githubusercontent.com/83930164/119293877-2a472d00-bc08-11eb-916d-20e197d3332e.png)

  Figure 1: Ball and Plate Model 

Equation 1 shows a nonlinear equation of motion that is derived from Fig. 1: Ball and Plate Model, above. Using the geometry of the motor and the plate, Equation 2 and 3 are derrived to find 𝛼 and θ. Substituting equations 2, and 3 into equation 1 yields equation 4. Taking a small angle approximation, seen in equation 5, and the laplace transform, seen in equation 6, the final transfer function of one motor is found, seen below in equation 7. 

![eq](https://user-images.githubusercontent.com/83930164/119277033-34e6cf80-bbd2-11eb-9917-9041d22ea9aa.JPG)

### III. Sensor Calibration
<img width="1288" alt="Screen Shot 2021-05-23 at 9 12 38 PM" src="https://user-images.githubusercontent.com/83930770/119295428-aee77a80-bc0b-11eb-9315-0cd2d5aeb999.png">

In the controller architecture below, the outer loop is used to covert the position to angular. The angular position is sent to the inner loop, which controls the postion of the servo motors. Pbb(s), at the end, is the ballplate that is connect to the servo motors. Xd(s) would be the input, which would be the balls postion.

### IV. Controller Design and Simulation
Control system block diagram model can be seen below in Fig. 2: Block Diagram. Two system models show each controlling x-axis, and y-axis. 

![image](https://user-images.githubusercontent.com/83930919/119284179-eba77780-bbf3-11eb-980b-37c9ee95ed39.png)

  Figure 2: Block Diagram.


### V. Simulation Results
Coppelia is used to perform the systems simulation. The code for Coppelia communicates with Matlab to run the simulation. 

![image](https://user-images.githubusercontent.com/83930164/119297569-19021e80-bc10-11eb-93f7-e3f8808cffb6.png)

![image](https://github.com/Pkim10-csuchico/Ball-and-Plate/blob/main/ballandplate1.png)

Figure 3: Ball and plate simulation

### VI. Appendix A: Simulation Code

The below figures show the code for connecting matlab/simulink to copelliasim.

![image](https://user-images.githubusercontent.com/83930164/119306942-c7fa2680-bc1f-11eb-9498-bfbb64d6589e.png)

![image](https://user-images.githubusercontent.com/83930164/119307003-dcd6ba00-bc1f-11eb-9a5a-d4bb2167f9be.png)

![image](https://user-images.githubusercontent.com/83930164/119307028-e3fdc800-bc1f-11eb-885a-45d1a8869545.png)

![image](https://user-images.githubusercontent.com/83930164/119307064-f0822080-bc1f-11eb-97cc-f92193ef87a7.png)

![image](https://user-images.githubusercontent.com/83930164/119307082-f972f200-bc1f-11eb-95e7-5fa2d41a2a7a.png)
