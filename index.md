# Welcome to my personal website

<p align="center" >
<img src="https://github.com/j-505/JonathanFlores.github.io/blob/Webpage/images/Professional-Picture.jpg?raw=true" width="300">
</p>

Hello, I'm Jonathan Flores.
As a mechatronics engineer I have a strong passion for
designing and building unique hardware. I love to learn
and apply new concepts and am eager to pursue innovation.

If you have any questions, feel free to contact me.
My contact information is on the bottom of the page.

Enjoy!

# Personal Projects:


## 1. Gearbox Design Competition (1st Place)

<p align="center" >
<img src="https://user-images.githubusercontent.com/54735464/121645957-a4214800-ca49-11eb-9b8d-0abf2e0ba9c1.jpg" width="300">
</p>
<p align = "center">
 Special Thanks to
</p>
<p align = "center">
 Professor Nurullah, ME 2030-09 peers and makerspace staff
</p>
### Objective
The purpose of this report is to manufacture an efficient gearbox that improves on 
the characteristic of insufficient power corresponding to the torque and velocity of 
the source. In accordance to the design process in mechanical design, this project
undertakes multiple phases that correspond to the motion and power transmission 
in a gearbox system.

### Design Report

I think it would take some time to go through the whole project on this page.
So here is the <a href="./images/GearboxReport.pdf">downloadable report</a> for the project.
<p align="center" >
<img src="https://user-images.githubusercontent.com/54735464/121646354-1560fb00-ca4a-11eb-96c4-90c2fb46d262.jpg" width="400">
</p>



### Conclusion

<p align="center" >
<img src="https://user-images.githubusercontent.com/54735464/121646336-1134dd80-ca4a-11eb-9711-3c1656dbe8c4.jpg" width="200">
</p>

The time performances of the gearbox with a gear ratio of 15.2 was higher than 
determined from the calculations. The team suspected this was caused by an 
irregularity, where the teeth of the gears did not fully mesh together. 
Possible reasons are the calibration of the laser cutting machine and the 
number of cutting cycles applied to the acrylic glass that would deform 
its shape. Overall, the team was satisfied with the final test performance 
time of 5.66 seconds.

## 2. Five Degree of Freedom Robot Arm (ROS)

<div style="text-align: center;">
  <img src="https://github.com/j-505/JonathanFlores.github.io/assets/54735464/4f032af3-840b-4434-ac50-6a2fa72476ed" alt="5DOF_Red_Arm (1)" width="100" height="300">
</div>

<p align="center" >
The objective of this robotic arm was initially just to see if I
could design and learn how to program one. I soon went down a
rabbit hole and wanted to program one to move and pickup an object
using object detection! In this example I will only be showing how I
went about designing and controlling the robotic arm without Computer vision.
Adding the object detection is one of the main goals I am currently trying to achieve. 
</p>

Key Hardware:
<ul>
<li>x4 - 20kgcm Servo Motor </li>
<li>x2 - SG90 Servo Motor </li>
<li>x1 - Benchtop Power Supply</li>
<li>x1 - Arduino Uno  </li>
<li>x1 - Jetson Nano  </li>  
<li>Access to 3D printer/ Filament </li>    
</ul>

### Objectives
1. Design files for 5DOF robot using Solidworks.
2. 3D print and Assemble Parts.
3. Flash and install ROS/Moveit plugin on Jetson Nano.
4. Create and upload Arduino sketch to Robot.

### Design

I did not want to spend my money on purchasing a robotic arm
from online so I decided to design and built my own. 
I plan on putting this design on thingverse once I'm done with the full design.

### Programming/Testing
The main programming will be written onto a arduino microcontroller. 
 We will also be using the Jetson Nano to speak to the arduino microcontroller. 
 The Jetson nano runs on Linux. We are using it because Linux will
 allow us to install ROS and ultimately MoveIt! which will allow us to 
 control the robotic arm using inverse kinematic solvers. ROS also has
 existing packages that I will be using in the future for object detection.

I've written arduino code for a 2 Wheel drive arduino robot
 that allowed me to control individual dc motors using
 the H-bridge motor driver. 
This was a bit more challenging because the layout
 changes when using Servo motors and ROS. Addressing the arduino and
 servo motors are interpreted in terms of subscribing
 and publishing to topics and nodes. The serial
 node (ROS node for arduino interfacing) will basically
 be subcribing to the 5 servo topics so that when it
 is subscribed to some angle the arduino will write
 that particular value to the pwm pin of the motors.
 So if we are publishing some value to the ROS topics
 the servos will move. Modifying the code to have different
 switch cases will allow all the robotic servos to move
 in tandem to provide a forward, backward, left & right movement.



## 3. Quadruped Robot

<p align="center" >
<img src="https://raw.githubusercontent.com/j-505/JonathanFlores.github.io/Webpage/images/1.png" width="300"> 
</p>

I worked on this project for my circuits analysis course.
It was the final project for the course and the objective
was to design and program a robot using arduino and then 
present your project so that students could follow along.

I had some prior knowledge before this project that involved
controlling a servo motor arm using ROS and decided that it 
would be pretty neat if I could create a robotic dog like the
Boston Dynamics spot robot.

Hardware:
<ul>
<li>x5 - SG90 Servo motor</li>
<li>x1 - Arduino Uno</li>
<li>x1 - L298N Motor Driver</li>
<li>x1 - 9V Battery</li>
<li>x1 - Breadboard</li>
<li>Access to 3D printer/ Filament  </li>
</ul>

