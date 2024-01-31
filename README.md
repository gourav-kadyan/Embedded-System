# Embedded System in Automobiles

## System

In the context of automobiles, the system refers to the integrated network of electronic components and software that work together to control various vehicle functions.

## Embedded System

An embedded system in automobiles is a dedicated computing device designed for a specific function within the vehicle, such as engine control, safety systems, or entertainment.

### Components of Embedded System

1. Hardware
   - Examples: Microcontrollers, sensors, actuators
2. Software
   - Examples: Engine control software, infotainment systems
3. RTOS (Real-Time Operating System)
   - Examples: AUTOSAR (Automotive Open System Architecture)

### Characteristics of Embedded System in Automobiles

1. Must be Dependable
   - Example: Fault-tolerant braking systems to ensure safety
2. Single Functioned
   - Example: Airbag deployment system focused on a specific safety task
3. Tightly Constrained
   - Example: Engine control unit optimized for size, cost, and performance
4. Real-time Operation
   - Example: ABS (Anti-lock Braking System) reacting in real-time to prevent skidding
5. Microprocessors/Microcontroller-based
   - Example: Engine control unit using a specific microcontroller for optimal performance
6. Connected (Peripherals)
   - Example: In-car sensors and actuators connected to the central control unit
7. Software
   - Example: Advanced Driver Assistance Systems (ADAS) providing features like lane departure warning
8. Hardware
   - Example: High-performance computing hardware for autonomous driving systems

### Real-Time Application and Non-Realtime in Automobiles

- **Non-Realtime**
  - Example: Multimedia entertainment systems
- **Realtime**
  1. **Soft Realtime**
     - Example: Adaptive cruise control adjusting speed with some permissible delay
  2. **Hard Realtime**
     - Example: Airbag deployment with immediate response in case of a collision

## ECU (Electronic Control Unit)

The Electronic Control Unit in automobiles is a critical embedded system component acting as the vehicle's central computing hub.

- Examples:
  - **Engine Control Unit (ECU):** Manages fuel injection and ignition timing for optimal engine performance.
  - **ABS Control Unit:** Monitors wheel speed and modulates brake pressure to prevent skidding.

## Autosar

AUTOSAR (Automotive Open System Architecture) is a standardized software architecture for automotive embedded systems.

- Hardware -> Autosar -> Application
- Examples:
  - **Classical Autosar (C):** Used in traditional engine control units.
  - **Adaptive Autosar (C++):** Applied in advanced systems like autonomous driving.

# CPU Architecture in Automobiles

## RISC (Reduced Instruction Set Computer)

RISC architecture in automotive CPUs focuses on simplicity and efficiency.

- Reduced Instruction Set Computer
- Single clock cycle, low cycle per second
- Large code size, less complex hardware
- Emphasis on software
- Examples:
  - **Engine Management Systems:** Use RISC processors for quick and efficient control.
  - **In-Vehicle Infotainment:** RISC processors handle multimedia tasks effectively.

## CISC (Complex Instruction Set Computer)

CISC architecture in automotive CPUs emphasizes versatility and complexity.

- Complex Instruction Set Computer
- Multi-clock cycle, high cycle per second
- Small code size, high complex hardware
- Emphasis on hardware
- Examples:
  - **Autonomous Driving Systems:** Use CISC processors for handling complex algorithms.
  - **In-Car Networking:** CISC processors manage communication protocols efficiently.


# Embedded Systems in Automobiles

## Why We Need Multicore

- Increasing the performance in a single CPU by overclocking leads to higher power dissipation.
- Preferring multiple cores instead of overclocked single core provides a balance between performance and power efficiency.

## Requirements of CPU

- Low latency
- Better power management
- Safety
- Increased computation power

## CAN Bus

- High-speed, robust, and suitable for safety-critical applications.
- Higher cost and complexity.
- Speed: 1 Mbps

**Real-life Example:** 
- In modern automobiles, the CAN bus is extensively used for communication between various control units, such as those managing engine control, anti-lock braking systems (ABS), and airbag deployment.

## LIN Bus

- Low-speed, cost-effective, and suitable for non-critical applications.
- Simplified structure with lower data rates.
- Speed: 10 kbps to 100 kbps

**Real-life Example:** 
- LIN Bus is commonly employed in automotive interiors for non-critical applications like controlling window motors, mirrors, or interior lighting systems.

