---
title: User Needs and Benchmarking
---

## Stakeholder Mapping

| Stakeholder                   | Role                                                                      | Key Concerns & Needs                                                                                               |
| :---------------------------- | :------------------------------------------------------------------------ | :----------------------------------------------------------------------------------------------------------------- |
| **Operator / End User**       | Operates and monitors the gripper during tasks.                           | Sufficient grip force, intuitive operation, safe edges, and rapid deployment.                                      |
| **Maintainer / Assembler**    | Assembles, services, tunes, and replaces parts on the mechanism.          | Accurate assembly documentation, quality-controlled hardware kits, standardized fasteners, and robust wiring.    |
| **Firmware / Software Lead**  | Writes motor drivers, closed-loop feedback routines, and calibration code.| Direct ADC sensor interfacing, straightforward signal conditioning, clear reference schematics, and soft limits.  |
| **Mechanical Integrator**     | Mounts and adapts the gripper mechanism onto custom platforms/robot arms. | Standardized mounting interfaces, tight fastener tolerances, and mechanical stability without relying solely on servos. |
| **Robot Arm / Host Platform** | Host system (drone or robotic manipulator) bearing the payload.           | Minimal power consumption, low weight, structural rigidity, and no interference with rotating joints.              |
| **Payload (Target Object)**   | The physical object being handled by the end-effector.                    | Stable gripping without slipping, dynamic compliance for varying stiffness, and non-destructive contact force.   |

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
| This is a well-designed and useful gripper for grabbing a wiffle-ball, 2” cube or similar-size objects. It can be ordered with or without a servo. This can be put right on your prototype or spark your creativity for a custom design. It comes with additional screws.| Gripper jaws open wide enough to accommodate medium sized objects (2 inch objects) (Explicit) |
||Purchasing options provide flexibility for users with existing actuation options (Explicit)|
||Design supports rapid mounting and mechanical adaptation to custom platforms (Latent)|
| Good quality materials. |Structural components are manufactured from durable materials to allow long service life (Explicit)|
||Materials should resist flexing under operating loads (Latent) |
| NOTE: NO OTHER USEFUL REVIEWS | |

##### Negative Comments

| Voice of the Customer | Restated Customer Need                                                              |
| --- | --- |
| Meshing gear teeth ONLY exist on the servo driven side. the servo driving side has NO mounting points (claw to base) without a servo. Do not buy this item if you do not have or plan to get a servo to complete it. |Product documentation clarifies hardware dependencies (Explicit)|
||Structural integritiy should not rely solely on the actuator's output shaft (Latent)|
||Mechanism should elminate single point drive failure possibilites (Latent)|
| I am happy with it, though the gripping function is not too strong with common metal servos. |Linkage design should maximize the potential force application from servos (Explicit)|
||Contact surfaces should be high friction to prevent slipping (Latent)|
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
| I purchased these grippers as part of a project I am working on to equipment a drone (a pixhawk based coaxial octocopter) with a payload gripper. These grippers assembled nicely and function well. The servo included has a good grip strengh (enough to hold a filled water bottle easily) and the assembly was straight forward and largely self explanatory. My only recommendation to the vendor would be that the instructions were printed in low resolution black and white. given the price tag I would have appreciated a full color print| Gripper provides sufficient grip strength to securely hold everyday payloads (Explicit) |
||Assembly process is intuitive and simple (Explicit) |
||Documentation includes clear instructions (Latent) |
||System interfaces easily with existing control hardware (Latent) |
| This is a strong and steady. The claws are aligned. It takes time to install and it’s a good product. | Claws maintain precise alignment during operation (Explicit) |
||Gripping mechanism is sturdy under load (Explicit) |
||Assembly is streamlined to minimize installation time (Latent)|
| A little time consuming to assemble and very sharp, but it saved our robotics season at the last minute! |Components should have safe edges to prevent user injury (Explicit) |
||Reliable rapid deployment (Latent) |



##### Negative Comments

