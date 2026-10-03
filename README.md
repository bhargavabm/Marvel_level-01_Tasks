# Marvel Tasks

# Task 01 - LTspice and KiCad

**Objective:** Design and simulate a 555 timer-based astable multivibrator using LTspice to observe the frequency and pulse-width behavior. Create the circuit schematic in KiCad, assign appropriate footprints, and design a PCB layout with proper routing. This task introduces SPICE-based circuit simulation and PCB design fundamentals.

**Outcomes and Learnings:** I successfully designed and simulated a **555 timer-based astable multivibrator** using **LTspice**. I learned how the resistor and capacitor values influence the output frequency and duty cycle of the timer circuit. I also gained hands-on experience with **KiCad** by creating the schematic, assigning footprints, performing the **Electrical Rules Check (ERC)**, and designing the PCB layout.

The PCB was completed by placing the components, routing all electrical connections, and verifying the design using the **Design Rules Check (DRC)**. The circuit consists of an **NE555P timer IC**, **1 kΩ resistor**, **10 kΩ resistor**, **10 µF polarized capacitor**, and **10 nF capacitor**.

Finally, I successfully completed the **LTspice simulation**, **KiCad schematic**, and **PCB layout** for the 555 timer astable multivibrator circuit with all design checks passing successfully.

<img src="https://github.com/bhargavabm/images/blob/main/5c815ea8-3033-4037-b0e9-76776bb1c9f7.jpg?raw=true"
     alt="Task Image"
     width="700">
<img src="https://github.com/bhargavabm/images/blob/main/d13375b2-a969-442f-b50e-3e628f315a8c.jpg?raw=true"
     alt="Task Image"
     width="700">
<img src="https://github.com/bhargavabm/images/blob/main/3f4acea9-5d5f-4fb4-a774-eb564fbbcc4d.jpg?raw=true"
     alt="Task Image 3"
     width="700">
<img src="https://github.com/bhargavabm/images/blob/main/fa9f8d3d-5333-4b0b-9990-4cc605ecd186.jpg?raw=true"
     alt="KiCad PCB Layout"
     width="800">

---

# Task 02 - Point Turn of a Vehicle with Ultrasonic Sensor (Embedded)

**Objective:** Build an **obstacle-avoiding robot** using an **HC-SR04 ultrasonic sensor**, **Arduino Uno**, and a **motor driver**. The vehicle detects obstacles in its path and performs a **point turn**, rotating in place, to change direction. This task combines sensor data processing with **differential motor control**.

**Outcomes and Learnings:** I successfully built an **obstacle-avoiding vehicle** using an **Arduino Uno**, **HC-SR04 ultrasonic sensor**, **L298N motor driver**, and **two DC motors**. The Arduino sent a trigger pulse to the sensor, measured the width of the returning echo pulse, and converted it into a distance in centimetres. The vehicle drove forward while the path was clear.

When an obstacle came closer than the preset threshold distance of **20 cm**, the Arduino stopped both motors and performed a **point turn** by driving one wheel forward and the other backward at the same speed. This made the vehicle rotate about its own centre instead of making a wide arc. Once the turn was complete, the vehicle resumed moving forward in the new direction.

During this task, I learned how **ultrasonic distance measurement** works, how to use `pulseIn()` with a timeout so the program never hangs, and how a **motor driver (H-bridge)** controls motor direction and speed using direction pins and **PWM**. I also learned the principle of **differential drive**, where steering is achieved by running the left and right wheels differently. I understood the importance of a **common ground** between the Arduino and the motor power supply, and how a simple **sense, decide and act** loop forms the basis of autonomous robots.

This task enhanced my understanding of **sensor interfacing**, **motor control**, **autonomous navigation logic**, and their applications in robot vacuum cleaners, warehouse robots, parking assist systems, and collision avoidance in vehicles.

Finally, I successfully completed the **Obstacle-Avoiding Vehicle with Point Turn**, which detected obstacles and avoided them autonomously using ultrasonic sensing and differential motor control.

<img src="https://github.com/bhargavabm/images/blob/main/d06f7a5b-227f-4db7-b390-06c3bdf5719a.jpg?raw=true"
     alt="Obstacle Avoiding Vehicle Circuit"
     width="800">
<img src="https://github.com/bhargavabm/images/blob/main/78d55647-66ed-4244-a7da-c27551f7cac5.jpg?raw=true"
     alt="Vehicle Performing Point Turn"
     width="800">

---

# Task 03 - Temperature and Humidity Detection (Embedded)