# Memory Architecture

## Harvard Architecture

- Separate memory for data and instructions (two buses).
- Potentially faster due to parallel access of data and instructions.
- Simultaneously fetching data and instructions.
- Parallel access can lead to higher throughput.
- More complex hardware designs, potentially higher cost.
- Use case: Embedded systems, digital signal processors.

**Real-life Example:** 
- In automotive embedded systems, the Harvard Architecture is applied in engine control units (ECUs) to optimize performance by enabling parallel access to data and instructions.

## von Neumann Architecture

- Single memory for data and instructions (single bus).
- May have slower access due to a shared bus for data and instructions.
- Sequentially fetching data and instructions.
- Simplicity and flexibility in programming.
- Limited by the speed of a single bus - may be slower.
- General-purpose computing, most modern computers.

**Real-life Example:** 
- General-purpose computers in vehicles, like in-car infotainment systems, often use von Neumann Architecture for flexibility in programming.

# Multiprocessors vs Multicontrollers

## Multicontroller

- Standalone system.
- Typically integrated with CPU, memory, and peripherals on a single chip.
- Designed for specific tasks or applications, often embedded in devices.
- Often includes integrated peripherals like timers, GPIO, ADC, and communication interfaces.
- Optimized for low power consumption, suitable for battery-operated devices.
- Typically simpler in terms of architecture and capabilities.
- Use case: Embedded systems, IoT devices, consumer electronics.
- Examples: Atmel AVR, PIC, ARM Cortex-M.

**Real-life Example:** 
- In automotive applications, microcontrollers like ARM Cortex-M are employed in standalone ECUs, managing specific functions like fuel injection or airbag deployment.

## Multiprocessor

- CPU is a standalone component, and additional components like memory and peripherals are separate.
- General-purpose and versatile, used in a wide range of applications.
- Relies on external components for peripherals.
- May have a higher overall cost when additional components are considered.
- Power consumption can vary, may not be as optimized for low power as microcontrollers.
- Generally more complex with a broader range of capabilities.
- Use case: Desktop computers, laptops, servers, high-performance computing.
- Examples: Intel Core series, AMD Ryzen.

**Real-life Example:** 
- In automotive applications, multiprocessors like those in the Intel Core series are used in infotainment systems, providing the computational power needed for multimedia and advanced features.

# Memory

## EEPROM (Electrically Erasable Programmable Read-Only Memory)

- Non-volatile memory.
- Byte-level storage.
- Slower compared to SRAM and Flash.
- Limited write endurance (typically in thousands of cycles).
- Can retain data without power.
- Electrically erasable.
- Used for configuration data, parameter storage.
- Use case: Firmware.

**Real-life Example:**
- EEPROM is commonly used in automotive ECUs for storing configuration parameters, such as engine timing and fuel injection settings.

## SRAM (Static Random-Access Memory)

- Volatile memory.
- Bit-level storage.
- Fastest compared to EEPROM and Flash.
- Cannot retain data without power.
- Erases when there is no power.
- Use case: Register for cache memory.

**Real-life Example:**
- SRAM is employed in automotive control units for cache memory to provide quick access to frequently used data, enhancing processing speed.

## Flash Memory

- Non-volatile memory.
- Block-level storage.
- Slower compared to SRAM and faster than EEPROM.
- Limited write endurance (typically in thousands of cycles).
- Can retain data without power.
- Block erasable (faster than EEPROM).
- Use case: Storage, e.g., in SSDs.

**Real-life Example:**
- Flash memory is widely used in automotive applications for data storage in devices like infotainment systems and navigation units.

# Diagnostic

- Utilizes two CPUs (C1 and C2) and PWM (Pulse Width Modulation) for high-temperature monitoring.
- C1 provides output through PWM, while C2 monitors.
- C2 becomes the primary output provider in case of temperature rise or malfunction in C1/PWM.

**Real-life Example:**
- In an engine control unit (ECU), two processors are employed for redundancy. One monitors and takes over if the other malfunctions, ensuring continuous operation.

# Architectural Approach in Multicore

## Four Main Types

1. **VLIW (Very-Long Instruction Word)**

   - Multicore processor.
   - Parallel processing of tasks.
   - Natural successor to RISC, as it focuses on compiler optimization.

   **Benefits:**
   - Reduced hardware complexity.
   - Shorter cycle time.
   - Power consumption reduction.

