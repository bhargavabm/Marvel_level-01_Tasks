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

# Task 05 - Battery Capacity Measurement (Power Electronics)

**Objective:** Monitor the voltage of a **Li-ion battery** using the analog input of an **Arduino** and use a **MOSFET as a switch** to disconnect the load when the voltage drops below a safe threshold. The task ensures safe battery operation and demonstrates basic **battery protection logic**.

**Outcomes and Learnings:** I successfully designed and simulated a **battery voltage monitoring and protection circuit** in **Tinkercad** using an **Arduino Uno**, an **N-channel MOSFET**, an **LED load**, a **9 V battery** and resistors. Two equal resistors formed a **voltage divider** that scaled the battery voltage down by half, so it stayed within the Arduino's **0 to 5 V ADC range**. The scaled voltage was read on pin **A0**, and the Arduino converted the reading back to the real battery voltage in software.

The MOSFET was connected as a **low-side switch**, with its gate driven by an Arduino digital pin. While the battery voltage stayed above the preset threshold, the Arduino kept the MOSFET ON and the LED load stayed lit. When the voltage dropped below the threshold, the Arduino turned the MOSFET OFF and **disconnected the load**, protecting the battery from over-discharge. I tested this by lowering the battery voltage in the simulation and watching the **Serial Monitor** readings fall until the LED switched off. A series resistor protected the LED, and a **common ground** between the battery and the Arduino was required for correct readings.

During this task, I learned how a **voltage divider** scales a voltage for ADC measurement, how `analogRead()` values (0 to 1023) are converted into volts, and how a **MOSFET works as an electronic switch** controlled by a small gate signal. I also learned the **threshold-based protection logic** used in a battery management system (BMS), why a **hysteresis margin** prevents flickering near the cutoff, and why Li-ion cells must not be discharged below about **3.0 to 3.2 V** per cell to avoid damage and safety hazards.

This task enhanced my understanding of **battery monitoring**, **analog sensing**, **MOSFET switching** and **over-discharge protection**, as used in power banks, laptops, e-bikes, drones and electric vehicles.

Finally, I successfully completed the **Battery Capacity Measurement and protection circuit**, demonstrating protection through **voltage monitoring and switching**.

<img src="https://github.com/bhargavabm/images/blob/main/470451fa-9bd0-4dc4-bee1-44853e321e9f.jpg?raw=true"
     alt="Battery Protection Circuit in Tinkercad"
     width="800">

---

# Task 06 - Battery Charging (Power Electronics)

**Objective:** Charge a **Li-ion battery** using a **solar panel** and a **solar charging module**, and understand the practical implementation of solar-based charging. The task covers how a solar source, a charge controller and a battery work together, including the **constant-current / constant-voltage (CC/CV)** charging method used for Li-ion cells.

**Outcomes and Learnings:** I studied the working of a **solar battery charger for an 18650 Li-ion cell** using a **solar panel**, a **TP4056 charging module with protection** and a **battery holder**. The panel's output feeds the module's input, and the module charges the cell safely, stopping at **4.2 V** and showing the charging and full states with its indicator LEDs.

Since Tinkercad has no solar panel, TP4056 module or real Li-ion cell, I built a **charging simulation** in **Tinkercad** using an **Arduino Uno**, a **DC power supply (5 V)** as the solar source, a **1N4007 diode**, a **1 kΩ charge-limiting resistor**, a **1000 µF polarised capacitor** acting as the battery, and **red and green LEDs** with 220 Ω resistors. The diode blocked reverse current, as a blocking diode does between a panel and a battery at night. The resistor limited the charging current, and the capacitor voltage rose gradually, like a cell charging.

The Arduino read the battery voltage on pin **A0**, showed it on the **Serial Monitor**, turned the **red LED ON while charging**, and switched to the **green LED** once the voltage reached about **4.2 V**. A larger resistor (10 kΩ) slowed the charge so the red LED stayed visible longer. The simulation is only a model: the capacitor cannot show a real battery's capacity, and unlike a TP4056, the Arduino only indicates the full state and doesn't stop the charge.