**Objective:** Use the LM35 analog temperature sensor to monitor ambient temperature and trigger an LED using a BJT transistor when the temperature exceeds a predefined threshold. Simultaneously, interface the DHT11 digital sensor with an Arduino to measure and display temperature and humidity values on a 16×2 LCD. This task introduces analog and digital sensor interfacing, threshold-based control, and real-time data display.

**Outcomes and Learnings:** I successfully interfaced the **LM35 temperature sensor** and implemented threshold-based switching using a **BJT transistor** to control an LED. I learned how analog sensor readings can be converted into temperature values and used to trigger external devices.

In parallel, I interfaced the **DHT11 temperature and humidity sensor** with an **Arduino Uno** and displayed the measured temperature and humidity values on a **16×2 LCD**. This task helped me understand the difference between analog and digital sensors, Arduino sensor interfacing, LCD communication, and embedded system programming.

The project was tested successfully, and the LCD displayed real-time temperature and humidity values while the LED turned ON whenever the LM35 detected a temperature above the preset threshold.

Finally, I successfully completed the **LM35 threshold detection system** and the **DHT11 temperature and humidity monitoring system** using Arduino.

<img src="https://github.com/bhargavabm/images/blob/main/6dfcbccf-42cc-41b5-a882-f857ba62eab5.jpg?raw=true"
     alt="LM35 Temperature Detection Circuit"
     width="800">

---
# Task 10 - Auto Night Lamp Using LED for Electric Vehicles (Embedded)

**Objective:** Design and implement an automatic night lamp circuit using an **LDR (Light Dependent Resistor)** and a **BJT transistor** to control an LED based on ambient light intensity. The LED automatically turns ON in low-light conditions and OFF in bright light, simulating an automatic headlamp system for electric vehicles.

**Outcomes and Learnings:** I successfully designed and implemented an **automatic night lamp circuit** using an **LDR**, **NPN BJT transistor**, **LED**, and resistors. The LDR continuously monitored the surrounding light intensity, and the transistor acted as an electronic switch to control the LED.

When the surrounding light intensity decreased, the resistance of the LDR increased, causing the transistor to turn ON and illuminate the LED. Under bright light conditions, the LDR resistance decreased, switching the transistor OFF and turning the LED OFF. The circuit was tested using a **mobile flashlight** to simulate different lighting conditions and verify its operation.

This task enhanced my understanding of **light sensing**, **analog sensor interfacing**, **transistor switching**, and **automatic control systems** used in embedded applications. It also demonstrated a practical implementation of an automatic headlamp system commonly used in electric vehicles and smart lighting systems.

Finally, I successfully completed the **Auto Night Lamp Using LED** project, gaining practical knowledge of sensor-based automation and transistor-controlled switching circuits.

<img src="https://github.com/bhargavabm/images/blob/main/868106ce-485e-4008-9ecd-726bb9de23c6.jpg?raw=true"
     alt="Auto Night Lamp Using LED Circuit"
     width="800">
<img src="https://github.com/bhargavabm/images/blob/main/ca2e35be-e92b-4e5f-8763-1e9a7ab3d18b.jpg?raw=true"
     alt="Auto Night Lamp Circuit Demonstration"
     width="800">  

---
# Task 11 - Buck Converter on LTspice (Power Electronics)

**Objective:** Design and simulate a **DC-DC Buck Converter** using **LTspice** to understand the principle of step-down voltage conversion. Observe the input voltage, output voltage, inductor current waveform, and switching frequency to study the performance and efficiency of a switching power converter.

**Outcomes and Learnings:** I successfully designed and simulated a **DC-DC Buck Converter** in **LTspice** using a **MOSFET**, **Schottky diode (1N5819)**, **400 µH inductor**, **100 µF capacitor**, and a **20 Ω resistive load**. A PWM pulse source was used to drive the MOSFET and control the switching operation of the converter.

The converter was supplied with an **input voltage of 50 V** and successfully produced an **output voltage of approximately 19.67 V**, demonstrating effective step-down voltage conversion. During the simulation, I observed the switching operation of the MOSFET, the charging and discharging behavior of the inductor, and the filtering action of the output capacitor, which helped maintain a stable DC output.

The inductor current remained **continuously above zero** throughout the switching cycle, confirming that the converter operated in **Continuous Conduction Mode (CCM)**. This mode provides lower current ripple, improved efficiency, and more stable output voltage compared to discontinuous conduction mode.

