## NAME : ALIYA SHEEMA N
## REGISTER NO : 23005529
# Experiment--02-Implementation-of-combinational-logic
Implementation of combinational logic gates
 
## AIM:
To implement the given logic function verify its operation in Quartus using Verilog programming.
F1= A’B’C’D’+AC’D’+B’CD’+A’BCD+BC’D

 

## Equipments Required:
Hardware – PCs, Cyclone II , USB flasher
Software – Quartus prime


## Theory
A Combinational circuit is a circuit in which the output depends on the present combination of inputs. Combinational circuits are made up of logic gates. The output of each logic gate is determined by its logic function. 
Combinational circuits can be made using various logic gates, such as AND gate, OR gates, and NOT gates.
 


## Procedure
1. Create a New Project:
   - Open Quartus and create a new project by selecting "File" > "New Project Wizard."
   - Follow the wizard's instructions to set up your project, including specifying the project name, location, and target device (FPGA).

2. Create a New Design File:
   - Once the project is created, right-click on the project name in the Project Navigator and select "Add New File."
   - Choose "Verilog HDL File" or "VHDL File," depending on your chosen hardware description language.

3. Write the Combinational Logic Code:
   - Open the newly created Verilog or VHDL file and write the code for your combinational logic.
     
4. Compile the Project:
   - To compile the project, click on "Processing" > "Start Compilation" in the menu.
   - Quartus will analyze your code, synthesize it into a netlist, and perform optimizations based on your target FPGA device.

5. Analyze and Fix Errors:
   - If there are any errors or warnings during the compilation process, Quartus will display them in the Messages window.
   - Review and fix any issues in your code if necessary.
   - View the RTL diagram.

6. Verification:
   - Click on "File" > "New" > "Verification/Debugging Files" > "University Program VWF".
   - Once Waveform is created Right Click on the Input/Output Panel > " Insert Node or Bus" > Click on Node Finder > Click On "List" > Select All.
   - Give the Input Combinations according to the Truth Table amd then simulate the Output Waveform.

     
## Program:

Program to implement the given logic function and to verify its operations in quartus using Verilog programming.

module combinationalcircuit(A,B,C,D,F1);

input A,B,C,D;

output F1;

wire Abar,Bbar,Cbar,Dbar,a1,a2,a3,a4,a5;

assign Abar=~A;

assign Bbar=~B;

assign Cbar=~C;

assign Dbar=~D;

assign a1=Abar&Bbar&Cbar&Dbar;

assign a2=A&Cbar&Dbar;

assign a3=Bbar&C&Dbar;

assign a4=Abar&B&C&D;

assign a5=B&Cbar&D;

assign F1=a1|a2|a3|a4|a5;

endmodule 


## RTL realization
![CC RTL](https://github.com/23005529/Experiment--02-Implementation-of-combinational-logic-/assets/139842207/659615d8-7cd4-4ce1-ac5a-c716cda26157)

## Truth table
![tt](https://github.com/23005529/Experiment--02-Implementation-of-combinational-logic-/assets/139842207/538a6bdb-f3c3-4510-a350-e6d6e8ecd895)

## Waveform
![CC WF](https://github.com/23005529/Experiment--02-Implementation-of-combinational-logic-/assets/139842207/e26c43b4-ba32-45b0-ab7b-047e2b7cedf2)

## Result:
Thus the given logic function are implemented using  and their operations are verified using Verilog programming.
