---
title: User Needs and Benchmarking
---


## Expert User Interview

* **Interviewee:** Rajdeep Adak
* **Credentials:** PhD candidate - Robotics, Control Systems, Advanced Manufacturing
* **Format:** In person
* **Date:** 9-14-26

---

## Questions Asked & Responses

**Q1. What's your experience with grippers or force/pressure sensors?**  
Worked on both grippers and force/pressure sensors in industry and research environments.

**Q2. What's the most common failure mode you've seen in grip force sensors (drift, noise, wear)?**  
The most common issue is a lack of feedback about the object being gripped, especially since objects vary in shape and must be oriented correctly. This comes down to dexterity and the lack of adequate feedback.

**Q3. What sensing method would you recommend (FSR, strain gauge, load cell) and why?**  
Dynamic touch arrays are the most common sensing method used for robotic hands, and most industrial robotic hands use them.

**Q4. How do you handle sensor drift or calibration over time?**  
For long-term reliability, industry often avoids force sensors altogether and instead hard-codes robotic tasks for example, an object placed in the same position on an assembly line, where the robot moves to known Cartesian coordinates and closes its gripper by a known amount. For our application, long-term reliability (over hours or days) is not a major concern.

**Q5. How do you detect whether a grasp failed due to a sensor fault vs. an actuator fault?**  
Actuator faults are highly dependent on the grasping algorithm, if the algorithm is faulty, the actuator is likely to fail as a result. Gripping an object with the right amount of force can't be treated as a binary outcome, sensing has to be precise. Sensors typically fail when there's a lack of a controlled environment.

**Q6. What wiring/connector issues have you seen at moving joints?**  
As joints rotate, wires and connectors must not interfere with the joint's motion or be affected by it. Rolling contact joints are common in industry and are used to minimize wiring issues at joints that must rotate precisely. Whatever challenges humans face with gripping, you must consider when building a sensor.

**Q7. What's a good control strategy for grasping objects of varying stiffness?**  
Model-based control does not perform well for this. An adaptive control strategy is needed, one that can adjust as the object is pressed and react to sensor input in real time.

**Q8. What environmental factors (dust, temp, vibration) cause the most problems?**  
Vibration causes the most problems. Temperature is also a factor for IMU-based sensors. The biggest challenge in this research has been deterministic feedback, or whether an object is grasped the exact same way each time it's grabbed again. Initial conditions also matter significantly. Some objects that need to be grasped are often aligned differently every time your end-effector is going to pick them up.

**Q9. What's the biggest sourcing/cost/assembly headache with force sensors?**  
Cost is a major challenge, industrial-grade force sensors start at a minimum of about $2,000 each, which is difficult for research budgets. Assembly of the sensors themselves is not too difficult but integrating them with the robotics system is a significant challenge, especially for less experienced students and researchers.

---

## Voice of the Customer Benchmarking Example

### Search #1

**Keywords:** "robot gripper kit"