| Voice of the Customer | Restated Customer Need|
| --- | --- |
| bearing is missing, it is useless without it. Flimsy, can be called "professional" sarcastically. |Hardware kits need to undergo verified quality control to contain all parts (Explicit) |
||Structural parts should not flex under operating loads (Explicit)|
||Pivot points should use durable bearings for dynamic loads (Latent)|
| the kit is....ok. The stampings are good. No burs or sharp edges. Some of the holes had to be redrilled they didn't line up and everywhere flathead screw were used need to be countersunk Fail enough. But the instructions....the instructions are bad. They are tiny, poorly printed, even more poorly translated and just plain confusing and/or wrong. The pictures on the Amazon page are more useful to help understand how it goes together. |Mounting holes and fastener locations align within tolerances (Explicit) |
||Countersinks/counterbores should match specified hardware (Explicit)|
||Assembly manual should be accurate and clear (Explicit)|
| It locks up if you go beyond its range of operation. Open it too far or close it too far.|Linkages should include physical hard stops to prevent lock-ups (Explicit)|
||Firmware or servo controller should enforce soft limits to prevent motor burnout from "stalling" (Latent)|
||Linkages should be backdrieable without seizing if pushed to limits (Latent)|

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
| Worked with my esp32 perfectly. It had an adhesive backside that I did not use but is convenient to have just in case. |The sensor integrates with common microcontroller platforms without special adapters. (Explicit)|
||Clear reference schematics should be provided (Latent)|
||Circuit design should allow simple signal conditioning, not trial and error tuning (Latent)|
| Very helpful for my school project. The sensor was easy to connect and worked well with my Arduino setup. It responded accurately to pressure changes and helped me finish my project successfully. | The sensor provides accurate pressure feedback (Explicit)|
||Sensor integrates directly with microcontroller ADC inputs (Explicit)|
||Sensor functions consistently under load (Latent)|


##### Negative Comments

| Voice of the Customer | Restated Customer Need|
| --- | --- |
| Sensor would drift after long periods of continuous use, values would gradually drift high when the sensor was used for more than 2 hours. | Sensor can include robustness and precision in order to prevent drift (Explicit)|
| The force sensor worked well for our project however signals would often bounce due to some electrical malfunction. Was not able to take apart and fix. | Sensor parts need to be robust as to prevent user from debugging an deep electromechanical issue. (Explicit)|
| No other useful negative comments | |


## Organized Need Statements

### First Placement

