# SCARA-Robot-Arm

A SCARA type robot arm with four degrees of freedom


## Abstract
At the time of conception, I had no singular end application for this project, I saw it as a way to develop my skills in various parts of engineering design. 

Upon further consideration, the potential applications of use cases of this robot are quite robust. One that comes to mind is PCB development; specifically with regards to component pick and place. Other applications include CNC milling, 3D printing, laser engraving, process automation for manufacturing, and as much as you can imagine.

This project pushes me to learn new concepts and develop my skills in 3D CAD, Electronic circuit (PCB) design and Embedded software development.
I say this because every aspect of this project involves utilizing or developing skills in the areas listed above.




## Mechanical
### Base
The base of the robot houses a singular stepper motor that creates the first degree of freedom on the robot which rotates the aluminum extrusion mount that the arm will eventually be fixed on. To achieve this, a gear reduction of 15:1 has been implemented.
This is done using a NEMA 17 stepper motor (motor specs here) that drives a compound gear, with 60 and 20 teeth. The output of the stepper motor is directly driving the 60 tooth part of the gear causing a 3:1 gear reduction. The 20 tooth part of the gear then drives the final 100 tooth gear that connects to the output base using a thrust bearing where the aluminum extrusion arm mount will eventually rest upon. This creates a gear ratio of 5:1, which when multiplied by the initial 3:1 reduction gives a total reduction of 15:1.

The part (called turntable) which connects to the final 100 tooth gear to rotates at an angle determined by the two limit switches placed on the top of the base. These switches control the functional angle of the extrusion mount and stop the turntable from spinning continuously which would be very bad for the robot and things around 😅

![base top](https://user-images.githubusercontent.com/78376139/207982161-b029e927-a005-4076-8e5a-98888a343626.png)
![gears](https://user-images.githubusercontent.com/78376139/207982723-a7b1eacc-2b4a-42ea-b8cc-d08c1529a0be.png)

    
     
### Extrusion mount & Linear actuator
The second degree of freedom offers a linear movement.
The arm is mounted to a part that moves along the z-axis. Initially I went for a gantry design but decided to go with a stepper controlled linear rod instead. 
I felt the gantry was too finicky and would require more power to move because of its own weight. The linear rod offers a simpler design, without the need of adding a timing belt like we would with the gantry.

Initial design:
![gantry](https://user-images.githubusercontent.com/78376139/207983213-87784e79-82ee-4f0c-b5af-4b3ef91dc8db.png)

More information on the linear rod and the rest of the project will be released shortly! :)