**Search Results Link:** [https://www.amazon.com/s?k=robot+gripper+kit](https://www.amazon.com/s?k=robot+gripper+kit)

### Selected Products

#### 1. [Mechanical Robot Arm Claw/Gripper Robot Gripper (Black Mechanical Claw Without servo)](https://a.co/d/09uhPVCP)

![Mechanical Claw](image/MechanicalClaw.avif)
* Price: $16.99

* Vendor: Amazon

* Description: Specification
If you want to test the Robotic Claw directly, please use a servo tester. (ASIN: B07485M6PH) <br>
Note: If the Claw(with servo) has any problem or servo missing, please come to us and we will solve it for you.<br>
Please keep your fingers away from the Claw from getting hurt.<br>
Close & Open Range: 0 - 7.62in/193.5mm<br>
Max Grab Weight: 1.54LB / 700g<br>
<br>
Wrap-around Pick-up<br>
The wrapping area of the mechanical claw is large, and the wrapping grabbing makes it more stable when picking up items
<br>
<br>
Metal and Fiberglass Materials<br>
The mechanical claw is made of hard aluminum alloy and glass fiber material, which is beautiful and compact.
<br>
<br>
Large Contact Surface<br>
The inner edge of the claw adopts a wavy design, the contact area of the jaw is large, and the grip is more stable when picking items
<br>
<br>
Mounting Holes<br>
The claw is equipped with multiple M2 and M3 holes, which is convenient for DIY expansion.
<br>
<br>
Easy to Control<br>
Through the servo tester, the steering gear can be controlled to quickly test the claws.
<br>
<br>
Unlimited Creativity<br>
Claws can be widely used in other products such as robotic arms and trolley chassis.
<br>

##### Positive Comments

| Voice of the Customer | Restated Customer Need                                                              |
| --- | --- |
| This is a well-designed and useful gripper for grabbing a wiffle-ball, 2” cube or similar-size objects. It can be ordered with or without a servo. This can be put right on your prototype or spark your creativity for a custom design. It comes with additional screws.| 1. NEEDS HERE |
| Good quality materials. | 2. NEEDS HERE |
| NOTE: NO OTHER USEFUL REVIEWS | |

##### Negative Comments

| Voice of the Customer | Restated Customer Need                                                              |
| --- | --- |
| Meshing gear teeth ONLY exist on the servo driven side. the servo driving side has NO mounting points (claw to base) without a servo. Do not buy this item if you do not have or plan to get a servo to complete it. | 1. NEEDS HERE |
| I am happy with it, though the gripping function is not too strong with common metal servos. | 1. NEEDS HERE |
| NOTE: NO OTHER USEFUL REVIEWS | |


#### 2. [Professional Metal Robot Arm/Gripper/Mechanical Claw/Clamp/Clip with High Torque Servo, RC Robotic Part Educational DIY for Arduino/Raspberry Pie, Science STEAM Maker Platform (Black)](https://a.co/d/031xCJhw)

![Professional Metal Robot Arm Gripper](image/ProfessionalMetal.avif)

* Vendor: Amazon

* Description: 

[ What You Get ]: In this order, you will get 1set unassembled gripper, 1 bag screw, and 1pc MG996R servo; This mechanical robot arm claw is metal including many accessories, so please have patience to install the claw. After that, the claw is very beautiful and solid.

[ NOTE ]: The claw is UNASSEMBLED for convenience of transport. But we provide the installation manual with this item or visit gitnova to get the documents, or contact us to get the document.
[ Programming ]: By this metal robot claw, you can learn the robotic structure. Importantly, you can learn the code programming to control the gripper to the destinations, arduino coding, raspberry pie, microbit, and other.

[ Function ]: You can use this clamp to realize some useful functions, i.e., use this claw to grip some items to the destinations. Many people use this claw to factory applications, experiments, and other repeat applications.

[ Learning ]: This paw can be used for the function model realization. Maybe the precision is not high, but you can learn how to control the robot claw with servo motor by the controller, like Arduino, Raspberry pie. This robot arm gripper is a research and learning kit for adult college students.



##### Positive Comments

| Voice of the Customer | Restated Customer Need|
| --- | --- |
| I purchased these grippers as part of a project I am working on to equipment a drone (a pixhawk based coaxial octocopter) with a payload gripper. These grippers assembled nicely and function well. The servo included has a good grip strengh (enough to hold a filled water bottle easily) and the assembly was straight forward and largely self explanatory. My only recommendation to the vendor would be that the instructions were printed in low resolution black and white. given the price tag I would have appreciated a full color print| 1. NEEDS HERE|
| This is a strong and steady. The claws are aligned. It takes time to install and it’s a good product. | 2. NEEDS HERE |
| A little time consuming to assemble and very sharp, but it saved our robotics season at the last minute! | 3. NEEDS HERE |



##### Negative Comments

| Voice of the Customer | Restated Customer Need|
| --- | --- |
| bearing is missing, it is useless without it. Flimsy, can be called "professional" sarcastically. | 1. NEEDS HERE |
| he kit is....ok. The stampings are good. No burs or sharp edges. Some of the holes had to be redrilled they didn't line up and everywhere flathead screw were used need to be countersunk Fail enough. But the instructions....the instructions are bad. They are tiny, poorly printed, even more poorly translated and just plain confusing and/or wrong. The pictures on the Amazon page are more useful to help understand how it goes together. | 2. NEEDS HERE |
| It locks up if you go beyond its range of operation. Open it too far or close it too far.| 3. NEEDS HERE |

#### 3. [Force Sensor FSR402 for Arduino, ESP32, ESP8266, Raspberry Pi](https://www.amazon.com/Force-Sensor-Arduino-ESP8266-Raspberry/dp/B0D2K6TVLT?th=1)

![Force Sensor FSR402](https://m.media-amazon.com/images/I/71rJGapC+VL._SX522_.jpg)

* Vendor: Amazon

* Description:
- Detects force or pressure applied to its surface
- Flexible construction for varied applications
- The higher the pressure, the lower the resistance.
- Compatible with breaboard
- Self-adhesive tape on the back, make it stickable


##### Positive Comments

| Voice of the Customer | Restated Customer Need|
| --- | --- |
|These FSR402 pressure sensors work fine for DIY projects, but you need to know exactly what board or interface you’re connecting them to. Once paired with the proper resistors and calibrated correctly, they respond well to pressure and are consistent enough for hobby builds. Just expect a bit of trial and error if it’s your first time using force-sensitive resistors.| The sensor provides consistent, repeatable pressure readings once calibrated.|
| Worked with my esp32 perfectly. It had an adhesive backside that I did not use but is convenient to have just in case. |The sensor integrates with common microcontroller platforms without special adapters. |
| Very helpful for my school project. The sensor was easy to connect and worked well with my Arduino setup. It responded accurately to pressure changes and helped me finish my project successfully. | The sensor provides accurate pressure feedback for first-time users. |



##### Negative Comments

| Voice of the Customer | Restated Customer Need|
| --- | --- |
| bearing is missing, it is useless without it. Flimsy, can be called "professional" sarcastically. | 1. NEEDS HERE |
| he kit is....ok. The stampings are good. No burs or sharp edges. Some of the holes had to be redrilled they didn't line up and everywhere flathead screw were used need to be countersunk Fail enough. But the instructions....the instructions are bad. They are tiny, poorly printed, even more poorly translated and just plain confusing and/or wrong. The pictures on the Amazon page are more useful to help understand how it goes together. | 2. NEEDS HERE |
| It locks up if you go beyond its range of operation. Open it too far or close it too far.| 3. NEEDS HERE |

#### 4. Next Product goes here

#### 5. Next Product goes here


## Organized Need Statements

### First Placement

| Source                 | Need Statement                                                                               | Category                  | Explicit/Latent|
| :---                   | :---                                                                                         | :---                      | :---          |
| Expert Interview       | Gripper provides feedback to grasp objects of varying shapes.                                | Sensing                   | Latent        |
| Expert Interview       | Grippers accommodate variation in object orientation.                                        | Control                   | Latent        |
| Expert Interview       | Gripper senses force across its gripping surface.                                            | Sensing                   | Explicit      |
| Expert Interview       | System performs reliably for short-duration tasks without long-term recalibration.           | Reliability               | Latent        |
| Expert Interview       | Control algorithm avoids inducing actuator faults.                                           | Control                   | Latent        |
| Expert Interview       | Force sensor gives graduated (non-binary) feedback.                                          | Sensing                   | Explicit      |
| Expert Interview       | Sensors perform reliably under real-world conditions.                                        | Environmental             | Latent        |
| Expert Interview       | Wiring at joints withstands rotation without failure.                                        | Mechanical                | Explicit      |

### Grouped with categories

### Ranked

## Compiled list of user Needs

1. The device will...
1. The device is ...
1. The device can ...
100. The device is...