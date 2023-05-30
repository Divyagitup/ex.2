### Ex. No. : 2 
### Date: 31.3.23 
# Implementation of Combinational logic circuit using Verilog HDL
## Aim:
To implement the following Boolean functions using Verilog HDL and to verify the truth table.
1. F1= A’B’C’D’+AC’D’+B’CD’+A’BCD+BC’D
2. F2=xy’z+x’y’z+w’xy+wx’y+wxy

## Components Required:
1.	Laptop with Quartus software and modelsim software.

## Theory:
Combinational Logic Circuits are memoryless digital logic circuits whose output at any instant in time depends only on the combination of its inputs.
The outputs of Combinational Logic Circuits are only determined by the logical function of their current input state, logic “0” or logic “1”, at any given instant in time.

![image](https://github.com/rvinifa/ex.2/assets/133735746/949815d3-0912-49c7-81c0-eea1c148d48e)

The result is that combinational logic circuits have no feedback, and any changes to the signals being applied to their inputs will immediately have an effect at the output. In other words, in a Combinational Logic Circuit, the output is dependant at all times on the combination of its inputs. Thus, a combinational circuit is memoryless.

## Procedure:
1.	Type the program in Quartus software.
2.	Compile and run the program.
3.	Generate the RTL schematic and save the logic diagram.
4.	Create nodes for inputs and outputs to generate the timing diagram.
5.	For different input combinations, generate the timing diagram.

## Simplification:
![WhatsApp Image 2023-05-30 at 8 30 02 AM](https://github.com/Divyagitup/ex.2/assets/134514564/9f19ba79-8be4-48f8-9409-d4382831f0b0)
![WhatsApp Image 2023-05-30 at 8 31 04 AM](https://github.com/Divyagitup/ex.2/assets/134514564/89c21594-96dd-40a5-95c7-2f9929b73c70)


## Truth Table:

![WhatsApp Image 2023-05-30 at 8 30 42 AM](https://github.com/Divyagitup/ex.2/assets/134514564/a1269c0c-f5ee-464f-84da-fb0a353584cd)
![WhatsApp Image 2023-05-30 at 8 31 04 AM (1)](https://github.com/Divyagitup/ex.2/assets/134514564/e71bb4c1-5fd2-403c-a944-576dd156865a)

## Program:
module exp2(a,b,c,d,f1,f2);
input a,b,c,d;
output f1,f2;
wire bdash,ddash,p,adash,q,cdash,r,u,v,w;
not(bdash,b);
not(ddash,d);
and(p,bdash,ddash);
not(adash,a);
and(q,adash,b,d);
not(cdash,c);
and(r,a,b,cdash);
or(f1,p,q,r);
and(u,cdash,d);
and(v,a,c);
and(w,b,c);
or(f2,u,v,w);
endmodule 

## RTL Schematic:

<img width="898" alt="exp2 dia" src="https://github.com/Divyagitup/ex.2/assets/134514564/8a24f7a2-9910-486f-a541-7dbe8aac8e10">



## Timing Diagram:
<img width="952" alt="exp 2" src="https://github.com/Divyagitup/ex.2/assets/134514564/44aaf4b1-7568-409c-afe2-3f5a8c2de6f5">




## Result:

Thus the given Boolean functions are implemented in Verilog HDL and the truth table are verified.



