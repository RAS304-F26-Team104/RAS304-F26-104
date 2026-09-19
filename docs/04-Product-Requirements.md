---
title: Product Requirements
---

## Project Objective

This project aims to investigate and develop smart adaptive technologies, an improved user experience, better fit, improved product design, and product customization options for the next-generation AirPods. The target is to maintain global dominance in the wireless earphone market, drive up AirPod sales to 100 million+ units sold with a 60% global market share in 2021 and expand the user base more towards the luxury, professional, and fitness segments. We believe that adding smart interactions and adaptive audio filters alone will already expand our user base by 15%. With the new generation AirPods we aim to match at least the sound quality of our main competitor, the Sony WF-1000XM3, and include Active Noise Canceling that is also featured in Mifo, House of Marley, Bose, and Amazon Echo products. We will also obtain IPX4 sweat-resistant rating equal to Bose, House of Marley, and Amazon Echo earbuds, and aim to extend our range of colors, as seen in Urbanista and Jabra’s lifestyle products.

## Stakeholders

* **Target group** High-income upper-class professionals between the age of 20 and 45. Their personalities are determined and ambitious. The main benefits sought are recreation and self-expression.
* **Target purchaser** Target group profile with special attention to Full Nest I and Full Nest II mothers.
* **Customer service** Prefers easy-to-repair, recyclable product, and easy-to-fix complaints to fit with Apple’s intuitive user experience.
* **Marketing & Sales division** Looks for unique selling points around the Apple Aspirer-Explorer lifestyle and user experience.
* **Retailers** Prefer products that can withstand a wide range of storage conditions including variations in temperature, vibration, humidity, and atmospheric pressure, and have a strong and compact, theft, and vandalism-proof packaging.

## Use Cases

### User Story #1: Jenna

Jenna is a 33-year-old executive who regularly visits a bar for lunch to blow off some steam. The bar is often loud with people, but it is paramount that she can hold business conversations over the phone there. Then again, she does not want to miss out on the atmosphere and be able to hear the waiters as well. Her new Apple wireless earphones allow her to switch instantly between a mode where she can fully focus on the phone conversation and a mode where the phone call and environmental sound are seamlessly combined. They also allow her to rapidly adjust the volume on the earbuds themselves without having to take out her phone.

Jenna occasionally visits the bar in the evenings. She is a big fan of the L.A. Lakers, and whenever they play, she streams the live footage through her phone. Her new earbuds allow her to easily switch to hearing everything around her and streaming the match commentary without having to ever take the earbuds out.  She sometimes gets compliments on how stylish the earbuds look on her, and she wouldn’t want to miss out on hearing those either.

### User Story #2

Dr. Ortiz buys 12 kits for her embedded systems course. The lab technician, Sam, checks each kit against the parts checklist in a few minutes and finds all kits complete. Six weeks in, one station's readings start to drift and its jaw pads are worn. Sam runs the self-test, which points to the force sensor. He swaps the sensor and pads in about 15 minutes without unmounting the gripper from the arm or tearing down the linkage, then recalibrates.

During the same week a student commands the jaws to close on a fixed vise. Firmware current limiting and the hardware over-current protection stop the servo from stalling into burnout, and the linkage does not lock up. A warning label at the jaws had already reminded the student about the pinch hazard, and no one is hurt. At the end of term, Dr. Ortiz orders gripper-only kits to fit six older arm bases left over from previous years, using the adapter plates.

## Aspects

The end effector gripper design will be based on that of the user needs with improvements based on the following requirements. The **P1 - P10** is the "code" to indicate the priority of the requirement, from low to high.