**Real-life Example:**
- Modern automotive ECUs use VLIW architecture to process multiple tasks simultaneously, improving overall system efficiency.

2. **Super Scalar**

   - Emphasis on hardware.
   - Executes multiple instructions in parallel.
   - Optimizes performance through parallelism.

**Real-life Example:**
- High-performance computing in vehicles, such as autonomous driving systems, uses Super Scalar architecture for parallel execution of complex algorithms.

3. **Vector**

   - Used in GPUs.
   - Processes multiple data elements simultaneously.
   - Optimized for parallel mathematical operations.

**Real-life Example:**
- Graphics processing units (GPUs) in automotive applications use Vector architecture for parallel processing of graphical data, enhancing visual displays.

4. **Multi-Threading**

   - Allows multiple threads to run concurrently.
   - Improves overall system throughput.
   - Efficiently utilizes CPU resources.

**Real-life Example:**
- Infotainment systems in modern cars use multi-threading to run concurrent processes, ensuring smooth user experiences while simultaneously handling multiple tasks.

# Relevance of Using Multicore

- Critical and non-critical tasks must run parallel without affecting each other.
- Multicore supports running multiple operating systems simultaneously.
- Efficient shared use of processor resources.

**Real-life Example:**
- In an advanced driver-assistance system (ADAS), a multicore processor handles critical tasks like collision detection concurrently with non-critical tasks like infotainment.

# Embedded System Design Process

## 1. Product Specification

- Identifying the required specifications and features for the product.

## 2. Hardware/Software Partitioning

- Deciding which features to implement in hardware and which in software.

## 3. Independent Hardware Software Design Phase

- Developing hardware and software designs independently.

## 4. Hardware Software Integration Phase

- Integrating software and hardware to create a functional system.
- Using SIL (Software in Loop)/MIL (Model in Loop) methodologies.

## 5. Acceptance Testing (Product/System Testing) and Release

- Testing the system using HIL (Hardware In Loop) methods.
- HIL ensures the interaction of hardware and software in a simulated environment.

**Real-life Example:**
- During the development of an advanced braking system, HIL testing is crucial to validate the integration of control algorithms in the ECU with the physical braking components.


                        System Specification          ------------------------
                                 |                                           |
                                 |                                           |
                                 v                                     System Design
                           Functional Design                                  |
                                 |                                            |
                                 V                                            |
                           Architectural Design                               |
                           /                    \        ----------------------
                          /                      \                            |
                         V                        V                           |
               SW generation- co simulation --  Platform Simulation           |
               /                                      \                       |
              /                                        \                Hardware Dev.
             V                                          V                     |
      SW Integration  -- Detailed Co-simulation --  Real HW                   |
                                 |                                            |
                                 V                                            |
            Real Prototype : Validation / Qualification                       |
                                                            ------------------

# Typical Microcontroller Development Cycle 


      +----------------------+
      |   Software           |
      |   Development Cycle  |
      +----------------------+
               |
               v
      +----------------------+
      |      Coders Code     |
      |                      |
      |                      |<----------------+
      |                      |                 ^
      +----------------------+                 |
               |                               |
               v                               |
      +----------------------+                 |
      |      Compilation     |                 |
      |                      |                 |
      |                      |                 |
      |                      |                 |
      +----------------------+                 |
               |                               |
               v                               |
      +----------------------+                 |
      |      Debugger        |                 |
      |                      |                 |
      |                      |                 |
      |                      |                 |
      +----------------------+                 |
               |                               |
               v                               |
      +----------------------+                 |
      |   Bug-Free?          |  No             |
      |        |-------------|---------------->+
      |        v             |                 ^
      |      YES             |                 |
      +----------------------+                 |
               |                               |
               v                               |
      +----------------------+                 |
      |  Next Development    |                 |
      |  Phase (Testing,     |                 |
      |  Deployment, etc.)   |                 |
      +----------------------+                 |
               |                               |
               v                               |
      +----------------------+                 |
      |   Testing on Real    |                 |
      |   Hardware/ECU       |                 |
      |                      |                 |
      |                      |                 |
      +----------------------+                 |
               |                               |
               v                               |
      +----------------------+                 |
      |      Bug-Free?       |    No           |
      |        |-------------|---------------->+
      |        v             |
      |      YES             |
      +----------------------+
               |
               v
      +----------------------+
      |   Production         |
      |   Deployment to      |
      |   Production         |
      +----------------------+