| Source                                 | Need Statement                                                                               | Category                 | Explicit/Latent |
| :------------------------------------- | :------------------------------------------------------------------------------------------- | :----------------------- | :-------------- |
| Expert Interview                       | Gripper provides feedback to grasp objects of varying shapes.                                | Sensing                  | Latent          |
| Expert Interview                       | Grippers accommodate variation in object orientation.                                        | Control                  | Latent          |
| Expert Interview                       | Gripper senses force across its gripping surface.                                            | Sensing                  | Explicit        |
| Expert Interview                       | System performs reliably for short-duration tasks without long-term recalibration.           | Reliability              | Latent          |
| Expert Interview                       | Control algorithm avoids inducing actuator faults.                                           | Control                  | Latent          |
| Expert Interview                       | Force sensor gives graduated (non-binary) feedback.                                          | Sensing                  | Explicit        |
| Expert Interview                       | Sensors perform reliably under real-world conditions.                                        | Environmental            | Latent          |
| Expert Interview                       | Wiring at joints withstands rotation without failure.                                        | Mechanical               | Explicit        |
| Product 1 (Mechanical Claw)            | Gripper jaws open wide enough to accommodate medium sized objects (2 inch objects).          | Mechanical               | Explicit        |
| Product 1 (Mechanical Claw)            | Purchasing options provide flexibility for users with existing actuation options.            | Usability / Integration  | Explicit        |
| Product 1 (Mechanical Claw)            | Design supports rapid mounting and mechanical adaptation to custom platforms.                | Mechanical / Integration | Latent          |
| Product 1 (Mechanical Claw)            | Structural components are manufactured from durable materials to allow long service life.    | Durability / Materials   | Explicit        |
| Product 1 (Mechanical Claw)            | Materials should resist flexing under operating loads.                                       | Mechanical / Structure   | Latent          |
| Product 1 (Mechanical Claw)            | Product documentation clarifies hardware dependencies.                                       | Documentation            | Explicit        |
| Product 1 (Mechanical Claw)            | Structural integrity should not rely solely on the actuator's output shaft.                  | Mechanical               | Latent          |
| Product 1 (Mechanical Claw)            | Mechanism should eliminate single point drive failure possibilities.                         | Reliability              | Latent          |
| Product 1 (Mechanical Claw)            | Linkage design should maximize the potential force application from servos.                  | Mechanical               | Explicit        |
| Product 1 (Mechanical Claw)            | Contact surfaces should be high friction to prevent slipping.                                | Usability / Materials    | Latent          |
| Product 2 (Metal Claw with Servo)      | Gripper provides sufficient grip strength to securely hold everyday payloads.                | Performance              | Explicit        |
| Product 2 (Metal Claw with Servo)      | Assembly process is intuitive and simple.                                           | Usability                | Explicit        |
| Product 2 (Metal Claw with Servo)      | Documentation includes clear instructions.                                                   | Documentation            | Latent          |
| Product 2 (Metal Claw with Servo)      | System interfaces easily with existing control hardware.                                     | Integration              | Latent          |
| Product 2 (Metal Claw with Servo)      | Claws maintain precise alignment during operation.                                           | Mechanical               | Explicit        |
| Product 2 (Metal Claw with Servo)      | Gripping mechanism is sturdy under load.                                                     | Mechanical / Durability  | Explicit        |
| Product 2 (Metal Claw with Servo)      | Assembly is streamlined to minimize installation time.                                       | Usability                | Latent          |
| Product 2 (Metal Claw with Servo)      | Components should have safe edges to prevent user injury.                                    | Safety                   | Explicit        |
| Product 2 (Metal Claw with Servo)      | System provides reliable rapid deployment.                                                   | Reliability              | Latent          |
| Product 2 (Metal Claw with Servo)      | Hardware kits need to undergo verified quality control to contain all parts.                 | Quality Control          | Explicit        |
| Product 2 (Metal Claw with Servo)      | Structural parts should not flex under operating loads.                                      | Mechanical / Durability  | Explicit        |
| Product 2 (Metal Claw with Servo)      | Pivot points should use durable bearings for dynamic loads.                                  | Mechanical               | Latent          |
| Product 2 (Metal Claw with Servo)      | Mounting holes and fastener locations align within tolerances.                               | Manufacturing / Quality  | Explicit        |
| Product 2 (Metal Claw with Servo)      | Countersinks/counterbores should match specified hardware.                                   | Manufacturing / Mechanical | Explicit      |
| Product 2 (Metal Claw with Servo)      | Assembly manual should be accurate and clear.                                                | Documentation            | Explicit        |
| Product 2 (Metal Claw with Servo)      | Linkages should include physical hard stops to prevent lock-ups.                             | Mechanical / Safety      | Explicit        |
| Product 2 (Metal Claw with Servo)      | Firmware or servo controller should enforce soft limits to prevent motor burnout from stalling.| Control / Electrical   | Latent          |
| Product 2 (Metal Claw with Servo)      | Linkages should be backdrivable without seizing if pushed to limits.                         | Mechanical               | Latent          |
| Product 3 (FSR402 Sensor)              | The sensor provides consistent, repeatable pressure readings once calibrated.                | Sensing                  | Latent          |
| Product 3 (FSR402 Sensor)              | The sensor integrates with common microcontroller platforms without special adapters.        | Electrical / Integration | Explicit        |
| Product 3 (FSR402 Sensor)              | Clear reference schematics should be provided.                                               | Documentation            | Latent          |
| Product 3 (FSR402 Sensor)              | Circuit design should allow simple signal conditioning, not trial and error tuning. | Electrical               | Latent          |
| Product 3 (FSR402 Sensor)              | The sensor provides accurate pressure feedback.                                              | Sensing                  | Explicit        |
| Product 3 (FSR402 Sensor)              | Sensor integrates directly with microcontroller ADC inputs.                                  | Electrical / Integration | Explicit        |
| Product 3 (FSR402 Sensor)              | Sensor functions consistently under load.                                                    | Reliability              | Latent          |
| Product 3 (FSR402 Sensor)              | Sensor includes robustness and precision in order to prevent drift over time.                | Sensing / Reliability    | Explicit        |
| Product 3 (FSR402 Sensor)              | Sensor parts need to be robust to prevent users from having to debug deep electromechanical issues. | Reliability / Durability | Explicit |

