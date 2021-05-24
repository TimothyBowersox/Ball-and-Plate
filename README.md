# Ball-and-Plate
California State University of Chico-MECA 482-Spring 2021

## Team Members 
Timothy Bowersox,
Anthony Condos,
Cat De Vito,
Paige Kim,
Frank Silva,

### I. Introduction
A ball and plate system is an example that allows testing, and control of artificial intelligence algorithms. Two stepper motors controlling the angle of a plate. Each stepper motor will be used for the x axis, and y axis of plate motion. Adjustment of the plate position in order to control ball orientation, keeping it balanced on top of the plate is the goal. A controller for the ball-and-plate system will be designed, mathematical model analysis performed, and a simulation using MATLAB/Simulink for the ball and plate system. 

### II. Modeling
The figure below shows a simplified model of the the ball and plate system where:

m=mass of the ball

h=height of the motor arm

r_arm=radius of the motor arm

r=radius of the ball

L=length of the plate

𝛼=angle of the plate

θ=angle of the motor arm

J=moment of inertia of the ball
![image](https://user-images.githubusercontent.com/83930164/119275780-d7e81b00-bbcb-11eb-8777-ae1a42d760dd.png)

A nonlinear equation of motion is derived from the figure above and can be seen below in equation 1. Using the geometry of the motor and the plate, equation 2 and 3 are derrived to find 𝛼 and θ. Substituting equations 2 and 3 into equation 1 yields equation 4. Taking a small angle approximation, seen in equation 5, and the taking the laplace transform, seen in equation 6, the final transfer function of one motor is found, seen in equation 7. 

![eq](https://user-images.githubusercontent.com/83930164/119277033-34e6cf80-bbd2-11eb-9917-9041d22ea9aa.JPG)

### III. Sensor Calibration

### IV. Controller Design and Simulation

### V. Simulation Results

### VI. Appendix A: Simulation Code

### VII. Appendix B: MATLAB Code

%%Transfer functions for motors%%
m=
x=
g=
alpha=
theta=
J=
r=
h=
L=
r_arm=


%%Equation derived from diagram%%
mx= m*g*sin(alpha)-J*x/x^2
sin(alpha)=2*h/L 
sin(theta) = h/r_arm

%%Non Linear equation of motion%%
X*(m+(J/r^2)) = 2*m*g*r_arm*sin(theta)/L 

%%Linearized Equation of motion%%
X*(m*(J/r^2)) = (2*m*g*h/L)*theta(s)

%%Transfer Function%%
X(s)/theta(s) = 2*m*g*h/(s^2*L(m+(J/r^2)))


Second Order Underdamped System Transfer Function%%
omega=
s=
zeta=

%%Transfer Function%%
Y(s)/R(s) = omega^2/(s^2+2*zeta*omega*s+omega^2)