During this task, I learned the **CC/CV charging method**, why Li-ion cells must not be charged above **4.2 V**, and the role of a **blocking diode** and a **current-limiting resistor**. I also learned how to **read a battery voltage with an ADC**, how a **charge controller module** adds protection, and the practical limits of simulating batteries.

This task enhanced my understanding of **solar energy harvesting**, **Li-ion charging**, **power electronics** and **battery safety**, as used in solar lamps, power banks, IoT devices and electric vehicles.

Finally, I successfully completed the **Battery Charging task**, understanding the practical implementation of solar-based charging and demonstrating the charge indication in a **Tinkercad** simulation.

<img src="https://github.com/bhargavabm/images/blob/main/efb319b6-23a8-430d-a4f2-cf5035b32e71.jpg?raw=true"
     alt="Solar Battery Charging Circuit in Tinkercad"
     width="800">
<img src="https://github.com/bhargavabm/images/blob/main/ed7aaf34-e251-476c-8864-f27e3296a301.jpg?raw=true"
     alt="Charging Voltage and LED Indication"
     width="800">

---

# Task 07 - Solar Tracker (Embedded)

**Objective:** Use **LDRs (Light Dependent Resistors)** and a **servo motor** controlled by an **Arduino** to orient a solar panel toward the strongest light source. The system maximizes solar energy collection using **dual LDR comparison logic** and basic **actuator control**.

**Outcomes and Learnings:** I successfully designed and simulated a **solar tracker** in **Tinkercad** using an **Arduino Uno**, **two LDRs**, **two 10 kΩ resistors** and a **micro servo motor**. Each LDR formed a **voltage divider** with a resistor, so its brightness could be read as an analog voltage on pins **A0** and **A1**. The two LDRs represented the left and right sides of the solar panel.

The Arduino compared the two readings and turned the servo toward the brighter side in **small steps of 1°**, until both LDRs received about the same light and the panel was facing the light source. A **tolerance (dead zone)** was added so the servo did not jitter when the two readings were nearly equal, and the servo angle was limited to **0° to 180°**. I tested the system by changing the light level of each LDR in the simulation and observing the servo rotate toward the brighter side and stop when the readings balanced. The readings and servo angle were displayed on the **Serial Monitor**.

During this task, I learned how an **LDR's resistance changes with light**, how a **voltage divider** converts it to a readable voltage, how **comparison logic** decides the direction of movement, and how to control a **servo** using the Arduino `Servo` library. I also learned why a **dead zone** is needed for stable control, why a **divider wall** between the LDRs creates the light difference on a real panel, and why a larger servo needs a separate power supply with a common ground.

This task enhanced my understanding of **sensor-based automation**, **actuator control** and **solar energy maximization**, as used in solar farms, solar street lights, satellite panels and renewable energy systems.

Finally, I successfully completed the **Solar Tracker**, achieving energy maximization through a sun-tracking mechanism that orients the panel toward the strongest light.

<img src="https://github.com/bhargavabm/images/blob/main/91f16178-c674-4fd5-8c68-7c75c715f226.jpg?raw=true"
     alt="Servo Rotating Towards the Brighter LDR "
     width="800">
<img src="https://github.com/bhargavabm/images/blob/main/3fc5fece-b054-4c86-bc63-72ebb9cea65d.jpg?raw=true"
     alt="Coding related to LDR"
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

# Task 14 - LED Brightness Control Using PWM and MOSFET (Power Electronics)

**Objective:** Use an **Arduino** and an **N-channel MOSFET** to control the brightness of an LED through **Pulse Width Modulation (PWM)**. The Arduino sends a PWM signal to the MOSFET's gate, which controls the current flowing between the drain and source. A higher **duty cycle** gives a brighter LED, and a lower duty cycle gives a dimmer one.

