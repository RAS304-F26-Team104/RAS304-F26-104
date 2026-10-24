---
title: Product Requirements
---

## Introduction

Robotic grippers have been adopted across maker platforms, automation testbeds, and in house automation solutions. Customer feedback across numerous sites have revealed a considerable number of gaps to fill in the robotic gripper market. Some of these include mechanical constraint issues, grasping compliance, no tactile feedback, and virtually no information about the object being held by the gripper. Our team sees an opportunity to create a plug and play smart gripper capable of force control, broad object adaptability, and integrated multi-modal sensor feedback.

## Objectives

This project aims to research, engineer, and validate an adaptive robotic gripper system featuring tactile sensing, rigid structural mechanisms, and a simplified user interface for industrial, academic, and prototyping applications. Our primary objective is to fill the gaps left by other products in the market by delivering reliable force control and other sensor applications. The primary goals of this project include closed loop sensing and real time feedback, custom electronics and interfacing, modular and maintainable mechanical systems, and easy system integration. These extra feedback additions within our three-hundred dollar budget allow us to potentially price a quality based gripper at a much more affordable price compared to current competitors in the market, such as FerRobotics, OnRobot, Schunk, and Robotiq.


## Stakeholders
**Target Group (Primary Users):** Undergraduate and graduate university researchers, STEM Educators, automation testbeds, rapid prototypers aged 18-45. They are hands-on, technologically ambitious, and seek a highly reliable, modular system that can integrate flawlessly with their existing and future projects.<br>
**Target Purchaser:** University lab coordinators, academic department heads, STEM program directors, and budget conscious researchers looking for gripper systems that are able to provide feedback.<br>
**End Users (Lab Peers, Researchers, Prototypers, System Integrators):** Prefers easy to repair, reliable products that are able to permit rapid component replacement without full system teardowns.<br>  
**Robot Platform (Host system bearing the payload):** Wants minimal power consumption, low weight, structural rigidity, and allows high amounts of feedback to be sent over different communication protocols.<br>
**Payload (Target Object):** Needs stable gripping surfaces, dynamic force compliance for varying stiffnesses, and non-destructive contact forces.<br>

## Use Cases

### User Story #1: Undergraduate Professor


A professor at an undergraduate college program needs to teach his students about integrating sensors into feedback loops, and selects the robotic gripper for this purpose. The gripper allows him to build on existing instruction in robotic kinematics by mounting the gripper to the arm the students have used previously. The pressure sensors in the gripper allow the students to make a program that verifies successful collection of a block by measuring the mechanical resistance on the gripper’s closing action. 
<br>
The feedback provided by the gripper also allows him to teach his students about implementing the block-sensing program into an autonomously operating program, enabling it to detect errors when the block is missed. The students are then tasked with creating software to find and recollect the block when the error is detected.
<br>

### User Story #2: Manufacturer

A manufacturer is creating delicate glass components for chandeliers. As the components come down the line in a range of sizes, it is difficult to program a set claw separation without potentially damaging the parts or getting sharp glass fragments in the assembly line. The company therefore uses the haptic gripper on the end of their arm to lift the pieces free of the assembly line. Instead of attempting to identify the glass components and adjust the gripper separation accordingly, the sensors allow the robot to always use the same safe amount of force to collect the parts.

The implementation of the gripper not only removes the need for optical sensing algorithms to determine the part to be collected, but makes the robot code simpler and more reliable. The sensors also alert the robot when it fails to collect the components properly, allowing the robot to either make another attempt or flag itself for recalibration and maintenance.


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