### Grouped with categories
#### Sensing

| Source                                 | Need Statement                                                                               | Category                 | Explicit/Latent |
| :------------------------------------- | :------------------------------------------------------------------------------------------- | :----------------------- | :-------------- |
| Expert Interview                       | Gripper provides feedback to grasp objects of varying shapes.                                | Sensing                  | Latent          |
| Expert Interview                       | Gripper senses force across its gripping surface.                                            | Sensing                  | Explicit        |
| Expert Interview                       | Force sensor gives graduated (non-binary) feedback.                                          | Sensing                  | Explicit        |
| Product 3 (FSR402 Sensor)              | The sensor provides consistent, repeatable pressure readings once calibrated.                | Sensing                  | Latent          |
| Product 3 (FSR402 Sensor)              | The sensor provides accurate pressure feedback.                                              | Sensing                  | Explicit        |
| Product 3 (FSR402 Sensor)              | Sensor includes robustness and precision in order to prevent drift over time.                | Sensing / Reliability    | Explicit        |

#### Control

| Source                                 | Need Statement                                                                               | Category                 | Explicit/Latent |
| :------------------------------------- | :------------------------------------------------------------------------------------------- | :----------------------- | :-------------- |
| Expert Interview                       | Grippers accommodate variation in object orientation.                                        | Control                  | Latent          |
| Expert Interview                       | Control algorithm avoids inducing actuator faults.                                           | Control                  | Latent          |
| Product 2 (Metal Claw with Servo)      | Firmware or servo controller should enforce soft limits to prevent motor burnout from stalling.| Control / Electrical   | Latent          |

#### Mechanical

| Source                                 | Need Statement                                                                               | Category                 | Explicit/Latent |
| :------------------------------------- | :------------------------------------------------------------------------------------------- | :----------------------- | :-------------- |
| Expert Interview                       | Wiring at joints withstands rotation without failure.                                        | Mechanical               | Explicit        |
| Product 1 (Mechanical Claw)            | Gripper jaws open wide enough to accommodate medium sized objects (2 inch objects).          | Mechanical               | Explicit        |
| Product 1 (Mechanical Claw)            | Design supports rapid mounting and mechanical adaptation to custom platforms.                | Mechanical / Integration | Latent          |
| Product 1 (Mechanical Claw)            | Materials should resist flexing under operating loads.                                       | Mechanical / Structure   | Latent          |
| Product 1 (Mechanical Claw)            | Structural integrity should not rely solely on the actuator's output shaft.                  | Mechanical               | Latent          |
| Product 1 (Mechanical Claw)            | Linkage design should maximize the potential force application from servos.                  | Mechanical               | Explicit        |
| Product 2 (Metal Claw with Servo)      | Claws maintain precise alignment during operation.                                           | Mechanical               | Explicit        |
| Product 2 (Metal Claw with Servo)      | Gripping mechanism is sturdy under load.                                                     | Mechanical / Durability  | Explicit        |
| Product 2 (Metal Claw with Servo)      | Structural parts should not flex under operating loads.                                      | Mechanical / Durability  | Explicit        |
| Product 2 (Metal Claw with Servo)      | Pivot points should use durable bearings for dynamic loads.                                  | Mechanical               | Latent          |
| Product 2 (Metal Claw with Servo)      | Countersinks/counterbores should match specified hardware.                                   | Manufacturing / Mechanical | Explicit      |
| Product 2 (Metal Claw with Servo)      | Linkages should include physical hard stops to prevent lock-ups.                             | Mechanical / Safety      | Explicit        |
| Product 2 (Metal Claw with Servo)      | Linkages should be backdrivable without seizing if pushed to limits.                         | Mechanical               | Latent          |

#### Reliability