This task enhanced my understanding of **switch-mode power supplies (SMPS)**, **Pulse Width Modulation (PWM)**, **inductor energy storage**, **capacitor filtering**, **continuous conduction mode (CCM)**, and the practical operation of DC-DC buck converters used in electric vehicles, battery-powered devices, and embedded power management systems.

Finally, I successfully completed the **Buck Converter simulation in LTspice**, obtaining an output voltage of **19.67 V** from a **50 V** input while verifying stable operation in **Continuous Conduction Mode (CCM)**.

<img src="https://github.com/bhargavabm/images/blob/main/91216a66-bc42-4f4c-85c4-7f53341fcd35.jpg?raw=true"
     alt="Buck Converter Output Analysis"
     width="800">
<img src="https://github.com/bhargavabm/images/blob/main/9dd42ff3-422c-42c8-b9ae-e223eff3a33e.jpg?raw=true"
     alt="Buck Converter Output Waveforms"
     width="800">
<img src="https://github.com/bhargavabm/images/blob/main/dc15e079-0da4-4ee3-9fbb-ad810753954d.jpg?raw=true"
     alt="Buck Converter LTspice Simulation Results"
     width="800">
<img src="https://github.com/bhargavabm/images/blob/main/962af105-660f-4557-be2f-5255d48a7290.jpg?raw=true"
     alt="Inductor Current Waveform in Continuous Conduction Mode (CCM)"
     width="800">
<img src="https://github.com/bhargavabm/images/blob/main/bb119ab1-c8fe-43ef-957e-9fd507088e09.jpg?raw=true"
     alt="Buck Converter Circuit in LTspice"
     width="800">
     
---
# Task 12 - Wireless Charger Simulation on Tinkercad (Power Electronics)

**Objective:** Simulate the basic working principle of a wireless charging system using Tinkercad. Understand inductive power transfer between a transmitter and receiver coil through a virtual simulation and observe power transfer using basic electronic components and LED indication.

**Outcomes and Learnings:** I explored the working principle of **wireless power transfer** and learned how electrical energy can be transferred without direct electrical contact using **electromagnetic induction**. I understood the roles of the transmitter and receiver coils and the importance of alternating magnetic fields in wireless charging systems.

Using **Tinkercad**, I created a conceptual simulation to study the behavior of a wireless charging circuit. Although Tinkercad has limitations in simulating true inductive coupling, the project helped me understand the fundamental concepts of wireless charging, energy transfer, and circuit design.

This task improved my understanding of **power electronics**, **inductive charging**, and their applications in smartphones, wearable devices, electric vehicles, and other wireless power systems.

Finally, I successfully completed the conceptual simulation of a wireless charging system in **Tinkercad** and gained practical knowledge of the basic principles behind wireless power transfer.

<img src="https://github.com/bhargavabm/images/blob/main/7ee3b829-757d-41b1-8da0-444e80d79f54.jpg?raw=true"
     alt="Wireless Charger Simulation on Tinkercad"
     width="800">

---
# Task 13 - Utilizing Transistors as Switches and Voltage Regulators (Power Electronics)

**Objective:** Understand how transistors can be used as digital switches and basic voltage regulators. Interface an Arduino with an NPN transistor to control an LED using a digital signal and observe the switching operation. Simulate the circuit in Tinkercad to study the voltage drop introduced by the transistor and understand its practical applications in power electronics.

**Outcomes and Learnings:** I successfully designed and simulated a **transistor switching circuit** using **Arduino Uno**, an **NPN transistor**, an **LED**, and resistors in **Tinkercad**. The Arduino digital output controlled the transistor's base, allowing the transistor to operate as an electronic switch for turning the LED ON and OFF.

During the simulation, I observed how the transistor introduces a small voltage drop across the collector-emitter junction while efficiently controlling the load. This helped me understand the operating regions of a BJT, current amplification, switching behavior, and the importance of transistors in embedded systems and power electronic circuits.

This task enhanced my understanding of **transistor switching**, **digital control using Arduino**, **voltage regulation concepts**, and their applications in switching circuits, motor drivers, relay interfaces, and DC-DC converters.

Finally, I successfully completed the simulation of a **BJT transistor switch and voltage regulation circuit** in **Tinkercad**, gaining practical knowledge of transistor-based switching and basic voltage regulation principles.

<img src="https://github.com/bhargavabm/images/blob/main/be6e0544-8b95-4bb4-b131-90150595e990.jpg?raw=true"
     alt="Transistor as a Switch and Voltage Regulator Simulation"
     width="800">

---
