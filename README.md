# FULL_ADDER_SUBTRACTOR

Implementation-of-Full-Adder-and-Full-subtractor-circuit

EXP-4

DATE-22-10-2024

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
FULL ADDER

![image](https://github.com/user-attachments/assets/d8a51f07-fee2-412c-8d5d-a4a6c20e68ff)

FULL SUBTRACTOR

![image](https://github.com/user-attachments/assets/78da0dae-4786-4b9b-846f-4609a9876872)

**Procedure**

Write the detailed procedure here
 **Full Adder:**

 1.Open Quartus II and create a new project.
 
 2.Use schematic design entry to draw the full adder circuit. 
 
 3.The circuit consists of XOR, AND, and OR gates. 
 
 4.Compile the design, verify its functionality through simulation. 
 
 5.Implement the design on the target device and program it.
 
 **Full Subtractor:** 

1.Follow the same steps as for the full adder. 

2.Draw the full subtractor circuit using schematic design. 

3.The circuit includes XOR, AND, OR gates to perform subtraction. 

4.Compile, simulate, implement, and program the design similarly to the full adder

**Program:**

/* Program to design a half subtractor and full subtractor circuit and verify its truth table in quartus using Verilog programming.

Developed by: JEEVIKA R

RegisterNumber:24900508

 FULL ADDER

 module fa(a, b, cin, sum, carry);
 
 input a, b, cin;
 
 output sum, carry;
 
 assign sum = (a ^ b) ^ cin;         
 
 assign carry = (a & b) | (cin & (a ^ b)); 
 
 endmodule

 FULL SUBRACTOR
 
  module fs(a, b, bin, difference, borrow);
  
  input a, b, bin;
  
  output difference, borrow;
  
  assign difference = (a ^ b) ^ bin; 
  
  assign borrow = (~a & b) | (bin & (~(a ^ b))); 
  
  endmodule
 
*/

**RTL Schematic**

![image](https://github.com/user-attachments/assets/ca29f2cd-d285-4bde-80a3-1df7a799a869)

![image](https://github.com/user-attachments/assets/d2b7903e-6293-40fc-8c5a-9c62c96edb76)


**Output Timing Waveform**

![image](https://github.com/user-attachments/assets/b9925866-de35-484a-94d3-e3f57ef8c781)

![image](https://github.com/user-attachments/assets/b97e835c-a8d2-4336-9b29-c8a02a711f63)


**Result:**

Thus the Full Adder and Full Subtractor circuits are designed and the truth tables is verified using Quartus software.