| Source                                 | Need Statement                                                                               | Category                 | Explicit/Latent |
| :------------------------------------- | :------------------------------------------------------------------------------------------- | :----------------------- | :-------------- |
| Expert Interview                       | System performs reliably for short-duration tasks without long-term recalibration.           | Reliability              | Latent          |
| Product 1 (Mechanical Claw)            | Mechanism should eliminate single point drive failure possibilities.                         | Reliability              | Latent          |
| Product 2 (Metal Claw with Servo)      | System provides reliable rapid deployment.                                                   | Reliability              | Latent          |
| Product 3 (FSR402 Sensor)              | Sensor functions consistently under load.                                                    | Reliability              | Latent          |
| Product 3 (FSR402 Sensor)              | Sensor includes robustness and precision in order to prevent drift over time.                | Sensing / Reliability    | Explicit        |
| Product 3 (FSR402 Sensor)              | Sensor parts need to be robust to prevent users from having to debug deep electromechanical issues. | Reliability / Durability | Explicit |

#### Electrical & Integration

| Source                                 | Need Statement                                                                               | Category                 | Explicit/Latent |
| :------------------------------------- | :------------------------------------------------------------------------------------------- | :----------------------- | :-------------- |
| Product 1 (Mechanical Claw)            | Purchasing options provide flexibility for users with existing actuation options.            | Usability / Integration  | Explicit        |
| Product 1 (Mechanical Claw)            | Design supports rapid mounting and mechanical adaptation to custom platforms.                | Mechanical / Integration | Latent          |
| Product 2 (Metal Claw with Servo)      | System interfaces easily with existing control hardware.                                     | Integration              | Latent          |
| Product 2 (Metal Claw with Servo)      | Firmware or servo controller should enforce soft limits to prevent motor burnout from stalling.| Control / Electrical   | Latent          |
| Product 3 (FSR402 Sensor)              | The sensor integrates with common microcontroller platforms without special adapters.       | Electrical / Integration | Explicit        |
| Product 3 (FSR402 Sensor)              | Circuit design should allow simple signal conditioning, not trial and error tuning. | Electrical               | Latent          |
| Product 3 (FSR402 Sensor)              | Sensor integrates directly with microcontroller ADC inputs.                                  | Electrical / Integration | Explicit        |

#### Usability & Safety

| Source                                 | Need Statement                                                                               | Category                 | Explicit/Latent |
| :------------------------------------- | :------------------------------------------------------------------------------------------- | :----------------------- | :-------------- |
| Product 1 (Mechanical Claw)            | Purchasing options provide flexibility for users with existing actuation options.            | Usability / Integration  | Explicit        |
| Product 1 (Mechanical Claw)            | Contact surfaces should be high friction to prevent slipping.                                | Usability / Materials    | Latent          |
| Product 2 (Metal Claw with Servo)      | Assembly process is intuitive and simple.                                           | Usability                | Explicit        |
| Product 2 (Metal Claw with Servo)      | Assembly is streamlined to minimize installation time.                                       | Usability                | Latent          |
| Product 2 (Metal Claw with Servo)      | Components should have safe edges to prevent user injury.                                    | Safety                   | Explicit        |
| Product 2 (Metal Claw with Servo)      | Linkages should include physical hard stops to prevent lock-ups.                             | Mechanical / Safety      | Explicit        |

#### Materials & Durability

| Source                                 | Need Statement                                                                               | Category                 | Explicit/Latent |
| :------------------------------------- | :------------------------------------------------------------------------------------------- | :----------------------- | :-------------- |
| Product 1 (Mechanical Claw)            | Structural components are manufactured from durable materials to allow long service life.    | Durability / Materials   | Explicit        |
| Product 1 (Mechanical Claw)            | Materials should resist flexing under operating loads.                                       | Mechanical / Structure   | Latent          |
| Product 1 (Mechanical Claw)            | Contact surfaces should be high friction to prevent slipping.                                | Usability / Materials    | Latent          |
| Product 2 (Metal Claw with Servo)      | Gripping mechanism is sturdy under load.                                                     | Mechanical / Durability  | Explicit        |
| Product 2 (Metal Claw with Servo)      | Structural parts should not flex under operating loads.                                      | Mechanical / Durability  | Explicit        |
| Product 3 (FSR402 Sensor)              | Sensor parts need to be robust to prevent users from having to debug deep electromechanical issues. | Reliability / Durability | Explicit |