## Cross-Compiler

   - Create  a Hex. file for the other system 
   - example --> Kiel uVision

   - Kiel uVision --> Hex code --> Target Development board(8051/ARM)

# Build Tools

## Tools to Create Hex File

- A Hex file is generated using a build tool chain, which consists of a cross compiler, cross linker, and cross assembler.

## Responsibilities of Build Tools

Build tools are responsible for:

1. Running the program for the target.
2. Replacing the code image on the target.
3. Real-time monitoring of the program execution on the target, including the capability to observe processor registers and status.

## Various Debugger Tools

1. **Instruction Set Simulator (ISS)**
2. **In-Circuit Simulator (ICS)**
3. **In-Circuit Emulator (ICE)**
4. **In-Circuit Debugger (ICD)**

## Definition and Real-Life Automotive Examples

### Instruction Set Simulator (ISS)

- **Definition:** An ISS simulates the execution of instructions without running the actual hardware.
- **Real-Life Automotive Example:** Simulating the control algorithm of an Electronic Control Unit (ECU) without the physical ECU hardware.
- **Additional Points:**
  - ISS is suitable for early software development and algorithm testing.
  - It provides a fast and flexible environment for iterative software development.

### In-Circuit Simulator (ICS)

- **Definition:** ICS simulates the behavior of electronic circuits within a larger system.
- **Real-Life Automotive Example:** Simulating the behavior of a car's electronic control system, including sensors and actuators.
- **Additional Points:**
  - ICS is used for system-level testing and verification.
  - It allows testing complex systems before the availability of physical hardware.

### In-Circuit Emulator (ICE)

- **Definition:** An ICE emulates the entire microcontroller or processor, allowing software development and testing on actual hardware.
- **Real-Life Automotive Example:** Emulating an ABS module to test braking algorithms without the actual ABS unit.
- **Additional Points:**
  - ICE provides a more accurate representation of the target system.
  - It is useful for software development and testing in a real hardware environment.

### In-Circuit Debugger (ICD)

- **Definition:** ICD allows developers to observe and control the execution of code in real hardware.
- **Real-Life Automotive Example:** Debugging the firmware of an Engine Control Unit (ECU) in a running vehicle.
- **Additional Points:**
  - ICD provides real-time insight into code execution on the physical device.
  - It is crucial for identifying and fixing issues during software development.

## Usage in Automotive Development

In the automotive development process, these tools are vital for:

- Developing and testing control algorithms for various vehicle functions.
- Verifying the behavior of embedded systems in a simulated or emulated environment.
- Debugging and optimizing the software running on Electronic Control Units (ECUs).
- Ensuring the reliability and safety of automotive software through thorough testing and debugging processes.


# Microcontroller and Timer Information

## ECU and Microcontrollers

- Inside 1 ECU, there may be multiple microcontrollers.
- An ECU can have multiple cores/CPU, and for ADAS applications, TDAx from Texas Instruments is commonly used.

## Timers in Microcontrollers

### Timer Basics

Timers in microcontrollers are hardware components used for precise timing. Here's a basic overview:

- **Counting Units:** The "8-bit" and "16-bit" descriptors refer to the number of bits the timer can count up to.
  
### Uses of Timers

1. **Generating Time Delays:** Timers create accurate time delays in programs.
2. **Pulse Width Modulation (PWM):** Timers generate PWM signals for controlling analog devices.
3. **Measuring Time Intervals:** Timers measure the duration of events.
4. **Real-time Clocks:** Timers can function as real-time clocks.
5. **Capturing External Events:** Timers can timestamp external events.

### Timer Configuration

Microcontrollers have registers and settings to configure timers, including counting direction, initial value, and clock signal source.

### Interrupts

Timers often work with interrupts, triggered when a specific value is reached.

## Arduino Uno Overview

The Arduino Uno is a popular and versatile board for beginners:

- **Microcontroller:** ATmega328 from AVR family.
- **Clock Speed:** 16 MHz.
- **Memory:**
  - Flash: 32 KB.
  - SRAM: 2 KB.
  - EEPROM: 1 KB.
- **Digital I/O Pins:** 14.
- **Analog Input Pins:** 6.
- **PWM Pins:** 6.
- **Interfaces:** UART, SPI, I2C.
- **USB Connection:** Standard USB Type-B.
- **Power Supply:** 5V.
- **Reset Button, LEDs, Open-Source.**

