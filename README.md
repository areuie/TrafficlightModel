# Traffic Light System

 <img width="468" alt="image" src="https://github.com/areuie/TrafficlightModel/assets/63759859/558d116c-acc8-4760-a006-3dc33cbc8ed7">
![image](https://github.com/areuie/TrafficlightModel/assets/63759859/db87c20e-2390-465a-983a-0309adbd3a39)

## Introduction
This project aims to create a functioning traffic light system with the Arduino circuit.  Its core components include 3 traffic lights at a T-intersection, a pedestrian light, a parking gate, and a street light. The system has a number of decorations: a parking lot, a house, roads, benches, etc. A team of three, Olivia Chan, Alisa Wu, and Leo Farb created this traffic light system to simulate working on a computer engineering project and to learn how to implement significant engineering skills, such as circuitry design, coding, computer-aided design, and model construction. A circuit simulation software called TinkerCAD was used to model the physical circuit system. A 3D design software, SketchUp, was used to design the layout of the system. 

## Explanation
How do the traffic lights work at a T-intersection? On the shorter road, there are two traffic lights facing one another, and the timing of their lights are in sync, since the cars are able to travel in both directions when the lights are green. In the T-intersection, there is another traffic light perpendicular to the other two.
	How does a pedestrian light work? The pedestrian light signals to pedestrians when they are able to cross the crosswalk with two lights: one red and one green. Red indicates the person has to wait, and green tells them when to go. When the traffic lights facing each other are green or yellow (parallel to crosswalk), the pedestrian light is green. When the two traffic lights mentioned are red, the pedestrian light also lights up red due to people being unable to cross the crosswalk when there are cars passing along that road. 
How does a manual switch change the timing of the traffic lights? The manual switch checks what time the button was pressed when receiving input, and if it is switched on when the red light of the single traffic light is on, it speeds up the change for red and yellow, and the green light will stay on longer to allow the person to walk. If pressed when the yellow LED is on, it speeds up the change for yellow and lets green stay on for longer. If pressed when the green light is on, it will speed up the change for the next cycle. 
When will the street lamp be turned on or off? During the day the street lamp will be turned off (when the photoresistor detects a lot of light). When the photoresistor does not detect a lot of light, the street lamp will be turned on in order for people to see at night time. 
How does an ultrasonic sensor work with a gate? The ultrasonic sensor sends and receives ultrasonic waves, which would then be translated into the distance of an object approaching the sensor. When an object or person reaches a certain distance from the gate, it will tell the gate to open - only for a predetermined time period.
How does the IR sensor work with the gate? The IR sensor receives IR signals from the IR remote, and when a button is pressed, it tells the gate to open for a predetermined time period. This is so the parking gate can be controlled remotely. 

## Layout
<img width="335" alt="image" src="https://github.com/areuie/TrafficlightModel/assets/63759859/376f739d-d711-4930-83b2-759573504a0b">

## Challenge
1.	The main challenge we had in creating the traffic light system was the learning curve that came with the first time using SketchUp, TinkerCAD, and coding in C/C++. With no prior knowledge of circuitry, we had to research how certain components worked together in other’s circuits, as well as how they actually functioned. When we came across issues in SketchUp, resources like blogs and YouTube helped greatly. For example, creating the street light was difficult at first, as SketchUp doesn’t have a native sphere tool. By searching online, we found that we can make a semi sphere by using “Follow Me”, which leads a face along a path to create a 3D shape. We also had struggles with making the servo motor to work in TinkerCad, as the remote and ultrasonic distance sensors were conflicting with each other when we tried to open the gate. We fixed the issue by making the gate open for a certain time interval instead of letting the gate open whenever it met the distance requirements. That way, we could control the gate using both the remote and ultrasonic distance sensor.

2.	Another challenge that we had was that after the basic research was completed, troubleshooting the code for the circuit was also tedious due to being unable to find the exact issue we were facing online. However, we were able to overcome this eventually by creating simpler code to test components individually in order to discover the issue in the physical circuit. The traffic lights at the T-intersection, the street lamp, and the gate were fairly easy to troubleshoot in TinkerCAD, but the pedestrian light was a bit more difficult due to having to adjust the timing of the original lights when the input from the button was received. For the circuit, although the components worked individually, there were quite a few instances where they would not function when they were all integrated into the same circuit. This occurred because when multiple components were attached, the values of the input from the sensors were different. 
	
## Investigation - Process & Changes Made
We started the project by planning out the layout and the features, using a 3D design program called Sketchup. We each made a traffic model, so that we had the flexibility to choose what type of layout we wanted. Then we started designing the circuit using TinkerCAD, first making a basic prototype of a traffic light system that only had 3 traffic lights and a street lamp. After, we added more features, such as the pedestrian light, the pedestrian light button, the car gate, and fixing the timing. Now that the planning for the model and the circuit was finished, we then created the physical circuit using the Arduino Uno. We recreated all our features except for the car gate, as we had to refactor the TinkerCAD code to work for the physical model. 
Alisa soldered wires to the LEDs and the pedestrian button, while Olivia fixed circuit issues and helped Leo with making the decorations. Deciding to use Alisa’s traffic model as a base, we drew out the layout onto the board. Olivia added another gate, changed the orientation of the pedestrian crosswalk, changed the shape of the car parking lot, changed the street lamp design and added a house to the Sketchup model. A number of unforeseen changes had to be made in the physical model, since the dimensions were not exactly to scale to the SketchUp model. After creating the box for the traffic light and the house decoration, they were too large for the dimensions of the platform, and had to be scaled down. In addition, once the poles of the traffic light were made, some of the traffic lights blocked the other lights in the T-intersection from certain perspectives, and the poles had to be shortened. A few errors occurred due to faulty LEDs and photoresistors, which were able to be corrected once replaced. Other errors with the circuit occurred due to wires falling off when transporting to and from school.
Using Alisa’s traffic model as a base and adding Olivia’s street lamp design and house model, the final SketchUp model was completed. After the decoration and road design on the physical model was completed, Olivia glued all the circuit components onto the platform, and double checked the connectivity of the LEDs to the circuit. 

## Design Features
-	3 traffic lights, 1 pedestrian light, 1 pedestrian button, 1 street light, 2 gates, 1 gate sensor, 1 house, 1 bench, 1 crosswalk, 1 parking lot
-	Includes pedestrian sidewalks, road curbs, and street lines
  
## Materials
Physical materials:
-	Yellow Folder - Traffic lights, pedestrian light
-	Shoe Box Cardboard - House
-	Straws - Traffic/pedestrian/street light poles, pedestrian button pole, car sensor pole
-	Construction Paper (Green, grey, white) - Grass, sidewalk, curb, street white lines
-	Acrylic (Red, yellow, blue, silver, black, brown) - Traffic light poles (black), pedestrian light poles (silver), street light pole (silver), pedestrian button pole (silver), car sensor pole (black)
-	Popsicle sticks - Bench
-	Foam Board - Project platform, car gate
Technical components:
-	LED Lights (Red, yellow, green, white) - Traffic lights, pedestrian lights, street light
-	IR Sensor, Light Sensor
-	Button
-	Servo motor
-	String (Floss)
-	Resistors
-	Wires
-	Breadboard
-	Arduino Uno

## Evaluation
The project turned out fairly well, as all of the circuit components work as intended in the instructions in TinkerCAD and the physical circuit, and the model looks put together with all of the decorations. In addition, the code is comprehensive and structured in a logical way. 
	If we were to do the project again, doing planning all at once at an earlier time would have been much more beneficial. Since we did not do much planning of when and who we wanted to complete certain components, we finished things based on whatever was still left to do - which used up time in between, as we had to decide who would be completing what after every component, rather than having it all laid out. 
	Specifically, it would have been better to spend less time making decorations, since it is overall a very small portion of the mark. We would have also wanted to finish soldering everything all at once, rather than finishing one component and returning to it later. The main issue was that we did not allocate tasks for group members before starting the assignment, and some people were unsure of what they should be doing at certain points in time. 
Most of the issues laid out here are due to inefficient planning, and next time, we should purchase the materials all at once, and lay out the instructions of what to do with the materials extremely clearly after discussing together as a group. Making decisions independently due to interest of time led to a number of errors which could have been foreseen, as a result of not recuperating with the rest of the group efficiently. 

