## AIM:

To implement and design synthesis and simulation for uart using cadence - genus and innovus.

## TOOLS REQUIRED:

Functional Simulation: Incisive Simulator (ncvlog, ncelab, ncsim) Synthesis: Genus Floorplanning: Innovus

## PROCEDURE:

Step 1: Synthesis requires the following files as follows: ◦ Liberty Files (.lib) ◦ VerilogFiles (.v )

### Add Verilog  (.v ) file

### Add Testbench file

### Add run.tcl file

SDC (Synopsis Design Constraint) File (.sdc)

In your terminal type “gedit input_constraints.sdc” to create an SDC File if you do not have one.

The SDC File must contain the following commands; 

### Add SDC file

i→ Creates a Clock named “clk” with Time Period 2ns and On Time from t=0 to t=1. 

ii, iii → Sets Clock Rise and Fall time to 100ps. 

iv → Sets Clock Uncertainty to 10ps. 

v, vi → Sets the maximum limit for I/O port delay to 1ps.

•	The Liberty files are present in the library path,

•	The Available technology nodes are 180nm ,90nm and 45nm.

•	In the terminal, initialise the tools with the following commands if a new terminal is being used. ◦ csh ◦ source /cadence/install/cshrc

•	The tool used for Synthesis is “Genus”. Hence, type “genus -gui” to open the tool.

•	Genus Script file with .tcl file Extension commands are executed one by one to synthesize the netlist. Step 2 : Creating an SDC File Step 3 : Performing Synthesis

### Fig 1: RTL Simulation:
<img width="1606" height="825" alt="Screenshot 2025-11-24 100349" src="https://github.com/user-attachments/assets/d5f4a081-04ac-41f3-b0a6-8327a0de9c4c" />

### Fig 2: Synthesis RTL Schematic:
<img width="1600" height="882" alt="image" src="https://github.com/user-attachments/assets/dfefa39f-cc5f-4e1c-8c9e-200290f55202" />

### Fig 3: Area Report:
<img width="1604" height="825" alt="Screenshot 2025-11-24 100154" src="https://github.com/user-attachments/assets/0ebaffe4-be97-41b2-aa19-35208620aa8b" />

### Fig 4: Power Report:
<img width="1606" height="825" alt="Screenshot 2025-11-24 100349" src="https://github.com/user-attachments/assets/0db36178-1d36-4b5b-b271-8fa36d3b28ed" />

### Fig 5: Timing Report:
<img width="1560" height="786" alt="image" src="https://github.com/user-attachments/assets/0bb9f62a-65d4-4331-b87f-f528738e648c" />

### Fig 6: UART APR:

## RESULT:

The functionality of the uart was successfully verified using a testbench and simulated with the nclaunch tool and genus and for innovus creating the physical design.
