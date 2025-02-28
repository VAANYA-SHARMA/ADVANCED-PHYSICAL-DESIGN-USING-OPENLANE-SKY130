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
* **Clock Tree Synthesis (CTS)**  
Clock Tree Synthesis is performed before routing to ensure uniform clock distribution across all sequential elements, minimizing clock skew and optimizing timing performance.  

 **Routing**  
Routing establishes the necessary interconnections between components using designated metal layers. The specifications, including layer thickness and pitch, are defined by the Process Design Kit (PDK). The SKY130 technology node provides six metal layers for routing.  

 **Final Verification and Sign-Off**  
Before fabrication, the design undergoes critical verification steps to ensure functionality, manufacturability, and performance:  

- **Design Rule Check (DRC):** Validates that the physical design complies with manufacturing constraints, preventing layout violations that could lead to fabrication defects.  
- **Layout vs. Schematic (LVS):** Compares the physical layout to the schematic to confirm consistency. Any discrepancies must be resolved before proceeding further.  
- **Static Timing Analysis (STA):** Evaluates the circuit’s timing characteristics to verify compliance with setup and hold time requirements, maximum clock frequency, and overall performance constraints.  



### <br> Introduction To OpenLANE and Strive Chipsets



OpenLANE is an open-source ASIC design flow that streamlines digital design implementation launched by efabless and google. It started as an Open Source Tape - out EXperiment.
<br> Whereas, striVe is a family of **open everything** SoCs (Open PDK, Open EDA, Open RTL) by Efabless.
<br> ![Image](https://github.com/user-attachments/assets/c51b6afe-16c3-4176-aace-0c9d2fb7c3e1)
<br> SOURCE OF IMAGE - VSD-IAT PLATFORM


* _MAIN GOAL_ ~ Produce a clean GDSII with no human intervention (NO Human-In-The_Loop).
* By the term "clean GDSII" we mean,
  - NO LVS VIOLATIONS
  - NO DRC VIOLATIONS
  - NO TIMING VIOLATIONS (still in process)
* It is containerized too...
<br> ![Image](https://github.com/user-attachments/assets/f2f6447e-f078-407b-9734-8234f9ef4bd7)
<br> SOURCE OF IMAGE - VSD-IAT PLATFORM
* Can be used to harden Macros and Chips.
* Two modes of operation
  - Autonomous
  - Interactive
* Design Space Exploration
* Large No. of Design Examples (43 with best configurations, more will be added)

### <br> Introduction To OpenLANE Detailed ASIC Design Flow
<br> ![Image](https://github.com/user-attachments/assets/bca4e985-ba9e-456c-b4e7-3ddd3506f7d1)
<br> SOURCE OF IMAGE - VSD-IAT PLATFORM

OpenLANE is based on many Open source components such as OpenROAD, KLayout, Yosys etc..
The ASIC Design in OpenLANE starts with RTL and ends with GDSII.

The steps :-
+ **SYNTHESIS EXPLORATION** :- It has Delay and Area Report
  <br> ![image](https://github.com/user-attachments/assets/5fff7dd7-cae8-4bd3-a08c-996d037e463f)








  <br> SOURCE OF IMAGE - VSD-IAT PLATFORM.

+ **DESIGN EXPLORATION** :- It generates a report showing design metrics (35 +). Useful for finding best configuration(s) for nay gien design for OpenLANE that result in a clean layout. Report like below is generated.
<br> ![image](https://github.com/user-attachments/assets/3f41143b-9ad2-4965-8a12-9cc28fb6eed1)  <br> SOURCE OF IMAGE - VSD-IAT PLATFORM.

+ **OPENLANE REGRESSION TESTING** <BR> ![image](https://github.com/user-attachments/assets/fe2654ba-0a48-41fb-974b-aa62f6310f79)  <br> SOURCE OF IMAGE - VSD-IAT PLATFORM. 

+ **DESIGN FOR TEST (DFT)** ~ Adds extra logic that helps in testing after fabrication.
<BR> ![image](https://github.com/user-attachments/assets/f0682dab-598f-43b6-bdf5-1ed99b02e4b8)
<br> SOURCE OF IMAGE - VSD-IAT PLATFORM.

+ **PHYSICAL IMPLEMENTATION** ~ <BR> ![image](https://github.com/user-attachments/assets/8b735eae-af08-49d6-b2a3-b80446f471fc) <br> SOURCE OF IMAGE - VSD-IAT PLATFORM.
 

+ ***LOGIC EQUIVALENCE CHECK (AKA LEC)** ~ <BR> ![image](https://github.com/user-attachments/assets/8acc98b9-74b5-43bb-bea2-6b85b6def013) <br> SOURCE OF IMAGE - VSD-IAT PLATFORM.

  - _DEALING WITH ANTENA RULES VIOLATIONS_
  - ![image](https://github.com/user-attachments/assets/41e4f355-0c5b-4fab-9340-2b7284c9ce9e) <BR> SOURCE OF IMAGE - VSD-IAT PLATFORM. 
  - ![image](https://github.com/user-attachments/assets/86efe5aa-4a15-4fa9-80da-a11cc63d7e27) <BR> SOURCE OF IMAGE - VSD-IAT PLATFORM.
  - ![image](https://github.com/user-attachments/assets/5b2730eb-b7b3-46de-9d37-77f856f2f02c)  <BR> SOURCE OF IMAGE - VSD-IAT PLATFORM.
+ **STATIC TIMING ANALYSIS (STA)**
+ **PHYSICAL  VERIFICATION DRC & LVS**  

## <br> Get Familiar to Open-Source EDA Tools
### <br> OpenLANE Directory Structure In Detail
<br>
OpenLANE is a flow rather than a tool, that actually comprises of my EDA tools such as YOSYS, OpenSTA etc..
<br> The primary aim of having a tool like OpenLANE was to make the complete RTL to GDSII flow without any human intervention. This is very much similar to Commercial EDA Tools.


+ **_OPEN SOURCE EXPLORATION_**:-
  1. Open virtual box and then start terminal.
![image](https://github.com/user-attachments/assets/50ea6ab9-00d8-4979-b928-bb6ca65334d5) <br> SOURCE OF IMAGE - AUTHOR
![image](https://github.com/user-attachments/assets/f89204e1-0782-4c0f-a484-39356ca86ffa) <br> SOURCE OF IMAGE - AUTHOR
 > (the command that I've put in is used to CHANGE DIRECTORY to DESKTOP) 
<BR> (Bonus Point ~ To clear the any commands written previously, just type _"clear"_ and click enter)
2. Type in _"cd work/tools/"_ to change to that directory. This is because it conatins/stores the files we require.
  ![image](https://github.com/user-attachments/assets/6a4abe42-5fdd-4f4b-8a85-a236449844f2) <br> SOURCE OF IMAGE - AUTHOR

 3. Now, type in _"ls -ltr"_
    > ls is the linux command for listing. -ltr is the switch for listing files in a specific folder.

<br> ![image](https://github.com/user-attachments/assets/05815aef-4768-4c23-a8fe-47b439c95e1f) <br> SOURCE OF IMAGE - AUTHOR

4. The file we'llbe working in is "openlane_working_dir"; according we put in the command _"cd openalane_working_dir"_ and then _"ls -ltr"_ in order to view the contents of the folder.

<br> ![image](https://github.com/user-attachments/assets/cf88d3de-0c14-4b4f-b960-289163937d9b)
 <br> SOURCE OF THE IMAGE - AUTHOR

5. Let us first explore the pdks, so we change directory by _"cd pdks"_. Then,
_"ls -ltr"_ to list the files. Exploring sky 130A. then list files in this too.
<br> ![image](https://github.com/user-attachments/assets/a470dcda-9be9-4f14-94aa-4db826ef9dab)
<br> SOURCE OF THE IMAGE - AUTHOR

6. Upon exploring the files in sky130A option, we get 2 files;
   - libs.ref ~ Files specific to process and foundries.
   - libs.tech ~ Files specific to tools.
<br> ![image](https://github.com/user-attachments/assets/dc8bc681-06c2-4f01-a66f-e20b535aaac2) <br> SOURCE OF IMAGE - AUTHOR
> BONUS POINT ~ typing the command _"cd ../"_ levels back the directory to the parent directory, this will come in handy below and later.

Let us explore both of them;

![image](https://github.com/user-attachments/assets/cc9c6f2e-f4a8-4a66-8783-cea1ac0c05e4)
<br> SOURCE OF IMAGE - AUTHOR
Here you may notice that the files shown in libs.ref look like specific to technology and libs.tech look specific to tools (magic, ngspice, klayout etc.).

 We'll be working on the file in libs.ref that is _"sky130_fd_sc_hd"_ 
 <br>![image](https://github.com/user-attachments/assets/cd30fd5b-93ca-4a82-b740-3cd0a0a0b40c)
<br> SOURCE OF IMAGE - AUTHOR

Let us explore it further...

<br> ![image](https://github.com/user-attachments/assets/bb5bfa9a-8808-4b3d-b2f2-1b9b87dbd978)

> Here the "lib" file contains all timings related files.
> Here there are "lef" file too.

7. Return back to "openlane_working_dir" and open openlane tool.
<br> ![image](https://github.com/user-attachments/assets/9da60b49-8b7a-4cde-84f3-c9adb77b6d1b)
<br> ![image](https://github.com/user-attachments/assets/ba064b64-0a26-4033-83ba-33a805a39d09)
<br> Source Of images - Author


### <br> Design Preparation Step
To open OpenLane, start by running the Docker command in interactive mode. Once you do that, the terminal prompt will change to _"bash-4.2$"_, indicating that you’re inside the container.  

From there, follow these steps:  

1. Run  _"ls -lrth"_ to check the list of files, sorted by modification time.  
2. Execute _"./flow.tcl -interactive"_ to start OpenLane in interactive mode.  
3. Finally, type _"package require openlane 0.9"_ to load all the necessary components for OpenLane version 0.9.

<br> ![image](https://github.com/user-attachments/assets/aa2bb688-4a9a-47d8-8c08-9151378108c4) <br> SOURCE OF THE IMAGE ~ AUTHOR

> THE DESIGNS RUN BY THE OPENLANE ARE EXTRACTED FROM THE DESIGN FOLDER IN "openlane" DIRECTORY, OUT OF ALL THE DESIGNS WE'LL BE MOST INTERESTED IN "picorv32 a".
<br> ![image](https://github.com/user-attachments/assets/7d6ca1c8-7117-43da-ace4-94f89d608a13) <BR> SOURCE OF IMAGE ~ AUTHOR
> ![image](https://github.com/user-attachments/assets/6617c7e6-4805-4042-b983-a6e14cd54610)
<BR> SOURCE OF IMAGE ~ AUTHOR


8. Now before performing synthesis, we need to prepare required specific files. So we do design prepare setup. We put the command _"prep -design picorv32a"_

   <br> ![image](https://github.com/user-attachments/assets/e058b584-2666-43f8-92e0-08235293a494)
   <br> SOURCE OF IMAGE ~ AUTHOR

   9. Here, a step (as mentioned) was merging the LEF files (l.lef & t.lef), here it can store results. We can see this. <BR> ![image](https://github.com/user-attachments/assets/9b4f21bb-c5dd-43e3-93fd-0baa4858b81c) <BR> SOURCE OF IMAGE - AUTHOR
       
![image](https://github.com/user-attachments/assets/00388f7c-2026-4a39-835c-5b823b1107d7)
    
If you would look at the snapshot above, you would probably notice that in the runs folder there is the time and date of when we launched openlane and in that we have tech related files and it also has _merged.lef_.

### <br> Review Files After Design Prep and Run Synthesis

10. We can open the merged.lef folder by putting in _"less merged.lef"_. Below is what we'll get.

    <br> ![image](https://github.com/user-attachments/assets/8630cb2d-3ebd-4e42-bb8c-5c25a74cf98f)

11. Now, we run synthesis. Go to openlane and type in _"run_synthesis"_. This will run Yosys and ABC synthesis. This might take upto 5 mins (the time can vary).


<br> ![image](https://github.com/user-attachments/assets/304a1c85-a2e8-4b19-ac6a-f325a7a96f15)

<br> ![image](https://github.com/user-attachments/assets/cb182a1f-95a2-49e1-8fd7-29665ba8a40b)

SOURCE OF IMAGES ~ AUTHOR

### <BR> Steps to Characterise Synthesis Results 

Now, our main task will be to find out the FLIP-FLOP RATIO...

(FLIP FLOP RATIO = NO. OF DFF/NO. OF CELLS * 100)

After doing the synthesis, you would be get the printing statistics, this would help u find that ratio..

flip-flop ratio = 14876/1613 *100 = 10.84 %

![image](https://github.com/user-attachments/assets/8dda006e-7991-45f2-b562-38618b311089)

<BR> SOURCE OF IMAGE ~ VSD-IAT PLATFORM


We can look at the results of the synthesis too...

![image](https://github.com/user-attachments/assets/f725df00-2c31-457a-912e-ffa4ef7699c8)
<br> And by putting in command _"less picorv32a.synthesis.v"_ we can get the synthesised netlist..

![image](https://github.com/user-attachments/assets/cea91901-867d-4f80-9997-e0709bf20f80)


In order to check timimgs reports;

<br> ![image](https://github.com/user-attachments/assets/a4bfd774-a06f-4053-a1a3-5cec7676520f)

<br> ![image](https://github.com/user-attachments/assets/d236a509-4f22-47fe-a338-600fc8cf777b)























   





   







































     