**Outcomes and Learnings:** I successfully designed and simulated an **LED brightness control circuit** in **Tinkercad** using an **Arduino Uno**, an **N-channel MOSFET**, an **LED**, a current-limiting resistor and a gate pull-down resistor. A PWM-capable Arduino pin was connected to the MOSFET's **gate**, the LED and its resistor were connected between the supply and the **drain**, and the **source** was connected to ground, so the MOSFET acted as a **low-side switch** with a **common ground** shared with the Arduino.

Using `analogWrite()`, I varied the **duty cycle from 0 to 255** (0% to 100%). At a low duty cycle the MOSFET was ON for only a short part of each cycle, so the LED looked dim. As the duty cycle increased, the LED got brighter, and at full duty it was fully ON. The switching is fast enough that the eye sees only the **average power**, not the flicker. I also observed the PWM waveform on the **oscilloscope** and saw the pulse width change with the duty cycle.

During this task, I learned how a **MOSFET works as an electronic switch** controlled by a small gate voltage with almost no gate current, and how **PWM** delivers variable power by changing the ON time instead of the voltage. I also learned why a **gate pull-down resistor** keeps the MOSFET off when the pin is not driven, why a **series resistor** protects the LED, and why switching is more **efficient** than reducing power with a resistor, since a MOSFET that is fully ON or fully OFF wastes very little energy as heat.

This task enhanced my understanding of **PWM control**, **MOSFET switching** and **efficient power delivery**, as used in LED dimmers, motor speed controllers, fan controllers, DC-DC converters and electric vehicle lighting.

Finally, I successfully completed the **LED Brightness Control Using PWM and MOSFET**, understanding how MOSFETs operate as switches and how PWM controls power delivery efficiently.

<img src="https://github.com/bhargavabm/images/blob/main/d37ec0bd-641a-47e0-8166-e151f75770ca.jpg?raw=true"
     alt="PWM LED Brightness Control Circuit in Tinkercad"
     width="800">

---

# Task 15 - AC to DC Conversion and Observing Direct DC vs. Rectified DC (Power Electronics)

**Objective:** Simulate an AC-like signal using the **Arduino's PWM output**, then convert it to DC using **half-wave rectification**. Use a **diode** to block the negative cycle and a **capacitor** to filter the signal, producing rectified DC. Compare the **LED brightness** when powered by a direct DC source (battery or supply rail) with the rectified DC output.

**Outcomes and Learnings:** I successfully built and simulated a **half-wave rectifier circuit** in **Tinkercad** using an **Arduino Uno**, a **1N4007 diode**, a **470 µF polarised capacitor**, two **LEDs**, **220 Ω resistors** and an **oscilloscope**. The Arduino generated a **50 Hz square-wave signal** on pin **D9**, which was fed to the diode. The diode passed only the positive half-cycle and blocked the rest, giving **pulsating DC**.

When the capacitor was added across the output, it charged on each peak and discharged slowly into the LED between pulses, so the output became **smoother DC with a small ripple**. On the oscilloscope, I compared the signal at the source, the **rectified pulses without the capacitor**, and the **filtered DC with the capacitor**. The filtered output was about **4.3 V**, which is the 5 V signal minus the **0.7 V diode drop**. I then compared two LEDs: one powered from the **direct 5 V supply** and one from the **rectified, filtered output**. The directly powered LED was slightly brighter, since it received the full supply voltage with no diode drop or ripple.

During the build, my first circuit used two Arduino pins as the AC source, which swung the capacitor's negative side up and down and made the **polarised capacitor burst** in the simulation. I corrected this by returning the capacitor and LED to a fixed **GND** and learned that a polarised capacitor's **(+) leg must always be at the higher voltage**. I also found that printing to the Serial Monitor inside the loop delayed the signal and made the LED blink, so I removed it and kept the waveform timing steady.