### Objectives
1. Design solidworks model.
2. 3D print and Assemble Parts.
3. Create an application on MIT App Inventor.
4. Create and upload Arduino sketch to Robot.

### Design

The robot was designed using solidworks and 3D printed on a anycubic viper 3D printer.
This design was quickly put together because I honestly did not have enough time left and I needed to figure out how to go about  programming the actual robotic joints to move with my phone. One important thing that stood out on this robot was
how important it is to add a material that allows the end effector to grip the surface just enough
to the ground so that it provides enough force in the correct direction.

### Programming/Testing
The way this robot moves is by sending direction commands from a phone application via bluetooth module to the arduino microcontroller. The microcontroller then sends angle commands to the servos on each leg. This creates a walking gait in the direction needed so thatthe robot can move.

<p align="center" >
<img src="https://raw.githubusercontent.com/j-505/JonathanFlores.github.io/Webpage/images/2.png" width="300">  <img src="https://raw.githubusercontent.com/j-505/JonathanFlores.github.io/Webpage/images/3.png" width="300">
</p>

I designed the mobile application on the MIT app inventor website and created a button for each movement (Forward, Backward, etc).
Each button connects to the arduino codes use cases (1,2,3,4,5).
This is what distinguishes the different movements in the robot.
The important thing here is to add a bluetoothclient to the application
so that you're able to locate your robots bluetooth module on your phone.
When testing the code on the robot there is some latency but the overall movement in any given direction is shown.

The Code for this project is on my github.

I am currently working on a better version of this using 12 servo motors
I'll keep updating this page.

## 4. SENIOR DESIGN PROJECT - Refurbishing 6DOF Robotic Arm
<div style="text-align: center;">
  <img src="https://github.com/j-505/JonathanFlores.github.io/assets/54735464/0e46356c-40b9-4adb-9492-bd8441a0fe70" alt="20210910_144129" width="250" height="300">
</div>
This robotic arm had essentially been sitting inside my professors lab and instead of designiing one he wanted us to get this arm up and running and incorporate it into our "University Mars Rover Competition" senior design project. There was a lot of troubleshooting done on the DC motors, Belts and harness that we needed to do so a large portion of the project was dedicated to this and procurement of parts. We were able to eventually get it working. 
More information can be found here:
<a href = "https://github.com/ASME-ground-robot/2021-22"> Senior Design Project </a>

My tasks were to troubleshoot the robotic arm to see what parts we would need to procure. I was also in charge of redesigning the arm on solidworks so that we could have a representation of it. We would ultimately use this model to generate a URDF model that we could import onto the Jetson TX2. Finally I wrote the Arduino code used to control all 6 DC motors. This was controlled the exact same way as the previous project I showed. The different here is that we're using DC motors with encoders instead of servo motors. This meant that PID's would need to be implemented to accurately control the position of the robotic arm. Gear ratio's would also need to be taken into account for the base and translate that into the amount of encoder ticks for accurate position. One key component that we did not have time to implement was adding limit switches and boundary boxes onto RVIZ that prevent the arm from surpassing its own ROM.


## 5. Quadruped Robot (In progress)

This project is still in progress and I will be sharing different iterations of the designs, simulations and code.

### Objectives

1. Design lightweight and functional robotic leg

### Design

The following image is the second iteration of this robotic quadruped that I designed. T

<p align="center" >
<img src= "https://raw.githubusercontent.com/j-505/JonathanFlores.github.io/Webpage/images/RobotDog.jpg" width="250"> 
</p>
The following is the latest iteration of the quadruped leg. This design is much lighter than the previous leg design.

<div style="text-align: center;">
  <img src="https://github.com/j-505/JonathanFlores.github.io/assets/54735464/531fd59c-e578-4229-b4de-388a00901385" alt="Quadruped leg v3" width="150" height="200">
</div>

### Programming/Testing
I went ahead and attempted to create the URDF for the robot so that I could test it in a simulated environment called Rviz. I need to do
more research so that the coordinate axis and origin positions are correctly imported onto Rviz. It is likey that Moveit/Rviz can only simulate the arms moving and not physically movign the entire robot. There is another program called Pybullet that researchers are currently using to move their quadruped robots and I might have to switch over to this simulation software. More to come! 
<p align="center" >
<img src="https://user-images.githubusercontent.com/54735464/121630450-079f7b80-ca32-11eb-8644-c9f932d7f805.png" width="400"> 
</p>

The following images are the testing setups for the quadruped leg design of both version 2 (Left image) & 3 (Right image). I am currently still working on testing v3. 
<p align = "center">
  <img src="https://user-images.githubusercontent.com/54735464/122987714-c1adb600-d355-11eb-8577-d53a93b96b55.jpg" width="160" />  
  <img src="https://github.com/j-505/JonathanFlores.github.io/assets/54735464/7812cd09-e7de-4b07-80b5-7515e3d661da" width="160" /> 
</p>

## My Etsy Page!
<a href = "https://www.etsy.com/shop/Joeflow3D?ref=seller-platform-mcnav"> Solidworks Model Store</a>

### Contact Info

[Linkedin](https://www.linkedin.com/in/johnflores01/) |
Email: Jonathan.flores.9011@gmail.com
