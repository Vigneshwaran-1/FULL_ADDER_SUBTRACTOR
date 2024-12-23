# FULL_ADDER_SUBTRACTOR

Implementation-of-Full-Adder-and-Full-subtractor-circuit

**AIM:**

To design a Full Adder and Full Subtractor circuit and verify its truth table in Quartus using Verilog programming.

**Equipments Required:**

Hardware – PCs, Cyclone II , USB flasher

Software – Quartus prime

**Full Adder and Full Subtractor**

**Full Adder**

Full adder is a digital circuit used to calculate the sum of three binary bits. It consists of three inputs and two outputs. Two of the input variables, denoted by A and B, represent the two significant bits to be added. The third input, Cin, represents the carry from the previous lower significant position. Two outputs are necessary because the arithmetic sum of three binary digits ranges in value from 0 to 3, and binary 2 or 3 needs two digits. The two outputs are sum and carry.

Sum =A’B’Cin + A’BCin’ + ABCin + AB’Cin’ = A ⊕ B ⊕ Cin 

Carry = AB + ACin + BCin

![image](https://github.com/naavaneetha/FULL_ADDER_SUBTRACTOR/assets/154305477/0f30ba51-5ffb-4198-845f-18e054f675e7)

**Figure -1 FULL ADDER**

**Full Subtractor**

A full subtractor is a combinational circuit that performs subtraction involving three bits, namely minuend, subtrahend, and borrow-in . It accepts three inputs: minuend, subtrahend and a borrow bit and it produces two outputs: difference and borrow.

![image](https://github.com/naavaneetha/FULL_ADDER_SUBTRACTOR/assets/154305477/02b24f51-ab51-4304-9ad6-7b81ffc1ead5)

Diff = A ⊕ B ⊕ Bin 

Borrow out = A'Bin + A'B + BBin

**Truthtable**

**Procedure**

Write the detailed procedure here

1.Sum Calculation:

First, calculate the XOR of inputs A and B.

Then, XOR the result with the carry-in (Cin).

Formula: Sum = A ⊕ B ⊕ Cin

2.Carry Calculation:

Compute two AND gates: one for A and B, and another for Cin and (A ⊕ B).

The final carry output is the OR of the two AND gates.

Formula: Cout = (A ⋅ B) + (Cin ⋅ (A ⊕ B))



Difference Calculation:

Calculate the XOR of A and B.

XOR the result with Bin to obtain the difference.

Formula: D = A ⊕ B ⊕ Bin

Borrow Calculation:

Compute the borrow from three cases:

When A is 0 and B is 1: ¬A ⋅ B

When A is 0 and Bin is 1: ¬A ⋅ Bin

When B is 1 and Bin is 1: B ⋅ Bin

The final borrow output is the OR of these three cases.

Formula: Bout = (¬A ⋅ B) + (¬A ⋅ Bin) + (B ⋅ Bin)


**Program:**

/* Program to design a half subtractor and full subtractor circuit and verify its truth table in quartus using Verilog programming. Developed by: RegisterNumber:

i)FULL ADDER

module fa(a,b,cin,sum,carry);

input a,b,cin;

output sum,carry;

assign sum=( (a ^ b)^c);

assign carry= ( (a & b)| ( cin &(a ^ b ));

endmodule

ii)FULL SUBTRACTOR

module fs(a,b,difference,borrow);

input a,b,bin;

output difference,borrow;

assign difference= ( (a ^ b)^bin);

assign borrow= ( ( ~a & b)| ( bin & (~(a ^ b )));

endmodule


*/

**RTL Schematic**
1)HALF ADDER



![ex-4 1](https://github.com/user-attachments/assets/e23cd13e-771c-4181-aa7a-ddedf5531390)




**Output Timing Waveform**

1)HALF ADDER

![ex-4 2](https://github.com/user-attachments/assets/8b05bc18-167a-42f8-863f-67ca4eb92a95)



![ex-4 3](https://github.com/user-attachments/assets/3d296601-2b09-4e12-bc9c-9126fe997251)






**Result:**

Thus the Full Adder and Full Subtractor circuits are designed and the truth tables is verified using Quartus software.



