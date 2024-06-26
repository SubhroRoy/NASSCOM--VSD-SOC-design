# NASSCOM--VSD-SOC-design
# DAY 1 <br> 
## Introduction to open-source EDA, openLANE, skywater130 pdk and prerequisites. <br>
### Introduction to Packages for design, open-source EDA, openLANE and skywater130 pdk.
#### Introduction to QFN-48 Package. <br>
AUDRINO Board <br>
<figcaption style="text-align:center;">
<img width="259" alt="image" src="https://github.com/SubhroRoy/NASSCOM--VSD-SOC-design/assets/169291565/0d8ec951-9f47-4df3-a18a-f55aef344ba7">
 <img width="480" alt="image" src="https://github.com/SubhroRoy/NASSCOM--VSD-SOC-design/assets/169291565/ee9e2175-37df-4b46-96b9-523aa81d5653">
 <br>
FIG 1.1.1: AUDRINO BOARD and block diagram for the board
</figcaption> <br><br>
In Fig. 1.1.1, circled in yellow, is the chip in focus. Here we can see the chip and the block diagram. The block diagram shows the processor with the interface connections. 
<br><br>

<figcaption style="text-align:center;">
<img width="300" alt="image" src="https://github.com/SubhroRoy/NASSCOM--VSD-SOC-design/assets/169291565/55393ac9-4072-4522-90cf-cf48fa148cdc"> 
<img width="407" alt="image" src="https://github.com/SubhroRoy/NASSCOM--VSD-SOC-design/assets/169291565/cc6bfd37-ac02-4646-b07c-6c7c6ac081ee">
<img width="371" alt="image" src="https://github.com/SubhroRoy/NASSCOM--VSD-SOC-design/assets/169291565/fde7311b-5a2a-417b-a71b-f0cd4d2a8c79">
<img width="468" alt="image" src="https://github.com/SubhroRoy/NASSCOM--VSD-SOC-design/assets/169291565/563ad6ab-5374-4efe-9a68-551f422d64b0">
<br>
FIG 1.1.2: (i-top left)Chip structure in a QFN-48 package,(ii-top right)CHIP Inside: PADS, Core, Die, (iii-bottom left)RISC V SOC sample and (iv-bottom right) RISC V SOC core blocks.
</figcaption> <br><br>
If we take the chip in question and remove the cover. We will see the chip structure as seen above. It is a QFN-48 package structure i.e. Quad Flat No-Leads structure with 48 pins. The chip sits in the middle of the package and is connected to the pins using wire bonds. <br><br>

**Components of the CHIP :** <br>
**CORE**: Where all the logic sits.<br>
**DIE**: Size of the chip.<br>
**PADS**: Used to send the signals inside the chip. <br>

A typical RISC-V SoC core consists of: <br>
**Foundry IPs**(Intellectual Property) SRAM, ADC, DAC, PLL. <br>
**MACROS**(purely digital blocks) SPI, RISC V SOC. <BR>

#### Introduction to RISC V.
**RISC V ISA** (Instruction Set Architecture) --
This is the language of the computers, this is how we talk to the computer. <br>
<figcaption style="text-align:center;">
<img width="547" alt="image" src="https://github.com/SubhroRoy/NASSCOM--VSD-SOC-design/assets/169291565/c1c30821-8337-433a-9b22-0307301b50d3">
<br>
FIG 1.1.3: C-program, RTL implementation, and equivalent layout design. 
</figcaption> <br><br>

In FIG 1.1.3 we can see that the C-program is compiled to its RISC V assembly language program. <br> 
This assembly language program is then converted to its machine language program. In this case, it is stored in a hexadecimal format and then converted to the binary format, which the machine understands. <br>
The bits get executed inside the layout and we get the output. <br>
The HDL(Hardware Descriptive Language) acts as an interface between the RISC V architecture and the layout design. In this, the implementation is done using an RTL code. <br>
So, the RISC V architecture is implemented using an RTL code, after that the RTL to GDSII is performed to get the Layout. 

#### From software application to hardware.
<figcaption style="text-align:center;">
<img width="534" alt="image" src="https://github.com/SubhroRoy/NASSCOM--VSD-SOC-design/assets/169291565/5cc10af1-5d13-4321-b460-929c8bca4378">
<br>
FIG 1.1.4: Flow application software to system software to hardware. 
</figcaption> <br><br>

In FIG 1.1.4 we can see the structure of the system software.<br><br>
Major components of system software are:
* Operating system. <br>
The primary function of operating system is to convert application software into its respective assembly-level program and subsequently into its binary-level program, which the machine can understand. Additionally, it handles I/O operations, allocates memory, and performs low-level system functions. <br>

* Compiler. <br>
The compiler converts small functions in C, C++, JAVA, etc language to instructions. These instructions are to be fed to the hardware. Therefore, the syntax of these instructions depends on what the hardware needs. For example, if the hardware is of a RISC V architecture then the instructions must be of a RISC V architecture. These instructions are present in a .exe file, which is the output of a compiler. <br>
* Assembler. <br>
The assembler converts the instructions generated from the compiler to 1's and 0's i.e. respective binary language, which the hardware understands. <br>

<figcaption style="text-align:center;">
<img width="544" alt="image" src="https://github.com/SubhroRoy/NASSCOM--VSD-SOC-design/assets/169291565/a10f6205-1e5f-46da-892e-61ea84a59077">
<br>
FIG 1.1.5: Stop Watch example. 
</figcaption> <br><br>

<figcaption style="text-align:center;">
<img width="596" alt="image" src="https://github.com/SubhroRoy/NASSCOM--VSD-SOC-design/assets/169291565/b5bfa7ae-c882-410a-b08c-41b5a404d361">
<br>
FIG 1.1.6: Compiler and assembler I/O for stop watch example
</figcaption> <br><br>

<figcaption style="text-align:center;">
<img width="555" alt="image" src="https://github.com/SubhroRoy/NASSCOM--VSD-SOC-design/assets/169291565/9e0f3de6-f74b-4bb6-bb22-09fd354eb5a7">
<br>
FIG 1.1.7: Instruction set generated in compiler for RISC V architecture acts as an abstract interface between C-language and Hardware.  
</figcaption> <br>
This is how the user interacts with the computer/hardware.<br><br>
In FIG 1.1.5 and FIG 1.1.6 shows a stop watch operation and its respective compiler and assembler input and output. <br><br>

<figcaption style="text-align:center;">
<img width="539" alt="image" src="https://github.com/SubhroRoy/NASSCOM--VSD-SOC-design/assets/169291565/f1b19908-0762-4a43-b79a-c02361b6314f">
<br>
FIG 1.1.7: Physical Design Implementation from software to hardware  
</figcaption> <br><br>


* SOC design and openLANE.
* Get familiar with open-source EDA tools.
<br><br>
  
PICORV32A PREP DONE
![image](https://github.com/SubhroRoy/NASSCOM--VSD-SOC-design/assets/169291565/05c30919-36f8-4d64-a5e2-2b652adeb588)