## Microcontroller Comparison: Modern 8051 vs. Arduino Uno

1. **Input/Output Lines:**
   - Modern 8051: 32.
   - Arduino Uno: 23.

2. **Internal Data (RAM) Memory:**
   - Modern 8051: 256 bytes SRAM.
   - Arduino Uno: 2 KB SRAM.

3. **Internal Data (EEPROM) Memory:**
   - Modern 8051: No specific mention.
   - Arduino Uno: 1 KB EEPROM.

4. **ROM Memory (Flash Program Memory):**
   - Modern 8051: Up to 64 KB.
   - Arduino Uno: 32 KB.

5. **Timers/Counters:**
   - Modern 8051: Three timers (16-bit).
   - Arduino Uno: Three timers (Two 8-bit / One 16-bit).

6. **A/D Converter:**
   - Modern 8051: Not specified.
   - Arduino Uno: 10-bit A/D converter, Six Channels.

7. **PWM (Pulse Width Modulation):**
   - Modern 8051: Not specified.
   - Arduino Uno: Six PWM channels.

Always refer to datasheets for precise details.

## Temperature Ranges in Microcontrollers

1. **Temperature Ranges:**
   - Consumer Grade: 0°C to 70°C (extended to 85°C).
   - Industrial Grade: -40°C to 85°C.
   - High Temperature Products: Above 85°C (e.g., 105°C, 125°C, 150°C).

2. **Automotive-Grade Processors:**
   - Definition: Tested to meet AEC-Q100 standards.
   - AEC-Q100 Standards: Ensure durability in automotive conditions.
   - Temperature Considerations: Must operate reliably across a wide range, meeting specific temperature levels.

## Texas Instruments MSP430F20x Microcontrollers

1. **Microcontroller Type:** MSP430 (16-bit).
2. **Temperature Specifications:** Operates up to 85°C or 105°C.
3. **AEC-Q100 Qualification:** Qualified up to 105°C.
4. **Grade 2 Identification:** Identified as Grade 2 in AEC-Q100.
5. **Usage Limitation in Engine Compartment:** Not suitable for high-temperature engine compartments.
6. **Application Focus - Cabin Applications:** Used for lighting control, HVAC, and keyless entry within the vehicle cabin.
7. **Significance:** Enhances comfort and convenience in the vehicle cabin.

## Qorivva MPC55xx Microcontrollers

1. **Microcontroller Type:** 32-bit based on Power Architecture.
2. **Application Focus:** Engine Management, Advanced Driver Assistance, Central Body Systems, Gateway Applications.
3. **Key Benefits for Automotive Designers:**
   - Software and Hardware Compatibility.
   - Scalability.
   - Embedded Flash Experience.
   - Efficiency through Parallel Processing.
   - Power Architecture Ecosystem.
4. **Practical Implications:** Adaptable and efficient for various automotive applications.
5. **Significance in Automotive Systems:** Manages and enhances performance, safety, and functionality.

## Qorivva MPC577xK for ADAS

1. **Microcontroller Type:** 32-bit based on Power Architecture.
2. **Application Focus:** Next-gen radar-based Advanced Driver Assistance Systems (ADAS).
3. **Integration and Performance:**
   - High integration for digital and analog components.
   - Reduction in external components.
4. **Complete Radar Solution:** Combined with MR2001 chipset for comprehensive ADAS functionalities.
5. **SafeAssure Functional Safety Solutions:** Adheres to safety standards for reliable ADAS operation.
6. **Practical Benefits:** Streamlined and integrated solution for ADAS applications.
7. **ADAS Applications:** Radar-based systems for adaptive cruise control, emergency braking, and blind-spot detection.

## AURIX Microcontrollers

1. **Microcontroller Family:** AURIX by Infineon, designed for automotive industry.
2. **Multicore Architecture:** Up to three independent 32-bit TriCore™ CPUs.
3. **Safety Standards:** Emphasis on meeting the highest safety standards.
4. **Performance Enhancement:** Balances increased performance with a focus on safety.
5. **Versatility in Applications:** Single platform for powertrain, body, safety, and ADAS applications.
6. **Single MCU Platform:** Controls various applications with a single MCU platform.
7. **Practical Implementation:** Versatile solution for high-performance and safety-critical automotive systems.

