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
   <li>1.1.  Utilization factor and Aspect Ratio
   <li>1.2.  Concept of preplaced cells 
   <li>1.3.  De coupling capacitors
   1.4.  Power planning
   1.5.  Pin placement and logical cell placement blockage
   1.6.  Pin arrangement UI and automatic grouping of vectors
   1.7.  Tips on pin placement and floorplanning chip
   1.8.  Floorplanning labs
   2.1.  Netlist binding and initial place design
   2.2.  Optimize placement using estimated wire length and capacitance
   2.3.  Final placement optimization
   2.4.  Need for libraries and characterization
   3.1.  Inputs for cell dessign flow
   3.2.  Circuit design step
   3.3.  Layout design step
   3.4.  Typical characterization flow
   4.1.  Timing threshold definitions
   4.2.  Propogation delay and transition time
  </li>
   </ol>
### Lab:



### DAY_3

### Theory:

 The day three responsibilities are to learn about
 
 1.1.  SPICE deck creation for CMOS inverter
 1.2.  SPICE simulation lab for CMOS inverter
 1.3.  Switching Threshold Vm
 1.4.  Static and dynamic simulation of CMOS inverter
 2.1.  Prelayout simulation of a test circuit
 2.2.  Layout using only stick diagram
 2.3.  Eulers path for Fn Input gate reordering
 2.4.  Improved stick diagram for new gate input ordering
 2.5.  Abstract layout from stick diagram
 3.1.  Device actual dimension for Fn
 3.2.  Script to create layout in Magic
 3.3.  Final layout and input/output labelling
 3.4.  Post layout ngspice simulation
 4.1.  Create active regions
 4.2.  Formation of N well and P well
 4.3.  Formation of gate terminal
 4.4.  Lightly doped drain (LDD) formation
 4.5.  Source drain formation
 4.6.  Local interconnect formation
 4.7.  Higher level metal formation
 


### Lab:



### DAY_4

### Theory:

 The day four responsibilities are to learn about
 
 1.1.  Introduction to delay tables
 1.2.  Delay table usage Part 1
 1.3.  Delay table usage Part 2
 2.1.  Setup timing analysis and introduction to flipflop setup time
 2.2.  Introduction to clock jitter and uncertainity
 3.1.  Clock tree routing and buffering using H tree algorithm
 3.2.  Crosstalk and clock net shielding
 4.1.  Setup timing analysis using real clocks
 4.2.  Hold timing analysis using real clocks
 
 

### Lab:



### DAY_5

### Theory:

 The day five responsibilities are to learn about


### Lab:
