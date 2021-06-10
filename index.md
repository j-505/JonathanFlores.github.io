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


### Contact Info

[Linkedin](https://www.linkedin.com/in/johnflores01/)
Email: Jonathan.Flores.1962@gmail.com
