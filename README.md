NAME: LOKESH M 

REGISTER NUMBER: 23001615
# Experiment--02-Implementation-of-combinational-logic
Implementation of combinational logic gates
 
## AIM:
To implement the given logic function verify its operation in Quartus using Verilog programming.
 F1= A’B’C’D’+AC’D’+B’CD’+A’BCD+BC’D
F2=xy’z+x’y’z+w’xy+wx’y+wxy
 
 
 
## Equipments Required:
## Hardware – PCs, Cyclone II , USB flasher Software- Quartus prime

## Theory:
A combinational circuit is a circuit in which the output depends on the present combination of inputs. Combinational circuits are made up of logic gates. The output of each logic gate is determined by its logic function. Combinational circuits can be made using various logic gates, such as AND gates, OR gates, and NOT gates.
 

## Procedure
Create a New Design File:

1. Create a New Project:

      • Open Quartus and create a new project by selecting "File" > "New Project Wizard."

      • Follow the wizard's instructions to set up your project, including specifying the project name, location, and target device (FPGAL

2. Create a New Design File:

      •  Once the project is created, right-click on the project name in the Project Navigator and select "Add New File

      •  Choose "Verilog HDL File" or "VHDL File, depending on your chosen hardware description language.

3. Write the Combinational Logic Coder:

      •  Open the newly created Verilog or VHDL file and write the code for your combinational logic.

4. Compile the Project:

      •  To compile the project, click on "Processing"> "Start Compilation" in the menu.

      •  Quartus will annlayse your code, systhesis it into a netlist, and perform optimizatioons based on your target FGPA device


5. Analyze and Fix Errors:

      • If there are any errors or warnings during the compilation process, Quartus will display them in the Messages window.

      • Review and fix any issues in your code if necessary.

      • View the RTL diagram

6. Verifications:

      • Click on "The "New"> "Verification/Debugging Files" > "University Program VWF".

      • Once Waveform is created flight Click on the Input/Output Panel > "Insert Node or Bus" > Click on Node Finder > Click On "List"> Select All

      • Give the Input Combinations according to the Truth Table and then simulate the Output waveform
Program:
## Program:
```
module exp2(A,B,C,D,F1);
input A,B,C,D;
output F1;
wire x1,x2,x3,x4,x5;
assign x1=(~A)&(~B)&(~C)&(~D);
assign x2=(A)&(~C)&(~D);
assign x3=(~B)&(C)&(~D);
assign x4=(~A)&(B)&(C)&(D);
assign x5=(B)&(~C)&(D);
assign F1=x1|x2|x3|x4|x5;
endmodule 
```
## RTL realization
![exp2RTL viewer](https://github.com/Lokesh23001615/Experiment--02-Implementation-of-combinational-logic-/assets/144979337/8cb19ac6-91a6-42f5-a7c9-6caf9c2570a6)


## TRUTH TABLE:
![exp2RTL viewer(1)](https://github.com/Lokesh23001615/Experiment--02-Implementation-of-combinational-logic-/assets/144979337/e5afdc23-b130-4657-a377-091029387584)

## TIMING DIAGRAM
![image](https://github.com/Lokesh23001615/Experiment--02-Implementation-of-combinational-logic-/assets/144979337/4e67b5f0-50a5-4cb1-8490-7269fceed3c7)

## Result:
Thus the given logic functions are implemented using  and their operations are verified using Verilog programming.
