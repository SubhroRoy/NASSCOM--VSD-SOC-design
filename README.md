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
FIG 1.1.6: Compiler and assembler I/O for stopwatch example
</figcaption> <br><br>

<figcaption style="text-align:center;">
<img width="555" alt="image" src="https://github.com/SubhroRoy/NASSCOM--VSD-SOC-design/assets/169291565/9e0f3de6-f74b-4bb6-bb22-09fd354eb5a7">
<br>
FIG 1.1.7: The instruction set generated in the compiler for RISC V architecture acts as an abstract interface between C-language and Hardware.  
</figcaption> <br>
This is how the user interacts with the computer/hardware.<br><br>
FIG 1.1.5 and FIG 1.1.6 show a stopwatch operation and its respective compiler and assembler input and output. <br><br>

<figcaption style="text-align:center;">
<img width="603" alt="image" src="https://github.com/user-attachments/assets/4c844bbb-9117-4bd5-aef5-6490ba584001">
<br>
FIG 1.1.8: ADD instruction read by hardware from its RISC V binary format  
</figcaption> <br><br> 

<figcaption style="text-align:center;">
<img width="539" alt="image" src="https://github.com/SubhroRoy/NASSCOM--VSD-SOC-design/assets/169291565/f1b19908-0762-4a43-b79a-c02361b6314f">
<br>
FIG 1.1.9: Physical Design Implementation from software to hardware  
</figcaption> <br><br>

<figcaption style="text-align:center;">
<img width="601" alt="image" src="https://github.com/user-attachments/assets/022f8118-6b93-4db6-aba5-29378f14682e">
<br>
FIG 1.1.10: Basic sections of the course  
</figcaption> <br><br>

We will deal with Part 1 i.e. RISC-V ISA (Instruction Set Architecture).<br>

### Contents of the course: SOC design and openLANE.
#### OpenSource ASIC design
In this section, we discuss SoC Design Using OpenLANE by Mohamed Shalan.<br>
<figcaption style="text-align:center;">
<img width="561" alt="image" src="https://github.com/user-attachments/assets/62f57f6c-0e1b-47a8-8ad2-3d7784e0e9e8">
<br>
FIG 1.2.1: Components that make digital ASIC design  
</figcaption> <br><br> 

VLSI Design companies are mostly divided into Pure Play FABs and FABLESS design companies.<br>
PDK (Process Design Kit) is the interface between the FAB and the designers. PDK includes :
1. Process Design Rules: DRC, LVS, PEX
2. Device Models
3. Digital Standard cell libraries
4. I/O Libraries
5. Much more sensitive information cannot be disclosed to the masses. Thus the information was protected by Non-Discloser Agreements.

But now we have an opensource PDK with the help of Google and Skywater.<br>
<figcaption style="text-align:center;">
<img width="584" alt="image" src="https://github.com/user-attachments/assets/7c569398-b287-4d4f-8ca6-74a74036390e">
<br>
FIG 1.2.2: Open Source PDK  
</figcaption> <br><br> 

<figcaption style="text-align:center;">
<img width="557" alt="image" src="https://github.com/user-attachments/assets/7ee1c669-9dce-45c8-a55b-fc0c574d074d">
<br>
FIG 1.2.3: Components that make OpenSource digital ASIC design
</figcaption> <br><br> 

<figcaption style="text-align:center;">
<img width="602" alt="image" src="https://github.com/user-attachments/assets/a478686a-1ad3-48ff-bf07-4e4f3d4712f9">
<br>
 FIG 1.2.4: Speed of 130nm process.
</figcaption> <br><br> 
The objective of the ASIC design flow is to take the design from the RTL level to the GDSII for the final layout.<br>

#### Simplified RTL to GDSII Flow

<figcaption style="text-align:center;">
<img width="605" alt="image" src="https://github.com/user-attachments/assets/d9482c1e-f758-4246-8c09-bc8a2fb8ddd9">
<br>
 FIG 1.2.5: Simplified RTL to GDSII flow.
</figcaption> <br><br> 
Synthesis:<br>
<img width="371" alt="image" src="https://github.com/user-attachments/assets/f8be1c08-6d37-452b-b75a-3f184ec7d99f">
<img width="374" alt="image" src="https://github.com/user-attachments/assets/09cd34ed-29f6-48ff-b3ea-b7aa8896743a">
<br>

Floor and Power Planning : <br>
<img width="366" alt="image" src="https://github.com/user-attachments/assets/c6595985-d79c-416f-acef-0d7033439bf0">
<img width="327" alt="image" src="https://github.com/user-attachments/assets/fd9039b0-94b5-485d-94a4-3e0e9c6bf607">
<img width="289" alt="image" src="https://github.com/user-attachments/assets/89581503-ef2d-48c4-b64f-bab8ad0d561a">
<br>

Placement : <br>
<img width="353" alt="image" src="https://github.com/user-attachments/assets/b54a3228-4d76-45b8-b385-bef97c64b61f">
<br>

Placement is done in 2 steps global and detailed.<br>
<img width="346" alt="image" src="https://github.com/user-attachments/assets/f8ec667e-a828-4e62-80f9-8e66107ba49b">
<br>

Routing can be seen in 2 steps 
1. Clock Tree Synthesis.
2. Signal Routing.

Clock Tree Synthesis:<br>
<img width="372" alt="image" src="https://github.com/user-attachments/assets/cf5dece5-41d7-425c-bd69-d183eb11419d">
<br>

Signal Routing: <br>
<img width="368" alt="image" src="https://github.com/user-attachments/assets/01fb8448-c1e7-4885-913c-7f2f61b1b80a">
<br>
The Skywater PDK defines 6 routing layers:
1. The lowest layer i.e. is the Local Interconnect Layer, this is a Titanium Nitride layer
2. The other layers are alluminum layers.

<br>
<img width="364" alt="image" src="https://github.com/user-attachments/assets/8c52efbc-fca1-444a-b219-38e63165c891">
<br>

Sign Off: <br>
<img width="220" alt="image" src="https://github.com/user-attachments/assets/9d0df3ca-b6e3-4e81-994b-7ea6c1f60964">
<br>

#### OpenLANE and Strive Chipsets
OpenLANE:<br>
<img width="359" alt="image" src="https://github.com/user-attachments/assets/e377ec6c-2e12-4eba-9f7e-12e08ea0732c">
<br>

striVe SoC Family:<br>
<img width="332" alt="image" src="https://github.com/user-attachments/assets/74412e42-77dd-42e0-8119-3994e345051b">
<br>

### Get familiar with open-source EDA tools.
<br><br>

PICORV32A PREP DONE
![image](https://github.com/SubhroRoy/NASSCOM--VSD-SOC-design/assets/169291565/05c30919-36f8-4d64-a5e2-2b652adeb588)
