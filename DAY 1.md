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
<BR> Below is the example f an RISC V. Out of many blocks seen below, some are specified as _FOUNDRY IPs_. Others are _MACROS_. And If we wish to manufacture this chip, we'll be contacting the _FOUNDRY_.

##### _IMPORTANT TERMINOLOGIES_

<br> 1.**PACKAGE:-** ***The case which has the chip and is connected to the circuit board. It is kind of a housing in which the chip is placed.***
<br> 2.**WIRE BONDS:-** ***Through which the chip is connected to the package and the outside signals are received by the chip.***
<br> 3.**Pads:-** ***Through which we can send in the signals to the chip or recive the signals from the chip.***
<br> 4.**CORE:-** ***Where all the logic sits. All the AND, NOT gates and the MUXES are placed here.***
<br> 5.**DIE:-** ***It is basically, the size of the entire chip.***
<br> 6.**FOUNDRY:-** ***It is a very critical term for chip design. It is a like a big factory with many large machines. It is where the chip gets manufactured.***
<br> 7.**IPs:-** ***Intellectual Property. It requires some _intelligence_ to be built.***
<br> 1.**MACROs:-** ***They are pure logic based.***




  




