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
**Study and review of various components in  RISC V based picoSoC**

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


### Lab:

>This specifies the synthesis command which uses the yosys to open the yosys terminal and how it gets opened and how it displays after the command was typed in terminal.it shows as **>yosys**

![](/IMAGES/DAY1/DAY-1%20LAB/mcq3/yosys.jpeg)

>This specifies the command **which sta** when typed in terminal it shows the location of sta ie.,where it is present that is in the usr folder to bin sub folder and there sta is present

![](/IMAGES/DAY1/DAY-1%20LAB/mcq4/sta%20command%20loc.jpeg)

>This command **git clone** mainly used for cloning the vsd flow which is taken from [kunal ghosh git hub](https://github.com/kunalg123/vsdflow) and from there the tools were imported

![](/IMAGES/DAY1/DAY-1%20LAB/mcq5/git%20clone.jpeg)

>This command **./vsdflow spi_slave_design_details.csv** is to initialize the design and the ls-ltr outdir_spi_slave |wc will specify the number of files

![](/IMAGES/DAY1/DAY-1%20LAB/mcq6/command.jpeg)

>There is a change in the directory and it is changed to **outdir_spi_slave** and qflow command is typed in ordere to display the spi_slave layout view

![](/IMAGES/DAY1/DAY-1%20LAB/mcq7/command.jpeg)

>This is the layou view of the spi_slave

![](/IMAGES/DAY1/DAY-1%20LAB/mcq7/layout.jpeg)

>This is the tkcon window in which the commands were typed in which **box** is typed in order to view the dimensions of the layout.Here the area is specified

![](/IMAGES/DAY1/DAY-1%20LAB/mcq7/tkcon.jpeg)

>These below figures specifies the **percentage ratio of flipflop to total logic**.For that to be known we should go to terminal and change the directory to **vsdflow**.make a directory **my_picorv32**.make three directories ie., source,synthesis,layout.In which the actual verilog source file **picorv32.v** is copied into source folder.Qflow is opened on the gui platform and the synthesis is done and report of the synthesis is taken.Number of cells = 13197 and Number of flops = 1613,Then the Ratio of flops to total logic  = 1317/1613 = 12.22%.
    

![](/IMAGES/DAY1/DAY-1%20LAB/mcq8/command.jpeg)

![](/IMAGES/DAY1/DAY-1%20LAB/mcq8/percentage%20ratio%20flipflopby%20tot.jpeg.jpeg)

![](/IMAGES/DAY1/DAY-1%20LAB/mcq8/qflow%20manager.jpeg)

![](/IMAGES/DAY1/DAY-1%20LAB/mcq8/qflow%20synthesis%20preparation.jpeg)

![](/IMAGES/DAY1/DAY-1%20LAB/mcq8/qflowtextreport.jpeg)


### DAY_2

**Chip planning strategies and introduction to foundry library cells**

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

>First we have to change the directory to vsdflow and then change the directory to pul_picorv32(which is our created directory it can be of any name).Then we should type the **qflow display picorv32** so that two windows will popup that is **layout** and **tkcon**.In tkcon we should type **box** so that length and width of the layout is obtained and from that we can calculate the area.

![](/IMAGES/DAY2/DAY-2%20LAB/MCQ5/layout%20command.jpeg)
![](/IMAGES/DAY2/DAY-2%20LAB/MCQ5/layoutarea.jpeg)
![](/IMAGES/DAY2/DAY-2%20LAB/MCQ5/layoutwindow.jpeg)

>The below figures are the **pinplacement** procedure that we follow.As the qflow is opened we will synthesis the design and in the placement settings we should click on the **arrange pins** option and there **reset,clk** pins must be grouped by newgroup by naming it.After that the iterations of standard cell and pins are taken place. 

![](IMAGES/DAY2/DAY-2%20LAB/PLACEMENT/ARRANGE%20PIN.jpeg)
![](/IMAGES/DAY2/DAY-2%20LAB/PLACEMENT/PLACEMENT%20SETTINGS.jpeg)

>These are the different iterations that are happened in the placement stage based on some algorithms and nearest pin specified in the option.


![](/IMAGES/DAY2/DAY-2%20LAB/PLACEMENT/PLACEMENTITERATION1.jpeg)
![](/IMAGES/DAY2/DAY-2%20LAB/PLACEMENT/PLCMNTITR3.jpeg)
![](/IMAGES/DAY2/DAY-2%20LAB/PLACEMENT/PLCMNTITR6.jpeg)

### DAY_3

**Design and characterize one library cell using Magic layout tool and ngspice**

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

>Here in this command the [ngspice_labs](https://github.com/kunalg123/ngspice_labs) are cloned inorder to use the spice labs.After cloning the directory is changed to ngspice_labs.Then inv.spice file is opened using **cat** command in order to view **width of pmos,nmos and wp/wn ratio** 

![](/IMAGES/DAY3/DAY-3%20LAB/d3sk1-mcq5.jpeg)

>This imaage specifies the ngspice **dc simulation** of the inv.spice file.To run the simulation we use **ngspice** tool.For that we use the command **ngspice inv.spice**,Then after run,setting plot to dc.A graph will appear where we can see the transfer characterstics of dc simulate

![](/IMAGES/DAY3/DAY-3%20LAB/d3sk1-mcq8.jpeg)

>By using the **leafpad** command we changed the width of pmos to 0.75u.Then performed the dc simulation in the spice labs.plotted the transfer charcterstics of the circuit.There is change in the switching threshold that can be observed in the graph.By clicking on the blue intersection line a change of x0 will be appeared compared to when width of pmos is 0.5u. 


![](/IMAGES/DAY3/DAY-3%20LAB/d3sk1-mcq5contd.jpeg)
![](/IMAGES/DAY3/DAY-3%20LAB/d3sk1-mcq10contd.jpeg)
![](/IMAGES/DAY3/DAY-3%20LAB/d3sk1-mcq10.jpeg)

>Here to calculate the **risedelay** we should take the transfer charcterstics of the inverter with pulse input which has a timeperiod.Firstly the ngspice tool is opened with **inv_tran.spice** file then the simulation is runned.setting the plot to **transient analysis** and plot the transfer characterstics a waveform is appeared.Rise delay is calculated by taking the 20% and 80% of rising wavefrom and calculating there difference. 

![](/IMAGES/DAY3/DAY-3%20LAB/d3sk1-mcq11.png)

>pre layout file is to be simulated in the ngspice and see its transient analysis.use the command  **ngspice fn_prelayout.spice**.run the simulation set the plot to transient analysis and plot the output graph at 1.25 as refrence we should calculate the value of x0 intersection of the rising waveform. 

![](/IMAGES/DAY3/DAY-3%20LAB/d3sk2-mcq1.jpeg)

>Similary the same file fn_prelayout is taken and run the tranisent analysis by plotting the output at the refrence 1.25 now we are calculating the falling waveform.Finding the value at where the intersection of refrence 1.25 cuts the point.

![](/IMAGES/DAY3/DAY-3%20LAB/d3sk2-mcq2.jpeg)

>Here the **magic** tool is used for layout drawing.The command **magic -T min 2 tech** is used to open the layout window where we can draw the layout.After typing in the terminal two windows will open viz **tkcon** and **layout1**.open tkcon window and source the **draw_fn.tcl** then the layout will appear select the layout by right click on bottom and left click on top and press **shift+i**.by typing box we can find the area by selecting the layout.in the layout y nsubstratecontact and polysilicon strips are found

![](/IMAGES/DAY3/DAY-3%20LAB/d3sk3-mcq3contd.jpeg)
![](/IMAGES/DAY3/DAY-3%20LAB/d3sk3-mcq3.jpeg)




>After sourcing the draw_fn.tcl.we will extract all files and also spice files by the commands **extract all and ext2spice**.From there we can obtain the **fn_postlayout.spice**,then this file is edited as it doent consists of vdd and gnd information.For the stimulus to obtain those were copied from the **fn_prelayout** and added to the fn_postlayout.Then the simulation is done and output charcterstics are plotted for transient analysis of te postlayout spice file.From there the rising and falling waveform are obatined.

![](/IMAGES/DAY3/DAY-3%20LAB/d3sk3-mcq4.jpeg)
![](/IMAGES/DAY3/DAY-3%20LAB/d3sk3-mcq5.jpeg)
![](/IMAGES/DAY3/DAY-3%20LAB/d3sk3-mcq5contd.jpeg)
![](/IMAGES/DAY3/DAY-3%20LAB/d3sk3-mcq5contd2.jpeg)
![](/IMAGES/DAY3/DAY-3%20LAB/d3sk3-mcq5contd3.jpeg)

### DAY_4

**Pre-layout timing analysis and importance of good clock tree**

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
>cd 
git clone https://github.com/kunalg123/ngspice_labs
cd ngspice_labs
cat inv_tran.spice
what is input rise slew and fall slew?

![](/IMAGES/DAY4/DAY-4%20LAB/d4sk1-mcq6.JPG)

>d4sk1-mcq7
2.ngspice inv_tran.spice
what is output load and rise delay?

![](/IMAGES/DAY4/DAY-4%20LAB/d4sk1-mcq7.JPG)
![](/IMAGES/DAY4/DAY-4%20LAB/d4sk1-mcq7contd.JPG)

>d4sk1-mcq8
1.output load to 20fF in inv_tran.spice.what is rise delay?

![](/IMAGES/DAY4/DAY-4%20LAB/d4sk1-mcq8.JPG)
![](/IMAGES/DAY4/DAY-4%20LAB/d4sk1-mcq8contd.JPG)

>d4sk2-mcq6
/usr/local/share/qflow/tech/osu018/osu018_stdcells.lib
what is value of slew_upper_hreshold_pct_fall?

>d4sk2-mcq7
what is output_threshold_pct_rise?

![](/IMAGES/DAY4/DAY-4%20LAB/d4sk2-mcq6.JPG)

>d4sk2-mcq8
what are the 2 variables of delay template 5x5?

![](/IMAGES/DAY4/DAY-4%20LAB/d4sk2-mcq8.JPG)

>d4sk2-mcq9
line num 2943 for which cell?invx1

![](/IMAGES/DAY4/DAY-4%20LAB/d4sk2-mcq9.JPG)

>d4sk2-mcq10
line number 2983?

![](/IMAGES/DAY4/DAY-4%20LAB/d4sk2-mcq10.JPG)

>d4sk2-mcq11
cd vsdflow/pul_picorv32
leafpad picorv32.sdc
create_clock -name clk -period 2.5 -waveform {0 1.25} [gets_ports clk]
leafpad prelayout_sta.conf
read_liberty /usr/local/share/qflow/tech/osu018/osu018_stdcells.lib
read_verilog synthesis/picorv32.rtlnopwr.v
link_design picorv32
read_sdc picorv32.sdc
report_checks
sta prelayout_sta.conf
slack value?


![](/IMAGES/DAY4/DAY-4%20LAB/d4sk2-mcq11conf.JPG)
![](/IMAGES/DAY4/DAY-4%20LAB/d4sk2-mcq11sdc.JPG)
![](/IMAGES/DAY4/DAY-4%20LAB/d4sk2-mcq11.JPG)

>d4sk2-mcq12
repeat all the steps
%
report_checks -digits 4
dat?



>d4sk2-mcq13
drt?

![](/IMAGES/DAY4/DAY-4%20LAB/d4sk2-mcq121.JPG)
![](/IMAGES/DAY4/DAY-4%20LAB/d4sk2-mcq12.JPG)


>d4sk4-mcq2
%
set_propogated_clock [all_clocks]
report_checks
slack after clock propogation?


![](/IMAGES/DAY4/DAY-4%20LAB/d4sk4-mcq2.JPG)

![](/IMAGES/DAY4/DAY-4%20LAB/d4sk4-mcq5.JPG)


### DAY_5

**Final steps for RTL2GDS**

### Theory:

 The day five responsibilities are to learn about

<ol>
<li>Introduction to Maze routing-Lees's ALgorithm</li>
<li>Lee's Algorithm conclusion</li>
<li>Design rule check</li>
<li>Introduction to IEEE 1481-1999 SPEF fomat</li>
<li>SPEF representation of a NET</li>
<li>Distributed resistance and capacitance representation in SPEF</li>
<li>SPEF header description</li>
<li>Few tips on pin placement and floorplanning chip</li>
<li>Placement and pre layout STA</li>
<li>Routing and post-route STA</li>
</ol>

### Lab:


![](/IMAGES/DAY5/DAY-5%20LAB/d5sk2-mcq1contd.JPG)
![](/IMAGES/DAY5/DAY-5%20LAB/d5sk2-mcq1.JPG)

![](/IMAGES/DAY5/DAY-5%20LAB/d5sk2-mcq2.JPG)
