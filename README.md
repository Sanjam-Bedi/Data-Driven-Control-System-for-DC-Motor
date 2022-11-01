# Data Driven PID Control System for DC Motor
## Abstract
Aim of the project is to implement the data driven control system to control the speed of a dc motor using a PID controller. In this paper, we have used component based modeling similar to the real dc motor by using a simscape electronics system to obtain the input
voltage and output speed of the dc motor
and system identification toolbox for
obtaining the model of the object. The
transfer function is derived by
performing the system identification
process in time domain data. Using the
acquired transfer function, the PID
controller is tuned using the Matlab
software. Routh stability criterion, root
locus, time domain analysis and
frequency domain analysis of the system
are done using Matlab and the results are
presented in the paper. In the end, the
simulation results of the speed control of
the dc motor are presented.

Keywords— Data driven control system,
System identification, DC motor, pid
controller, Simscape electronics system.
## Introduction
DC Motors has a wide range of applications
in the industry. They are used in home appliances, robot manipulators, toys,
agricultural devices and so on because of
their dynamic characteristics and high
efficiency. However, the speed of the dc
motors need to be controlled. This is due to
the fact that the motor’s load torque varies
due to external factors such as temperature,
humidity and changes over time and thus in
order to keep the motor running at a constant
speed, the speed needs to be controlled. In
order to design the controller, it is necessary
to first design the model. To solve this
problem, data driven control must be used.
Data driven control methods allow tuning a
controller without the need of an identified
model of the system. It is a designed
controller when no plant model is available.
In this case, component based modeling
similar to a real DC motor is used using
simscape electronic systems.
System Identification technique is used to
solve the objective of designing
mathematical models that is based on the
perceived system data. The system
identification toolbox is useful for
representing dynamic systems and ensures
some linear and nonlinear black-box model
structures. In this paper, nonlinear black-box
model structures in the system identification
toolbox have been used for representing the
continuous-time transfer function of the DC
motor. After the transfer function of the
system is estimated, the PID controller
parameters kp, ki and kd are auto tuned
using the pid tuner to achieve the stability of
the system. PID controller design has the
following special features: simple
mathematical modeling, good reliability,
high reliability, stabilization. Therefore, a
PID controller is used for the controller
design.
## Implementation
### Data Driven Control
Nowadays, many industrial processes and
robotic systems have become more complex.
Although the plant model of the systems
might be available, the complexity makes it
difficult to design the controller. In such
cases, data driven modeling can be used. In
this paper, we consider the data driven
control system of DC motor by using system
identification process and implement the
data driven control flow work as shown:
![image](https://user-images.githubusercontent.com/74055483/199232032-391f070e-20ef-4bb8-b29e-bb3b22379085.png)










In this paper, the DC motor is a
hardware part, from which input
voltage and output speed can be
measured. The measured data is used
to operate the system identification
process. And then we get the transfer
function of the plant model from the
system identification process. It is
also important to choose a controller
design for controlling the plant
model. After the modeling, real time
testing of the dc motor can be done.

### DC Motor Using SImscape system.
In this paper, a physical block
diagram of the simscape extension is
used to build the DC motor model.
The main advantage of the simscape
model is the ability to modify the
model quickly without having the
equations of the system.
![image](https://user-images.githubusercontent.com/74055483/199232214-3915aae9-67f7-45e1-a5a2-8409aa7e5728.png)


### System Identification Process
The System Identification Toolbox
provides Matlab functions,
Simulink blocks and interactive
tools for creating dynamic model
systems. In this process, input
and output data is required in the
time domain to identify the
continuous transfer function.
After doing the identification
process, we get the transfer
function with the following
parameterization:

1. Fit to estimation—
[97.93;89.89]% (stability
enforced)

2. FPE— 0.0009793

3. MSE— 0.4767

Transfer Function of the system
is estimated as:

ω(s)/Y(s) = (-0.04965s+0.008474)/(s^2+0.12
2s+0.008696)
### Controller Design
The control signal is a sum of three
components: Kp, Ki and Kd. Kp
depends on the error and is responsible
for the response to the instantaneous
control error. Ki contains the
accumulated control error, which is an
additional source of output power and
allows to achieve the maximum speed
of reaching the setpoint without
overshoot. Kd depends on the rate of
change of the parameter, which causes
the regulator to react to a sharp change
in the measured parameter, which can
be solving an external disturbing effect.
In this paper, a PID controller is used for
the proposed plant model. In order to
correctly regulate the plant model, it is
necessary to tune the coefficients of the
PID controller. The auto tuning method
is used to get the desired response of
the DC motor.
The tuned values are coming as follows:
Kp=0.825, Ki = 0.0423, Kd =2.156
## Authors
- Aryaman : [@Aryaman-Arya](https://github.com/Aryaman-Arya)
- Sanjam Kaur Bedi : [@Sanjam-Bedi](https://github.com/Sanjam-Bedi)


