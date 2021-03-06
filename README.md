#  VSD_PD_Using_OSET

The purpose of this repository is to provide a complete idea about the workshop on VLSI SoC/Physical design using open-source EDA Tools.The main target audience of the
workshop is 
1. one who wants to learn SoC planning 
2. one who wants to learn chip design from specifications to Layout
3. one who is curious to know, what happens before Synthesis, Physical design and STA.

The open source tools that are involved in this workshop are as follows
1. **Yosys** – for Synthesis
2. **Graywolf** – for Placement
3. **Qrouter** – for Routing
4. **Netgen** – for LVS
5. **Magic** – for Layout and Floorplanning
6. **Qflow** – RTL2GDS integration
7. **OpenSTA & Opentimer** -Pre-layout and Post-layout Static timing analysis
  
>The overall workshop is based on the RISC V processor to know about more [About RISC](https://riscv.org/about/) and its specifications [SPEC](https://riscv.org/technical/specifications/).

The refrence design used here is **RISC-V based Raven SoC (First silicon proven open source SoC)**

####  The total workshop is around 5 days.
The responsibilities of each individual day is listed below


## DAY1

### Theory:
 The day one responsibilities are to learn about
 <ol>
 <li> Introduction to QFN-48 package,chip,pads,die,core,IPs </li>
 <li> Introduction to RISC V </li>
 <li> From software application to hardware </li>
 <li> Pre requesities and RISC V,PICORV32 AND picosoc view </li>
 <li> Raven Soc and full chip review </li>
 <li> Introduction to IC design components and open source EDA tools </li>
 <li> Steps to start synthesizing picorv32, report ratio </li>
 <li> Test open source EDA tools using sample design and VSD flow utility </li>
 <li> Steps to perform labs on platform </li>
 </ol>




![](/IMAGES/DAY1/DAY-1%20THEORY/QFN48%20package/processor_soc%20block.jpeg)



![](/IMAGES/DAY1/DAY-1%20THEORY/QFN48%20package/QFN48blocksdescr.jpeg)


### Lab:

![](/IMAGES/DAY1/DAY-1%20LAB/mcq3/yosys.jpeg)

![](/IMAGES/DAY1/DAY-1%20LAB/mcq4/sta%20command%20loc.jpeg)

![](/IMAGES/DAY1/DAY-1%20LAB/mcq5/git%20clone.jpeg)

![](/IMAGES/DAY1/DAY-1%20LAB/mcq6/command.jpeg)

![](/IMAGES/DAY1/DAY-1%20LAB/mcq7/command.jpeg)

![](/IMAGES/DAY1/DAY-1%20LAB/mcq7/layout.jpeg)

![](/IMAGES/DAY1/DAY-1%20LAB/mcq7/tkcon.jpeg)

![](/IMAGES/DAY1/DAY-1%20LAB/mcq8/command.jpeg)

![](/IMAGES/DAY1/DAY-1%20LAB/mcq8/percentage%20ratio%20flipflopby%20tot.jpeg.jpeg)

![](/IMAGES/DAY1/DAY-1%20LAB/mcq8/qflow%20manager.jpeg)

![](/IMAGES/DAY1/DAY-1%20LAB/mcq8/qflow%20synthesis%20preparation.jpeg)

![](/IMAGES/DAY1/DAY-1%20LAB/mcq8/qflowtextreport.jpeg)


### DAY_2

### Theory:

 The day two responsibilities are to learn about

<ol>
   <li>  Utilization factor and Aspect Ratio </li>
   <li>  Concept of preplaced cells </li>
   <li>  De coupling capacitors</li>
   <li>  Power planning</li>
   <li>  Pin placement and logical cell placement blockage</li>
   <li>  Pin arrangement UI and automatic grouping of vectors</li>
   <li>  Tips on pin placement and floorplanning chip</li>
   <li>  Floorplanning labs</li>
   <li>  Netlist binding and initial place design</li>
   <li>  Optimize placement using estimated wire length and capacitance</li>
   <li>  Final placement optimization</li>
   <li>  Need for libraries and characterization</li>
   <li>  Inputs for cell dessign flow</li>
   <li>  Circuit design step</li>
   <li>  Layout design step</li>
   <li>  Typical characterization flow</li>
   <li>  Timing threshold definitions</li>
   <li>  Propogation delay and transition time</li>
  </ol>
  
### Lab:



### DAY_3

### Theory:

 The day three responsibilities are to learn about
 
 <ol>
 <li>  SPICE deck creation for CMOS inverter</li>
 <li>  SPICE simulation lab for CMOS inverter</li>
 <li>  Switching Threshold Vm</li>
 <li>  Static and dynamic simulation of CMOS inverter</li>
 <li>  Prelayout simulation of a test circuit</li>
 <li>  Layout using only stick diagram</li>
 <li>  Eulers path for Fn Input gate reordering</li>
 <li>  Improved stick diagram for new gate input ordering</li>
 <li>  Abstract layout from stick diagram</li>
 <li>  Device actual dimension for Fn</li>
 <li>  Script to create layout in Magic</li>
 <li>  Final layout and input/output labelling</li>
 <li>  Post layout ngspice simulation</li>
 <li>  Create active regions</li>
 <li>  Formation of N well and P well</li>
 <li>  Formation of gate terminal</li>
 <li>  Lightly doped drain (LDD) formation</li>
 <li>  Source drain formation</li>
 <li>  Local interconnect formation</li>
 <li>  Higher level metal formation</li>
 </ol>


### Lab:



### DAY_4

### Theory:

 The day four responsibilities are to learn about
 
 <ol>
 <li>  Introduction to delay tables</li>
 <li>  Delay table usage Part 1</li>
 <li>  Delay table usage Part 2</li>
 <li>  Setup timing analysis and introduction to flipflop setup time</li>
 <li>  Introduction to clock jitter and uncertainity</li>
 <li>  Clock tree routing and buffering using H tree algorithm</li>
 <li>  Crosstalk and clock net shielding</li>
 <li>  Setup timing analysis using real clocks</li>
 <li>  Hold timing analysis using real clocks</li>
 </ol>
 

### Lab:



### DAY_5

### Theory:

 The day five responsibilities are to learn about


### Lab:
