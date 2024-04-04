# BOOLEAN_FUNCTION_MINIMIZATION

**AIM:**

To implement the given logic function verify its operation in Quartus using Verilog programming.

F1= A’B’C’D’+AC’D’+B’CD’+A’BCD+BC’D 

F2=xy’z+x’y’z+w’xy+wx’y+wxy

**Equipment Required:**

Hardware – PCs, Cyclone II , USB flasher

**Software – Quartus prime**

**Theory**

**Logic Diagram**

**Procedure**

1.	Type the program in Quartus software.

2.	Compile and run the program.

3.	Generate the RTL schematic and save the logic diagram.

4.	Create nodes for inputs and outputs to generate the timing diagram.

5.	For different input combinations generate the timing diagram.


**Program:**

/* Program to implement the given logic function and to verify its operations in quartus using Verilog programming. 

Developed by: Saravanan C

RegisterNumber: 212222110041
*/

## Full Adder
```
module fulladder(a,b,cin,sum,carry);
input a,b,cin;
output sum,carry;
wire w1,w2,w3,w4;       
xor(w1,a,b);
xor(sum,w1,cin);        

and(w2,a,b);
and(w3,b,cin);
and(w4,cin,a);

or(carry,w2,w3,w4);
endmodule
```
## Full Subtractor
```
module fullsub(a,b,Bin,BO,DIFF);
input a,b,Bin;
output BO,DIFF;
assign DIFF = a ^ b ^ Bin;
  assign BO = (a & b) | ((a ^ b) & Bin);
endmodule
```


**RTL Schematic**
![Screenshot 2024-03-22 143255](https://github.com/Yogesh-Yogi-1/FULL_ADDER_SUBTRACTOR/assets/148514598/939151e8-c37b-49aa-8f44-513492ba509e)
![Screenshot 2024-03-22 143433](https://github.com/Yogesh-Yogi-1/FULL_ADDER_SUBTRACTOR/assets/148514598/aa118976-fe63-40e9-a31c-cec66367d805)
**Output Timing Waveform**
![Screenshot 2024-03-18 090939](https://github.com/Yogesh-Yogi-1/FULL_ADDER_SUBTRACTOR/assets/148514598/fe08e008-070e-4e8b-bee9-f26ade621c0e)
![Screenshot 2024-03-18 092119](https://github.com/Yogesh-Yogi-1/FULL_ADDER_SUBTRACTOR/assets/148514598/c37c43ae-514e-4fda-82d9-22ed613851e0)
**Result:**

Thus the Full Adder and Full Subtractor circuits are designed and the truth tables is verified using Quartus software.