#### Documentation

| Source                                 | Need Statement                                                                               | Category                 | Explicit/Latent |
| :------------------------------------- | :------------------------------------------------------------------------------------------- | :----------------------- | :-------------- |
| Product 1 (Mechanical Claw)            | Product documentation clarifies hardware dependencies.                                       | Documentation            | Explicit        |
| Product 2 (Metal Claw with Servo)      | Documentation includes clear instructions.                                                   | Documentation            | Latent          |
| Product 2 (Metal Claw with Servo)      | Assembly manual should be accurate and clear.                                                | Documentation            | Explicit        |
| Product 3 (FSR402 Sensor)              | Clear reference schematics should be provided.                                               | Documentation            | Latent          |

#### Manufacturing & Quality Control

| Source                                 | Need Statement                                                                               | Category                 | Explicit/Latent |
| :------------------------------------- | :------------------------------------------------------------------------------------------- | :----------------------- | :-------------- |
| Product 2 (Metal Claw with Servo)      | Hardware kits need to undergo verified quality control to contain all parts.                 | Quality Control          | Explicit        |
| Product 2 (Metal Claw with Servo)      | Mounting holes and fastener locations align within tolerances.                               | Manufacturing / Quality  | Explicit        |
| Product 2 (Metal Claw with Servo)      | Countersinks/counterbores should match specified hardware.                                   | Manufacturing / Mechanical | Explicit      |

#### Performance & Environment

| Source                                 | Need Statement                                                                               | Category                 | Explicit/Latent |
| :------------------------------------- | :------------------------------------------------------------------------------------------- | :----------------------- | :-------------- |
| Expert Interview                       | Sensors perform reliably under real world conditions.                                        | Environmental            | Latent          |
| Product 2 (Metal Claw with Servo)      | Gripper provides sufficient grip strength to securely hold everyday payloads.                | Performance              | Explicit        |


### Ranked


#### Critical (Primary functions and core project goals)
| Source                                 | Need Statement                                                                               | Category                 |
| :------------------------------------- | :------------------------------------------------------------------------------------------- | :----------------------- |
| Product 2 (Metal Claw with Servo)      | Gripper provides sufficient grip strength to securely hold everyday payloads.                | Performance              |
| Expert Interview                       | Gripper senses force across its gripping surface.                                            | Sensing                  |
| Expert Interview                       | Force sensor gives graduated (non-binary) feedback.                                          | Sensing                  |
| Product 2 (Metal Claw with Servo)      | Firmware or servo controller should enforce soft limits to prevent motor burnout from stalling.| Control / Electrical   |
| Product 2 (Metal Claw with Servo)      | Linkages should include physical hard stops to prevent lock-ups.                             | Mechanical / Safety      |

#### High (Essential interfacing and electrical architecture)
| Source                                 | Need Statement                                                                               | Category                 |
| :------------------------------------- | :------------------------------------------------------------------------------------------- | :----------------------- |
| Product 3 (FSR402 Sensor)              | Sensor integrates directly with microcontroller ADC inputs.                                  | Electrical / Integration |
| Product 3 (FSR402 Sensor)              | Circuit design should allow simple signal conditioning, not trial and error tuning. | Electrical               |
| Product 3 (FSR402 Sensor)              | The sensor provides accurate pressure feedback.                                              | Sensing                  |
| Product 3 (FSR402 Sensor)              | The sensor provides consistent, repeatable pressure readings once calibrated.                | Sensing                  |
| Expert Interview                       | Wiring at joints withstands rotation without failure.                                        | Mechanical               |
| Product 1 (Mechanical Claw)            | Linkage design should maximize the potential force application from servos.                  | Mechanical               |
| Product 2 (Metal Claw with Servo)      | Claws maintain precise alignment during operation.                                           | Mechanical               |
| Product 2 (Metal Claw with Servo)      | Gripping mechanism is sturdy under load.                                                     | Mechanical / Durability  |
| Product 1 (Mechanical Claw)            | Structural integrity should not rely solely on the actuator's output shaft.                  | Mechanical               |
| Product 1 (Mechanical Claw)            | Contact surfaces should be high friction to prevent slipping.                                | Usability / Materials    |
| Expert Interview                       | Control algorithm avoids inducing actuator faults.                                           | Control                  |

