# Welcome to Jonathan's Website

Hello, I'm Jonathan Flores.
Welcome to my personal page!
I'm an incoming 4th year mechanical engineering student
with a focus on hardware and robotics engineering
at California State University, Los angeles.
This is where I will be uploading some of the projects
I have been working on. I'm looking forward to growing
my design and programming skills to build huge meaningful
projects. 

If you have any questions, feel free to contact me.
My contact information is on the bottom of the page.

I hope you like some of the projects I have below! Enjoy!



# Project:


## 1. Gearbox Design Competition (1st Place)

<p align="center" >
<img src="https://github.com/j-505/JonathanFlores.github.io/blob/Webpage/images/Gearbox1.jpg" width="300">
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
<img src="https://github.com/j-505/JonathanFlores.github.io/blob/Webpage/images/Gearbox3.jpg" width="300">
</p>



### Conclusion

<p align="center" >
<img src="https://github.com/j-505/JonathanFlores.github.io/blob/Webpage/images/Gearbox2.jpg" width="300">
</p>

The time performances of the gearbox with a gear ratio of 15.2 was higher than 
determined from the calculations. The team suspected this was caused by an 
irregularity, where the teeth of the gears didnot fully mesh together. 
Possible reasons arethe calibration of the laser cutting machine and the 
number of cutting cycles applied to the acrylic glassthat would deform 
its shape. Overall, the team was satisfied with the final test performance 
time of 5.66 seconds






## 2. Five Degree of Freedom Robot Arm (ROS)

<p align="center" >
<img src="https://user-images.githubusercontent.com/54735464/121494705-d40b1580-c98d-11eb-98b2-e2fa5395a0e8.jpg" width="200">  <img src="https://user-images.githubusercontent.com/54735464/121500655-5cd88000-c993-11eb-9beb-002bf45ec35c.jpg" width="200">
</p>

Hardware:
<ul>
<li>x5 - MG90 Servo Motor (And attachments)</li>
<li>x1 - Breadboard</li>
<li>x1 - Arduino board connector</li>
<li>x1 - Arduino Uno  </li>
<li>x20 - Jumper Cables </li>  
<li>Access to 3D printer/ Filament </li>    
<li>Acess to Computer</li>
</ul>

### Objectives
1. Get CAD design files for 5DOF robot.
2. 3D print and Assemble Parts.
3. Download ROS melodic on Linux VM.
4. Create and upload Arduino sketch to Robot.

### Design

```markdown
The solidworks files were taken from thingiverse.
The link to the thingiverse CAD files is:
[5DOF CAD](https://www.thingiverse.com/make:702244)

Some of the parts originally did not mesh well together 
 because of the support filling.
Removing the support filling from the thin parts also 
 broke some of the pieces.
I had to print them again and remove the filling.
```
### Programming/Testing
```markdown
I've written code for arduino robots that allowed me to 
 control individual sg90 servo motors and dc motors using
 the H-bridge motor driver. 
This was a bit more challenging because the layout changes
 when using ROS. Addressing the arduino and servo motors are
 iterpretted in terms of subscribing and publishing to topics
 and nodes. The serial node (ROS node for arduino interfacing)
 will basically be subcribing to the 5 servo topics so that when it
 is subscribed to some angle the arduino will write that 
 particular value to the pwm pin of the motors. So if we are
 publishing some value to the ROS topics they will move.
Modifying the code to have different use cases in the loops
 will allow all the robots servos to move in tandem to provide
 the desired movement.
```






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
<li>x5 - SG90 Servo motor (and attachments)</li>
<li>x25 - Jumper Cables</li>
<li>x1 - Arduino Uno</li>
<li>x1 - L298N Motor Driver</li>
<li>x1 - 9V Battery</li>
<li>x1 - Breadboard</li>
<li>Access to 3D printer/ Filament  </li>
<li> Acess to Computer</li>
</ul>

### Objectives
1. Design solidworks model.
2. 3D print and Assemble Parts.
3. Create an application on MIT App Inventor.
4. Create and upload Arduino sketch to Robot.

### Design

```markdown
The design for the robot was catered to rapid prototyping.
The robot was designed using solidworks and I might add the 
stl files later on if you would like.

I designed the robot so that all the components could sit on
top of the it and built in some nodes on top of base of the 
robot so that components wouldn't slide. 

The way it moves is by turning the different servos on each
leg a certain angle that creates a forward walking gait so that
the robot can move. I had to redesign some of the legs a couple
of times but finally settled on a design.

The project is a prototype and I will continue working on it.

```
### Programming/Testing
```markdown
I wanted to try and implement the code for the robot just like
I had done for the robot arm since I already had a basic 
understanding of what each servo motor needed to do. 

The difference here is that 
1. This robot was not controlled using ROS
2. I wanted the quadruped robot to be controlled using a phone. 

This meant that the code would be easier to understand for me and 
that I needed to create an application on a phone that would 
move my robot.
```
<p align="center" >
<img src="https://raw.githubusercontent.com/j-505/JonathanFlores.github.io/Webpage/images/2.png" width="300">  <img src="https://raw.githubusercontent.com/j-505/JonathanFlores.github.io/Webpage/images/3.png" width="300">
</p>

```markdown
I designed the application on the MIT app inventor website and
created a button for each movement (Forward, Backward, etc).
Each button connects to the arduino codes use cases (1,2,3,4,5).
This is what distinguishes the different movements in the robot.
The important thing here is to add a bluetoothclient to the application
so that you're able to locate your robots bluetooth module on your phone.
Testing the robot was really fun because I was able to make the quadruped
robot gallop. One thing I would fix on this design is to add some 
rubber to the legs so that it has more friction allowing it to
grasp the floor and move better.

The Code for this project is on my github.

I am currently working on a better version of this using 12 servo motors
I'll keep updating this page.
```


## 4. Quadruped Dog Robot

<p align="center" >
<img src= "https://raw.githubusercontent.com/j-505/JonathanFlores.github.io/Webpage/images/RobotDog.jpg" width="400"> 
</p>

This project is still in progress and I will be sharing 
different iterations of the designs, simulations and code.

Hardware:
(P.S.A: This is not all the components needed!)
<ul>
<li>x12 - 20KGcm Digital Servo (And attachments)</li>
<li>x1 - Breadboard</li>
<li>x1 - Arduino board connector</li>
<li>x1 - Arduino Uno  </li>
<li>? - Jumper Cables </li>  
<li>Access to 3D printer/ Filament </li>    
<li>Acess to Computer</li>
</ul>

### Objectives

In Progress...

### Design

```markdown
I have 3D printed the design for the robot and I've
noticed that the legs are really heavy. So I will be redesigning the 
project to take off the weight. The servo's can probably handle the 
weight but I don't want to risk them overheating and getting damaged.
They were around $18 each! >.<

I'll update the page once I have everything sorted.
```
### Programming/Testing

<p align="center" >
<img src="https://user-images.githubusercontent.com/54735464/121630450-079f7b80-ca32-11eb-8644-c9f932d7f805.png" width="400"> 
</p>

```markdown
I went ahead and attempted to create the urdf for the robot so that
I can test it in a simulated environment. I need to do more research 
so that the meshes and origin positions are correctly imported onto
Rviz.

Again, I'll update the page once I have everything sorted.

See you soon!
```








### Contact Info

[Linkedin](https://www.linkedin.com/in/johnflores01/) |
Email: Jflor288@calstatela.edu
