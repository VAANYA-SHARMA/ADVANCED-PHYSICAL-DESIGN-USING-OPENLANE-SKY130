# SKY130 Day 1: Inception of OpenSource EDA, OpenLANE and SKY130 PDK
## <br> How to Talk to Computers
### <br> Introduction to QFN - 48 package, chip, pads, core, die and IPs
<br>
<br> Let us take an example of a typical circuitary board (arduino board). 

<br> ![Alt text](https://github.com/VAANYA-SHARMA/ADVANCED-PHYSICAL-DESIGN-USING-OPENLANE-SKY130/blob/main/Screenshot%202025-01-27%20142440.png
)
source of the image- VSD-IAT PLATORM
<br> The industry of chip design, the thing we have main focus on lies the that tiny black thing highlighted in below image. That highlighted thing is basically a processor.
<br> ![WhatsApp Image 2024-03-22 at 20 42 40_546c53fa](https://github.com/VAANYA-SHARMA/Advanced-Physical-Design-using-OPENLANE-Sky-130/assets/163661889/77287e70-be46-4858-9855-655b4036fe4d)
<br> source of the image- VSD-IAT PLATORM
<br> Let us now represent this _processor (chip)_ and surroundings using block diagram. For designing such a circuit, we would first need to represent it using a block diagram.
<br> Like this :-
<br> ![WhatsApp Image 2024-03-22 at 20 42 53_c0279c2d](https://github.com/VAANYA-SHARMA/Advanced-Physical-Design-using-OPENLANE-Sky-130/assets/163661889/e4aa7533-886a-483b-b1ec-ad111819a3db)
<br> Well rather than calling this a chip, we'll call it a _package_ and they are named also. Like the below image is of Package QFN-48 Quad Flat No-leads. The below shows the inside of a package. The size of this below is 7mm by 7mm, but it can definitely vary.
<br> ![Image](https://github.com/user-attachments/assets/192ac6c3-f0cd-49ce-a143-e2f7f1a279a6)
<br> SOURCE OF THE IMAGE - VSDIAT PLATFORM

<br> The actual chip lies somewhere in the center of the package and is connected to the pins like below; the white strand - like structure are known as _wire bonds_ . The pins that the wire bonds connect transfer the signal from the outside world to the chip.
<BR> ![WhatsApp Image 2024-03-22 at 20 43 09_46be60ff](https://github.com/VAANYA-SHARMA/Advanced-Physical-Design-using-OPENLANE-Sky-130/assets/163661889/cae4a683-eabd-421e-a0bd-f1d08eecb9fe) 
<br> SOURCE OF THE IMAGE - VSDIAT PLATFORM
<br> Now, there are some important components of the chip, _PADS_, _CORE_ & _DIE_.
![WhatsApp Image 2024-03-22 at 20 43 20_67d9d238](https://github.com/VAANYA-SHARMA/Advanced-Physical-Design-using-OPENLANE-Sky-130/assets/163661889/4aafde57-5a33-4864-a7fb-0f7b566c83fa)
<br> SOURCE OF THE IMAGE - VSDIAT PLATFORM

* PADS - THESES ARE LIKE DOORS IN THIS. THEY TRANSFER SIGNALS FROM OUTSIDE TO INSIDE.
* CORE - THIS IS WHERE THE ALL THE LOGIC SITS.
* DIE - THIS IS THE PERIMETER/MEASURE OF THE BORDER OF THE CHIP (SIZE OF THE CHIP). THIS IS WHAT IS ESSENTIALY PRINTED ON A SILICON PAPER.

- A typical chip essentialy contains A SoC, SRAM, PLL, SPI and a couple of other components.
<br> ![Image](https://github.com/user-attachments/assets/3c37f1bb-b281-499b-8568-b912d3a77d2f)
SOURCE OF IMAGE - VSD-IAT PLATFORM
<BR> Below is the example f an RISC V. Out of many blocks seen below, some are specified as _FOUNDRY IPs_. Others are _MACROS_. And If we wish to manufacture this chip, we'll be constantly contacting the _FOUNDRY_. We would have to maintain contact with the foundry using some interface. This interface might be a file that the foundry provides us with.


##### <br> _IMPORTANT TERMINOLOGIES_

<br> 1.**PACKAGE:-** ***The case which has the chip and is connected to the circuit board. It is kind of a housing in which the chip is placed.***
<br> 2.**WIRE BONDS:-** ***Through which the chip is connected to the package and the outside signals are received by the chip.***
<br> 3.**Pads:-** ***Through which we can send in the signals to the chip or recive the signals from the chip.***
<br> 4.**CORE:-** ***Where all the logic sits. All the AND, NOT gates and the MUXES are placed here.***
<br> 5.**DIE:-** ***It is basically, the size of the entire chip.***
<br> 6.**FOUNDRY:-** ***It is a very critical term for chip design. It is a like a big factory with many large machines. It is where the chip gets manufactured.***
<br> 7.**IPs:-** ***Intellectual Property. It requires some _intelligence_ to be built.***
<br> 1.**MACROs:-** ***They are pure logic based.***

 ### <br> <BR> <BR> Introduction To RISC V
 RISC V ISA ~  RISC V Instructions Set Architecture. If a C program is to be run on a hardware with a particular layout, we need to pass it in a specific flow. 
 + First, C program is converted to ASSEMBLY LANGUAGE PROGRAM (here it will be RISC V ASSEMBLY LANGUAGE PROGRAM).
 + Then this is converted to MACHINE/BINARY LANGUAGE PROGRAM.
 + Then this is fitted in layout
Betweeen RISC V architecture and LAYout there is another interface, HARWARE DESCRIPTION LANGUAGE, this is in essence the implementation (picorv32).


### <BR> <BR> From Software Applications to Hardware

<BR> _APPLICATION SOFTWARE OR APPS_, as generally they are called, runs on a wide range of hardware, including mobile phones, laptops, and other devices as they include chip.
<br> _HOW DO THESE SOFTWARES WORK ON OUR COMPUTERS??_
* First they enter a block, known as *SYSTEM SOFTWARE*. This converts this software into binary format which can be understood by the hardware. Output of OS are small functions in C, C++ OR JAVA script. Let's look into this in a detailed manner;
  + System Software has layers/parts:-
    - *OPERATING SYSTEM/OS* ~ Operating system has the following jobs:-
      <BR> } CONTROLS IO OPERATIONS
      <BR> } CONTROLS/ALLOCATES MEMORY
      <BR> } MAIN TASK OF OS - TAKES THE APP AND COVERTS INTO THE APP'S RESPECTIVE ASSEMBLY LANGUAGE PROGRAM.
   - *COMPILER* ~ Converts the input functions by OS into instructions. The syntax of these instructions depends on the type of hardware. If the hardware is of RISC V CPU, then the instructions will be in RISC V format.
   - *ASSEMBLER* ~ Converts the instructions into respective _BINARY LANGUAGE_ also known as _MACHINE LANGUAGE PROGRAM_. Well, the name is pretty much self explanatory.
     + This Binary Output(Logic 0 and Logic 1) is understood by hardware.
* Later or sooner, the output is Binary Output that is understood by hardware.
<br> ![Image](https://github.com/user-attachments/assets/502ce408-33a4-4722-866c-91db17a6c807)
<br> SOURCE OF IMAGE - VSD -IAT PLATFORM.
<BR> The output of Compiler i.e. the instructions act as a _ABSTRACT INTERFACE_ between the C language and the hardware. And therefore it is known as INSTRUCTION SET ARCHITECTURE or ARCHITECTURE OF COMPUTER.
 
## <br> SoC Design and OpenLANE
### <br> Introduction to All Components of Opensource Digital ASIC Design
<br> **_ASIC DESIGN_** ~ DIGITAL APPLICATION INTEGRATED CIRCUIT designing requires some components:- 
+ RTL IPs (HARDWRAE DESCRIPTION LANGUAGE)
+ EDA TOOLS
+ PDK DATA

For 100 % OPEN SOURCE ASIC DESIGN, WE NEED THE ABOVE LISTED ELEMENTS AS OPEN SOURCE.

 - RTL Designs- BLOCKS WRITTEN HARDWARE DESCRIPTION LANGUAGE ~ GITHUB, OPENCORES ...
 - EDA Tools - ELECTRONIC DESIGNING AUTOMATION tools ~ OPENROAD, OPENLANE ...
 - PDK Data ~ DO WE HAVE OPEN SOURCE PDK?? WELL, WHAT IS PDK?? LET US KNOW...
<BR> _*PDK*_ denotes Process Design Kits. This is the interface b/w FAB and the designers. This is the collection of files used to model a fabrication process for the EDA tools used to design an integrated circuit.
<br> We have OPEN SOURCE PDK as well. This is by Google and Skywater ~ FOSS 130nm PRODUCTION PDK.
<br> Well, now we think about it, we might have a question popped that _IS 130nm OLD AND NOT IN USE?_
<BR> Well, NO! Well, it actually conforms to industrial requirements.

<br> Well, the idea of 130nm not being handy doesn’t hold up for two main reasons:

1. Many applications don’t actually need advanced nodes, and 130nm chips provide enough power for those situations.
2. The cost of making 130nm chips is much lower.

<br> To mention, these 130nm tech isn't slow too... To clarify, kindly refer to below;

<br> ![Image](https://github.com/user-attachments/assets/ca5c8146-cb4c-4021-8c3b-e4af7d0c25d2)
<BR> SOURCE OF IMAGE - VSD-IAT PLATFORM


Now that we have all enablers/requirements, are we really ready to ASIC design...

### <br> Simplified RTL TO GDSII FLOW

<br> Well RTL to GDS II process has many steps:-
* **SYNTHESIS** ~ converts RTL (HARDWARE DESCRIPTION LANGUAGE) to a circuit out of components (GATE LEVEL) from the standard cell library (SCL)
<BR> ![Image](https://github.com/user-attachments/assets/7539c931-128b-4746-80da-582d0a13d128)
<BR> SOURCE OF IMAGE - VSD-IAT PLATFORM
* **FLOOR AND POWER PLANNING** ~ planning the implementation of macro, or whole chip and the silicon area.
<BR> -MACRO FLOOR PLANNING ~ DIMENSIONS, PIN LOCATIONS, ROWS DEFINED ET CETERA...
<br> ![Image](https://github.com/user-attachments/assets/ff47aab5-94cf-46a8-aaa0-f47b44aafac2)
<BR> -CHIP FLOOR PLANNING ~ CHIP DIE PARTITION, I/O PADS PLACEMENT ETC. ...
<br> ![Image](https://github.com/user-attachments/assets/511ad851-bbb3-46ee-b860-7d8f224134b0)
<BR> -POWER PLANNING ~ to reduce the wire length, resistance and make the chip planned well
<BR> ![Image](https://github.com/user-attachments/assets/1367f6b5-1618-4f5f-9874-fc22522b69b4)

* **PLACEMENT** ~ placing the cells on the floorplan rows, aligned with the sites.
  - GLOBAL - CELLS MIGHT OVERLAP
  - DETAILED - ALTERED GLOBAL PLACEMENTS.
*  