### **1. Hardware / Product Design**<br>
   1.1 The device shall provide feedback to the user in order to grasp various shapes and sized objects. (P9)<br>
   1.2 The device shall accommodate various orientations of the objects. (P10)<br>
   1.3 The device can open its jaws wide enough to accommodate larger than 2in. Sized objects. (P8)<br>
   1.4 The device’s linkage design maximises servo force. (P8)<br>
   1.5 The device is manufactured from aluminum, a durable material. (P10)<br>
   1.6 The device’s material will resist flexing under operating loads. (P9)<br>
   1.7 The device will use durable bearings at pivot points to handle dynamic loads. (P7)<br>
   1.8 The device will have wiring that will not interfere with the motion of the joints. (P7)<br>
  
### **2. Functionality**<br>
       2.1 The gripper’s grip strength shall be sufficient  to securely hold payloads. (P10)<br>
       2.2 The gripper shall sense force across its surface. (P10)<br>
       2.3 The force sensor shall give feedback. (P9)<br>
       2.4 Firmware or the servo controller shall enforce soft limits to prevent motor burnout from stalling. (P10)<br>
       2.5 The gripper sensor shall integrate directly with microcontroller ADC inputs. (P8)<br>
       2.6 The gripper sensor's circuit design shall allow simple signal conditioning rather than trial and error tuning. (P7)<br>
       2.7 The gripper sensor shall provide accurate pressure feedback. (P8)<br>
       2.8 The gripper sensor shall provide consistent and repeatable pressure readings. (P8)<br>
       2.9 Wiring at joints shall withstand rotation without failure. (P10)<br>
       2.10 The control algorithm shall avoid inducing actuator faults. (P7)<br>
       2.11 The sensor shall include precision in order to prevent drift over time. (P5)<br>
       2.12 Gripper sensor parts shall prevent users from having to debug deep electromechanical issues. (P5)<br>
       2.13 The gripper shall perform reliably for tasks without recalibration. (P5)<br>
       2.14 The gripper shall function consistently under load. (P5)<br>
       2.15 The gripper sensor will provide consistent, repeatable pressure readings once calibrated. (P8)<br>
       2.16 The gripper sensor will process precise force inputs to correctly identify whether a failed grasp was due to a sensor fault or an actuator fault. (P6)<br>

### **3. Interactivity**<br>
    3.1 The robotic arm is designed for a simple assembly process. (P8)<br>
    3.2 The gripper will include a clear circuit schematics. (P7)<br>
    3.3 The circuit should allow for simple signal conditioning without needing trial and error. (P7)<br>
    3.4 The robotic arm is easily accessible to use and integrate. (P8)<br>
    3.5 The robotic arm is designed to have a quick installation time. (P6)<br> 
    3.6 The robotic arm assembly process shall be simple, requiring no special tools. (P3)<br>
    3.7 The gripper shall work easily with existing control hardware. (P1)<br>
    3.8 The gripper sensor shall integrate with common microcontroller platforms without special adapters. (P1)<br>

### **4. Customization**<br>
    4.1 The gripper shall mount and adapt to different robotic arm bases. (P1)<br>
    4.2 Purchasing options are provided for users with preexisting components. (P1)<br>
    4.3 The robotic arm shall support the replacement of worn components of the gripper without requiring a full teardown of the gripper or mounting hardware. (P8)<br>
    4.4 The design shall support different gripper manufacturers.(P3)<br>

### **5. Manufacturing**<br>
    5.1 The total FOB cost price of the hardware of the robotic arm and gripper shall be <$700USD. (P10)<br>
    5.2 Hardware kits shall undergo quality control to ensure they contain all parts. (P7)<br>
    5.3 The manual for all assemblies shall be precise and clear. (P7)<br>
    5.4 A schematic for all parts shall be provided. (P10)<br>
    5.5 All documentation on the gripper's assembly will include clear instructions. (P5)<br>

### **6. Regulations**<br>
    6.1 The robotic arm's firmware shall be up to date. (P4)<br>
    6.2 The gripper's linkages shall have a system to prevent lock-ups. (P10)<br>
    6.2 The gripper shall not warp or become discolored under stress. (P7)<br>
    6.9 The robotic arm and gripper servo controller shall have enforced limits to prevent motor burnout. (P7)<br>

