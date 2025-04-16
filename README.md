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

/* 
Program to implement the given logic function and to verify its operations in quartus using Verilog programming. 

Developed by:VARUN JC  

RegisterNumber:212224240179
```
module varun(a,b,c,d,w,x,y,z,f1,f2);
  input a,b,c,d,w,x,y,z;
  output f1,f2;
  wire x1,x2,x3,x4,x5,y1,y2,y3,y4,y5;
  assign x1=((~a)&(~b)&(~c)&(~d));
  assign x2=(a&(~c)&(~d));
  assign x3=((~b)&(c)&(~d));
  assign x4=((~a)&(b)&(c)&(d));
  assign x5=(b&(~c)&(d));
  assign f1=x1|x2|x3|x4|x5;
  
  assign y1=(x&(~y)&(z));
  assign y2=((~x)&(~y)&z);
  assign y3=((~w)&x&y);
  assign y4=(w&(~x)&(y));
  assign y5=(w&x&y);
  assign f2=y1|y2|y3|y4|y5;
  endmodule
```
*/


**TRUTH TABLE**
![50d2a8e8-b177-47f9-9501-56091117da8c](https://github.com/user-attachments/assets/1af1a780-2863-41a7-8fba-1fd553c7618c)
![bf95fd33-aeea-49ad-aad3-bf246bc319b1](https://github.com/user-attachments/assets/66f485b5-8f60-4597-8b16-fdf98069a962)

**RTL**

![Screenshot 2025-04-16 084341](https://github.com/user-attachments/assets/fe7fc7c0-8d0a-428a-b5c3-a2a6dc6310aa)

**WAVEFORM**

![06a10208-67e3-4c62-b5f9-2553deba1aac](https://github.com/user-attachments/assets/e3f247ea-7df4-4bdf-a025-a95f241e72fc)

**Result:**

Thus the given logic functions are implemented using and their operations are verified using Verilog programming.