During this task, I learned the principle of **diode rectification**, the **diode voltage drop**, how a **capacitor filter** reduces **ripple**, and the difference between **pulsating DC and stable DC**. I also learned that an Arduino pin only outputs **0 to 5 V**, so it cannot produce a true negative half-cycle, and that a **function generator with a sine wave** shows the negative half being blocked.

This task enhanced my understanding of **AC to DC conversion**, **rectification** and **filtering**, as used in phone chargers, adapters, battery chargers, power supplies and electric vehicle charging systems.

Finally, I successfully completed the **AC to DC Conversion** task, understanding the basics of diode rectification, how filtering improves DC quality, and that LEDs glow brighter on stable direct DC than on filtered rectified DC.

<img src="https://github.com/bhargavabm/images/blob/main/a173ed03-b7a7-4247-b7f9-ca0da2e5b17a.jpg?raw=true"
     alt="Half-Wave Rectifier Circuit in Tinkercad"
     width="800">


---



# Task 17 - Building a Basic H-Bridge Motor Driver using MOSFETs (Power Electronics)

**Objective:** Design and build a basic **H-Bridge motor driver** using **N-channel MOSFETs** that controls the **direction of rotation of a DC motor** using digital signals from an **Arduino**. The H-Bridge connects the motor between two switched half-bridges, so reversing which diagonal pair of transistors is ON reverses the current through the motor.

**Outcomes and Learnings:** I designed and built an **H-Bridge motor driver** using **four IRF830 N-channel MOSFETs**, **two IR2104 half-bridge gate driver ICs**, **four flyback diodes**, **bootstrap diodes and capacitors**, a **DC motor**, a **12 V supply** and an **Arduino**. The circuit has two legs. Each leg has a **high-side** and a **low-side** MOSFET, with the motor connected between the midpoints of the two legs.

Because all four MOSFETs are N-channel, the two high-side MOSFETs need a gate voltage above the supply voltage when they conduct, which an Arduino pin cannot supply. The **IR2104 gate drivers** solved this using a **bootstrap diode and capacitor**, and they also drive the IRF830 gates at about 12 V, since the IRF830 is **not a logic-level MOSFET**. Each driver has a single input, controlled by an Arduino pin, that switches its high-side and low-side MOSFETs in opposite phase, with built-in **dead time** to prevent **shoot-through**.

With the Arduino inputs set one way, the **top-left and bottom-right** MOSFETs conducted and the motor turned **forward**. With the inputs reversed, the **top-right and bottom-left** MOSFETs conducted and the motor turned **in reverse**. Setting both inputs the same stopped the motor. **PWM** on an input reduced the average motor voltage and slowed the motor. Four **flyback diodes** across the MOSFETs gave the motor's inductive kickback a safe path when the transistors switched off.

During this task, I learned how an **H-Bridge** reverses motor direction, why a **high-side N-channel MOSFET needs a bootstrap gate drive**, and the difference between **logic-level and standard MOSFETs**. I also learned why a top and bottom MOSFET on the same leg must **never be ON together (shoot-through)**, how **dead time** protects against it, why **flyback diodes** protect the transistors from inductive spikes, and why the Arduino and the motor supply need a **common ground**. I understood the limits of the IRF830 as well: its high on-resistance means significant voltage drop and heat, so it suits small motors.

This task enhanced my understanding of **MOSFET switching**, **motor driver design** and **direction and speed control**, as used in robots, electric vehicles, drones, conveyor systems and industrial motor drives.

Finally, I completed the **Basic H-Bridge Motor Driver using MOSFETs**, demonstrating control of the rotation direction of a DC motor using an H-Bridge configuration.

<img src="https://github.com/bhargavabm/images/blob/main/30ae3a15-3a74-44bc-b3e9-a8581e21c265.jpg?raw=true"
     alt="H-Bridge Motor Driver Circuit"
     width="800">
<img src="https://github.com/bhargavabm/images/blob/main/cf0bcdba-5b11-4556-bc84-f8b6d29b6fb2.jpg?raw=true"
     alt="Motor Rotating Forward and in Reverse"
     width="800">

---