#### Medium (Adaptability, functionality, longevitiy, stability)
| Source                                 | Need Statement                                                                               | Category                 |
| :------------------------------------- | :------------------------------------------------------------------------------------------- | :----------------------- |
| Expert Interview                       | Gripper provides feedback to grasp objects of varying shapes.                                | Sensing                  |
| Expert Interview                       | Grippers accommodate variation in object orientation.                                        | Control                  |
| Product 1 (Mechanical Claw)            | Gripper jaws open wide enough to accommodate medium sized objects (2 inch objects).          | Mechanical               |
| Product 3 (FSR402 Sensor)              | Sensor includes robustness and precision in order to prevent drift over time.                | Sensing / Reliability    |
| Product 3 (FSR402 Sensor)              | Sensor parts need to be robust to prevent users from having to debug deep electromechanical issues. | Reliability / Durability |
| Product 1 (Mechanical Claw)            | Structural components are manufactured from durable materials to allow long service life.    | Durability / Materials   |
| Product 1 (Mechanical Claw)            | Materials should resist flexing under operating loads.                                       | Mechanical / Structure   |
| Product 2 (Metal Claw with Servo)      | Structural parts should not flex under operating loads.                                      | Mechanical / Durability  |
| Product 2 (Metal Claw with Servo)      | Mounting holes and fastener locations align within tolerances.                               | Manufacturing / Quality  |
| Product 2 (Metal Claw with Servo)      | Countersinks/counterbores should match specified hardware.                                   | Manufacturing / Mechanical|
| Product 2 (Metal Claw with Servo)      | Pivot points should use durable bearings for dynamic loads.                                  | Mechanical               |
| Product 2 (Metal Claw with Servo)      | Linkages should be backdrivable without seizing if pushed to limits.                         | Mechanical               |
| Expert Interview                       | Sensors perform reliably under real-world conditions.                                        | Environmental            |
| Expert Interview                       | System performs reliably for short-duration tasks without long-term recalibration.           | Reliability              |
| Product 3 (FSR402 Sensor)              | Sensor functions consistently under load.                                                    | Reliability              |
| Product 1 (Mechanical Claw)            | Mechanism should eliminate single point drive failure possibilities.                         | Reliability              |

#### Low (Convenience and Assembly factors)
| Source                                 | Need Statement                                                                               | Category                 |
| :------------------------------------- | :------------------------------------------------------------------------------------------- | :----------------------- |
| Product 2 (Metal Claw with Servo)      | System interfaces easily with existing control hardware.                                     | Integration              |
| Product 3 (FSR402 Sensor)              | The sensor integrates with common microcontroller platforms without special adapters.        | Electrical / Integration |
| Product 1 (Mechanical Claw)            | Design supports rapid mounting and mechanical adaptation to custom platforms.                | Mechanical / Integration |
| Product 2 (Metal Claw with Servo)      | Components should have safe edges to prevent user injury.                                    | Safety                   |
| Product 2 (Metal Claw with Servo)      | Assembly process is intuitive and simple.                                           | Usability                |
| Product 2 (Metal Claw with Servo)      | Assembly is streamlined to minimize installation time                                        | Usability                |



## Compiled list of user Needs

