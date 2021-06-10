# Welcome to Jonathan's Website

## 1. Five Degree of Freedom Robot Arm (Using ROS)

<p align="center" >
<img src="https://user-images.githubusercontent.com/54735464/121494705-d40b1580-c98d-11eb-98b2-e2fa5395a0e8.jpg" width="200">  <img src="https://user-images.githubusercontent.com/54735464/121500655-5cd88000-c993-11eb-9beb-002bf45ec35c.jpg" width="200">
</p>

### To Do
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
This was a bit more challenging because the syntax changes
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






## 2. Quadruped Robot

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

### To Do
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
<img src="https://raw.githubusercontent.com/j-505/JonathanFlores.github.io/Webpage/images/2.png" width="200">  <img src="https://raw.githubusercontent.com/j-505/JonathanFlores.github.io/Webpage/images/3.png" width="200">
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


### Contact Info

[Linkedin](https://www.linkedin.com/in/johnflores01/) |
Email: Jonathan.Flores.1962@gmail.com