## Requirement Criteria Specifications

Method: **I** = Inspection, **A** = Analysis, **T** = Test, **D** = Demonstration. Values are initial targets.

| Req. ID | Specification | Method |
|---|---|---|
| 1.1, 1.2 | Lifts and holds 5 reference objects (cylinder, cube, sphere, plate, rod) at 0-45° yaw in at least 9 of 10 trials each. | T |
| 1.3 | Jaw opening at least 60 mm. | I |
| 1.4 | Fingertip grip force at least 15 N at rated servo torque. | T |
| 1.5, 1.6 | Aluminum links; fingertip deflection 0.5 mm or less at 20 N. | I, A |
| 1.7 | Pivot play 0.3 mm or less after 50,000 cycles. | T |
| 1.8 | No wire contacts moving links; strain relief at every connector. | I |
| 2.1 | Holds a 500 g payload for 60 s, including a 300 mm move, in 10 of 10 trials. | T |
| 2.2, 2.3 | Sensor covers 80% or more of each jaw pad; 100 Hz sampling, 10 ms or less latency. | I, T |
| 2.4, 2.10 | Torque limited within 500 ms when blocked; zero servo faults over 1,000 cycles including 50 blocked closes. | T |
| 2.5, 2.6 | 0-3.3 V output read directly by an ADC; 1 IC and 6 passives or fewer, no trim pots. | I, T |
| 2.7, 2.8, 2.15 | Within ±5% of full scale versus a reference load cell (0-20 N); standard deviation 2% or less over 100 loads. | T |
| 2.9 | No continuity loss after 10,000 joint cycles. | T |
| 2.11, 2.13, 2.14 | Drift 2% or less per hour; accuracy holds for 8 h and 500 grasps without recalibration. | T |
| 2.12, 2.16 | Self-test gives pass/fail in 10 s or less; at least 18 of 20 injected faults classified correctly. | D, T |
| 2.17 | 5 V rail within 4.75-5.25 V from a 9 V input at up to 1.5 A. | T |
| 3.1, 3.5, 3.6 | First-time users, with only the manual and included tools, assemble the gripper in 60 min or less. | D |
| 3.2, 3.3 | At least 4 of 5 first-time users wire the sensor correctly from the schematic, with no tuning. | D |
| 3.4, 3.7, 3.8 | 5 or fewer library calls; runs on Arduino, ESP32, and STM32 with no adapters. | D |
| 4.1, 4.4 | Adapter plates for at least 2 arm bases and 2 third-party grippers. | I, D |
| 4.2 | At least 3 purchase options (full kit, gripper only, sensor + electronics only). | I |
| 4.3 | Worn parts replaced in 15 min or less with the gripper left on the arm. | D |
| 5.1 | BOM under $700 USD FOB at 100 units, backed by supplier quotes. | A |
| 5.2 | Parts checklist for every kit; 1 or fewer missing-part incident per 100 kits. | I |
| 5.3, 5.5 | Each assembly step has 3 or fewer actions and an exploded view. | I |
| 5.4 | STEP/PDF drawing of every part, plus schematic and BOM. | I |
| 6.1 | Shipped firmware matches the latest tagged release; version readable over serial. | I |
| 6.2 | No linkage lock-up in 1,000 cycles. | T |
| 6.3 | No deformation over 0.1 mm, warping, or discoloration after 30 N for 60 s. | T |
| 6.4 | Over-current protection trips at 1.5 A or less; a short trips it within 100 ms with no damage. | T |

## Open Questions

* Can we move towards a recyclable and repairable product, for example, with ZIF connectors and glue-free assembly?
* Can we improve on failing or self-igniting batteries, or remove onboard batteries?
* Which force-sensor type can meet ±5% accuracy within the cost target?
* Which regulations and standards formally apply to an educational robot kit?
