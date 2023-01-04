# Exp-02-Implementation-of-Half-Adder-and-Full-Adder-circuit

# Implementation-of-Half-Adder-and-Full-Adder-circuit
### AIM:
To design a half adder and full adder circuit and verify its truth table in Quartus using Verilog programming.

### Equipments Required:
Hardware – PCs, Cyclone II , USB flasher
Software – Quartus prime
Theory
Adders are digital circuits that carry out addition of numbers.

### Half Adder
Half adder is a combinational circuit that performs simple addition of two binary numbers. The input variables designate the augend and addend bits; the output variables produce the sum and carry. It is necessary to specify two output variables because the result may consist of two binary digits.

Sum = A’B+AB’ =A ⊕ B Carry = AB

### Full Adder
Full adder is a digital circuit used to calculate the sum of three binary bits. It consists of three inputs and two outputs. Two of the input variables, denoted by A and B, represent the two significant bits to be added. The third input, Cin, represents the carry from the previous lower significant position. Two outputs are necessary because the arithmetic sum of three binary digits ranges in value from 0 to 3, and binary 2 or 3 needs two digits. The two outputs are sum and carry.

Sum =A’B’Cin + A’BCin’ + ABCin + AB’Cin’ = A ⊕ B ⊕ Cin Carry = AB + ACin + BCin

 ![image](https://user-images.githubusercontent.com/36288975/163552156-a13e5a56-c638-4110-97d9-8896907c8d25.png)

#### Figure -01 HALF ADDER 


![image](https://user-images.githubusercontent.com/36288975/163552057-b3547877-6d07-45b4-b7e0-bcfebfad9e1d.png)

#### Figure -02 FULL ADDER 

### Procedure

Connect the supply (+5V) to the circuit
Switch ON the main switch
If the output is 1, then the led glows.

### Program:

```
Program to design a half adder and full adder circuit and verify its truth table in quartus using Verilog programming.

Developed by: Shriram S
RegisterNumber:22008494  

Half Adder

module halfadder(A,B,Sum,Carry);
input A,B;
output Sum,Carry;
xor(Sum,A,B);
and(Carry,A,B);
endmodule

Full Adder

module fulladder(A,B,C,Sum,Carry);
input A,B,C;
output Sum,Carry;
assign Sum = ((A^B)^C);
assign Carry = ((A&B)|(B&C)|(C&A));
endmodule

```

### Output:
### RTL

RTL Realization for Half Adder

![halfadderrtl](https://user-images.githubusercontent.com/117991122/210625521-9a98f79d-bb30-41a1-8653-079f9b683941.png)

RTL Realization for Full Adder

![fulladderrtl](https://user-images.githubusercontent.com/117991122/210628659-d57a3d8a-a38f-4d3e-be9f-16c17943e678.png)


### TIMING DIAGRAM

Timing Diagram for Half Adder

![halfaddertimimgdiagram](https://user-images.githubusercontent.com/117991122/210625418-202ee9bf-82b6-4bff-b44c-7d3472823b77.jpg)

Timing Diagram for Full Adder

![fulladdertimimgdiagram](https://user-images.githubusercontent.com/117991122/210628718-a3fadcc6-7e9d-4760-94b0-86e446ad00df.png)


### TRUTH TABLE 

Truth Table for Half Adder

![truthtableha](https://user-images.githubusercontent.com/117991122/210627417-ddcddf40-ed45-43e5-93e6-c4a65f56e2f2.jpg)

Truth Table for Full Adder

![fulladdertruthtable](https://user-images.githubusercontent.com/117991122/210629188-b8fc03c6-57dd-4e76-8db7-109dc7f5980c.jpg)


### Result:

Thus the Half adder and Full Adder Circuits was successfully implemented.
