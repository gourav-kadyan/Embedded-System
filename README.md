# Embedded-System

##System 

    --Arrangement or a way of working

##Embedded System 

    --Something that is attached to another thing or 
    --Independent System/ part of a large system

##Component of Embedded System

    1 - Hardware 
    2 - Software
    3 - RTOS(realtime operating system) -- used of provide set of rules like automation always there for large scale embedded system

##Characteristic of Embedded System

    1 - Must pe Dependable
        refer to image.png
    2 - Single Functioned --> Need for specific function or work to do 
    3 - Tightly Constrained --> as per cost , size , perfomance , power etc 
    4 - Realtime Operation --> Continuosly sensed enviroment(sensors used) and do tasks on realime (no delay should be there)
    5 - Microprocessors / Microcontroller based --> It should be application specific processor/controller not the general purpose
    6 - Connected(Peripherals) --> like input and output to connect 
    7 - Software --> for more features and flexibility
    8 - Hardware --> for perfomance and security


##RealTime Application and Non Realtime

    -In non-realtime we dont have any time barriers that any constraint that this has to done in that specific time like -- multimedia

    - In realtime it is divided into two -- 
    1 - Soft Realtime ---> 
        - in this we can have some time delay like virtual communication like Meets, Teams, Whatsapp chat

    2 - Hard Realtime ---> 
        - in this we cannot have some time delay like flight system , airbag system etc



##ECU 
    - Electronic Control Unit
    - It is System on Chip (SoC)
    - It is like a brain for System
    - It has multiple multicontrollers
    - It control various electronics/electromechanical system
    - ABS system control


##Autosar 
    --> Hardware --> Autosar --> Application
    --> POSIX based
    --> two types
        1 - Classical Autosar --> based on C
        2 - Adaptive Autosar --> base on C++

#CPU Architecture 

    --> Like a Design 
    --> Mainly Two Types --

##RISC

    --> Reduced Instructor Set Computer 
    --> Fixed Length of Instrutions
    --> Works only on Register to Register 
    --> Single clock cycle (break instruction into simpler than run parallely)
    --> Low cycle per second
    --> Large code size 
    --> Less complex hardware
    --> emphasis on software

##CISC
    
    --> Complex Instructor Set Computer
    --> Flexible Length of Instruction
    --> Work only on Memory to Memory
    --> Multi Clock cycle
    --> High cycle per second
    --> small code size
    --> high complex hardware
    --> emphasis on hardware


##Why we need multicore

    --> if we increase the performance in cput (increase the frequency of clock --> overclock) the power dissipation will increase

    --> thats why we prefer two core instead of overclocked single core

##Requirement of Cpu

    --> Low latency
    --> better power management
    --> safety
    --> increased computation power


##CAN Bus:

    --> High-speed, robust, and suitable for safety-critical applications.
    --> Higher cost and complexity.
    --> speed -- 1 Mbps

##LIN Bus:

    --> Low-speed, cost-effective, and suitable for non-critical applications.
    --> Simplified structure with lower data rates.
    --> speed -- 10 kbps to 100 kbps


#Memory Architecture

##Harvard Architecture

    --> Separate memory for data and instructions(two buses)
    --> separate buses for data and instructions
    --> potentially faster due to parallel access of data and instructions
    --> simultanously fetching data and instructions
    --> parallel access can lead to higher throughput
    --> more complex hardware designs potentially higher cost
    --> use case -- embedded system , digital signal processors

##von Neumann Architecture

    --> Single memory for data and instrutions(single bus)
    --> single bus for data and instrutions
    --> may have slower access due shared bus for data and instructions
    --> sequencially fetching data and instructions
    --> simplicity and flexibility in programming
    --> limited by the speed of a single bus - may be slower
    --> general purpose computing, most modern computers


#Multiprocessors vs Multicontrollers

##Multicontroller

    --> standalone system
    --> typically integrated with cpu, memory and peripherals on a single chip
    --> designed for specific tasks or application, often embedded in devices
    --> Often include integrated peripherals like timers, GPIO(general purpose input and output), ADC(analog to digital convertor) and communication interfaces
    --> optimized for low power consumption, suitable for battery-operated devices
    --> typically simpler in terms of architecture and capabilities 
    --> use case -- embedded system , IOT devices, consumer  electronics
    --> atmel AVR, PIC, ARM Cortex-M

##Multiprocessor 

    --> cpu is a standalone component, and additional components like memory and peripherals are separate 
    --> general purpose and versatile, used in a wide range of applications
    --> relies on external components for peripherals
    --> may have a higher overall cost when additional components are considered
    --> power consumption can vary, may not be as optimized for low power as microcontroller
    --> generally more complex with a broader range of capabilities 
    --> use case - desktop computer, laptops servers, high-performance computing
    --> example -- intel core series, amd ryzen


