# NASSCOM--VSD-SOC-design
# **DAY 1** <br> 
## **Introduction to open-source EDA, openLANE, skywater130 pdk and prerequisites.** <br>
* Introduction to Packages for design, open-source EDA, openLANE and skywater130 pdk.
  * Introduction to QFN-48 Package. <br>
  
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
<img width="379" alt="image" src="https://github.com/SubhroRoy/NASSCOM--VSD-SOC-design/assets/169291565/26ac838d-22e6-4e75-8ce2-442a31b58bef">
<br>
FIG 1.1.2: (i-top left)Chip structure in a QFN-48 package,(ii-top right)CHIP Inside: PADS, Core, Die, (iii-bottom left)RISC V SOC sample and (iv-bottom right) RISC V SOC core blocks 
</figcaption> <br><br>
If we take the chip in question and remove the cover. We will see the chip structure as seen above. It is a QFN-48 package structure i.e. Quad Flat No-Leads structure with a total of 48 pins. The chip sits at the middle of the package connected to the pins using wire bonds. <br><br>

**Components of the CHIP :** <br>
**CORE**: Where all the logic sits.<br>
**DIE**: Size of the chip.<br>
**PADS**: Used to send the signals inside the chip. <br>

A typical RISC-V SoC core consists of
**SRAM, ADC, DAC, PLL** are called foundry IPs.
SPI <BR>

* SOC design and openLANE.
* Get familiar to open source EDA tools.
<br><br>
  
PICORV32A PREP DONE
![image](https://github.com/SubhroRoy/NASSCOM--VSD-SOC-design/assets/169291565/05c30919-36f8-4d64-a5e2-2b652adeb588)