1. The device will provide feedback to grasp objects of varying shapes.
2. The device can accommodate variations in object orientation.
3. The device will sense force across its gripping surface.
4. The device will perform reliably for short duration tasks without long term recalibration.
5. The device will use a control algorithm that avoids inducing actuator faults.
6. The device will give graduated (non binary) force feedback.
7. The device will perform reliably under real world environmental conditions.
8. The device will feature wiring at joints that withstands rotation without failure.
9. The device can open its jaws wide enough to accommodate medium sized objects (e.g., 2 inch objects).
10. The device will offer purchasing options that provide flexibility for users with existing actuation options.
11. The device can support rapid mounting and mechanical adaptation to custom platforms.
12. The device is manufactured from durable materials to allow a long service life.
13. The device will resist flexing under operating loads.
14. The device will include product documentation that clearly defines hardware dependencies.
15. The device will not rely solely on the actuator's output shaft for structural integrity.
16. The device will feature a mechanism that eliminates single point drive failure possibilities.
17. The device will feature a linkage design that maximizes the potential force application from servos.
18. The device will have high friction contact surfaces to prevent slipping.
19. The device will provide sufficient grip strength to securely hold everyday payloads.
20. The device is designed for an intuitive and simple assembly process.
21. The device will include clear instructions in its documentation.
22. The device can interface easily with existing control hardware.
23. The device will maintain precise claw alignment during operation.
24. The device is sturdy under load.
25. The device is streamlined to minimize installation time.
26. The device will have safe edges on all components to prevent user injury.
27. The device can be reliably and rapidly deployed.
28. The device will undergo verified quality control to ensure kits contain all necessary parts.
29. The device's structural parts will not flex under operating loads.
30. The device will use durable bearings at pivot points to handle dynamic loads.
31. The device will have mounting holes and fastener locations that align within tight tolerances.
32. The device will have countersinks and counterbores that perfectly match specified hardware.
33. The device will come with an accurate and clear assembly manual.
34. The device will include physical hard stops in its linkages to prevent lockups.
35. The device will enforce soft limits via firmware or servo controllers to prevent motor burnout from stalling.
36. The device can be back driven without seizing if pushed to its physical limits.
37. The device will provide consistent, repeatable pressure readings once calibrated.
38. The device can integrate with common microcontroller platforms without the need for special adapters.
39. The device will be accompanied by clear reference schematics.
40. The device's circuit design will allow for simple signal conditioning rather than trial and error tuning.
41. The device will provide accurate pressure feedback.
42. The device can integrate directly with microcontroller ADC inputs.
43. The device will function consistently under load.
44. The device is robust and precise in order to prevent signal drift over time.
45. The device is physically robust to prevent users from having to debug deep electromechanical issues.
46. The device will provide tactile feedback about the object being gripped.
47. The device can adapt to targets that vary significantly in physical shape.
48. The device can successfully accommodate objects presented in various orientations.
49. The device will exhibit high dexterity to handle complex grasping tasks.
50. The device will use a dynamic touch array to gather spatial force data.
51. The device will perform reliably for short duration tasks without requiring long term, multi day calibration.
52. The device will support hard coded Cartesian coordinates for highly repeatable tasks.
53. The device will track the exact closure amount of the gripping mechanism.
54. The device will rely on a robust grasping algorithm to prevent actuator faults.
55. The device will measure grip force precisely rather than relying on binary contact detection.
56. The device will maintain sensor accuracy even when operating outside of strictly controlled environments.
57. The device will feature wiring routing that does not interfere with the motion of the joints.
58. The device will feature connectors that remain unaffected by continuous joint rotation.
59. The device will use rolling contact joint principles to minimize wiring stress during actuation.
60. The device will mimic the sensory and dexterity considerations of human grasping.
61. The device will use an adaptive control strategy rather than relying solely on model based control.
62. The device can safely handle and adjust to objects of varying stiffness.
63. The device will adjust its grip dynamically as the target object is pressed and deformed.
64. The device will react to sensor input in real time to update its control loop.
65. The device will isolate its sensing elements from environmental vibrations.
66. The device will maintain stable readings regardless of ambient temperature fluctuations.
67. The device will provide deterministic feedback to ensure an object is grasped exactly the same way during repeated attempts.
68. The device can successfully grasp targets despite varying initial conditions.
69. The device will adjust its approach for objects that are aligned differently during each pickup attempt.
70. The device will be cost effective to accommodate standard university research budgets.
71. The device is priced significantly below the standard two thousand dollar industrial sensor baseline.
72. The device is designed for simple physical assembly of the sensing components.
73. The device will integrate its sensors with the broader robotics system.
74. The device is accessible for integration and operation by less experienced students and researchers.
75. The device will process precise force inputs to correctly identify whether a failed grasp was due to a sensor fault or an actuator fault.