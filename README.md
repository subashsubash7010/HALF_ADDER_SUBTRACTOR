# HALF_ADDER_SUBTRACTOR

Implementation-of-Half-Adder-and-Half Subtractor-circuit

**AIM:**

To design a half adder and half subtractor circuit and verify its truth table in Quartus using Verilog programming.

**Equipments Required:**

Hardware – PCs, Cyclone II , USB flasher 

Software – Quartus prime Theory Adders are digital circuits that carry out the addition of numbers.

**Half Adder**

Half adder is a combinational circuit that performs simple addition of two binary numbers. The input variables designate the augend and addend bits; the output variables produce the sum and carry. It is necessary to specify two output variables because the result may consist of two binary digits.

Sum = A’B+AB’ =A ⊕ B Carry = AB

![image](https://github.com/naavaneetha/HALF_ADDER_SUBTRACTOR/assets/154305477/bd4a0b2c-cdbc-4184-ab08-81578f121e1f)

Figure -01 HALF ADDER

**Half Subtractor**

The half-subtractor is a combinational circuit which is used to perform subtraction of two bits. It has two inputs, X (minuend) and Y (subtrahend) and two outputs D (difference) and B (borrow). To perform x - y, we have to check the relative magnitudes of x and y. If x ;;, y, we have three possibilities: 0 - 0 = 0, 1 - 0 = 1, and 1 - I = 0. The result is called the difference bit. If x < y, we have 0 - I, and it is necessary to borrow a 1 from the next higher stage. The I borrowed from the next higher stage adds 2 to the minuend bit, just as in the decimal system a borrow adds 10 to a minuend digit. With the minuend equal to 2, the difference becomes 2 - I = 1. The half-subtractor needs two outputs. One output generates the difference and will be designated by the symbol D. The second output, designated B for borrow, generates the binary signal that informs the next stage that a I has been borrowed. 

Diff = A’B+AB’ =A ⊕ B
Borrow = A’B

![image](https://github.com/naavaneetha/HALF_ADDER_SUBTRACTOR/assets/154305477/d76b099c-513f-4e7c-843a-e2fd028a531a)

Figure -02 HALF Subtractor

**Truthtable**

![Screenshot 2024-09-26 210602](https://github.com/user-attachments/assets/547148e0-b5e7-4266-9e73-c2582afe498d)


**Procedure**

1.	Type the program in Quartus software.

2.	Compile and run the program.

3.	Generate the RTL schematic and save the logic diagram.

4.	Create nodes for inputs and outputs to generate the timing diagram.

5.	For different input combinations generate the timing diagram.


**Program:**

Program to design a half adder and full adder circuit and verify its truth table in quartus using Verilog programming.

```
Developed by: SUBASH M
RegisterNumber: 212224220109
```

HALF ADDER
```
module ha(a,b,sum,carry);
input a,b;
output sum,carry;
assign sum=(a^b);
assign carry=(a&b);
endmodule
```
HALF SUBTRACTOR
```
module hs(x,y,diff,borr);
input x,y;
output diff,borr;
assign diff = (x^y);
assign borr = (~x&y);
endmodule
```

**RTL Schematic**

HALF ADDER
![Screenshot 2024-09-20 092757](https://github.com/user-attachments/assets/90b78822-3750-4053-83d2-41e421379728)

HALF SUBTRACTOR
![Screenshot 2024-09-20 093951](https://github.com/user-attachments/assets/ca19a462-d33f-4a8d-b0cc-8a2c55f9dd0e)


**Output/TIMING Waveform**

HALF ADDER
![Screenshot 2024-09-20 093103](https://github.com/user-attachments/assets/78eda0e4-1614-4b03-ac82-914b4418eb39)

HALF SUBTRACTOR
![Screenshot 2024-09-20 094658](https://github.com/user-attachments/assets/a7db4467-8869-496a-a0ba-0020b138e5ff)


**Result:**

Thus the design of a half adder and half subtractor circuit and its truth table in Quartus using Verilog programming is successfully completed.
