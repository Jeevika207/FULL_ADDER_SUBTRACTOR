# FULL_ADDER_SUBTRACTOR

**EXPERIMENT 4**

**DATE**- 22/10/2024 

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

# Truth Table
![WhatsApp Image 2024-12-21 at 09 58 41_5d681529](https://github.com/user-attachments/assets/bc098c26-9e2e-44b2-b08d-892fe39174ef)


**Full Subtractor**

A full subtractor is a combinational circuit that performs subtraction involving three bits, namely minuend, subtrahend, and borrow-in . It accepts three inputs: minuend, subtrahend and a borrow bit and it produces two outputs: difference and borrow.

![image](https://github.com/naavaneetha/FULL_ADDER_SUBTRACTOR/assets/154305477/02b24f51-ab51-4304-9ad6-7b81ffc1ead5)

Diff = A ⊕ B ⊕ Bin 

Borrow out = A'Bin + A'B + BBin

**Truthtable**

# Truthtable

![WhatsApp Image 2024-12-21 at 09 59 00_fcb9fcab](https://github.com/user-attachments/assets/3de697b1-b45f-48eb-bccb-e2c3fee632af)

**Procedure**

Write the detailed procedure here

1.Type the program in Quartus software.

2.Compile and run the program.

3.Generate the RTL schematic and save the logic diagram.

4.Create nodes for inputs and outputs to generate the timing diagram.

5.For different input combinations generate the timing diagram.

**Program:**

## Full_adder
```
module fa(a,b,cin,sum,carry);
input a,b,cin;
output sum,carry;
assign sum=( (a ^ b)^cin);
assign carry= ( (a & b)| ( cin &(a ^ b )));
endmodule

```

## Full_subtractor
```
module fs(a,b,bin,difference,borrow);
input a,b,bin;
output difference,borrow;
assign difference= ( (a ^ b)^bin);
assign borrow= ( ( ~a & b)| ( bin & (~(a ^ b ))));
endmodule


```
/* Program to design a half subtractor and full subtractor circuit and verify its truth table in quartus using Verilog programming.

Developed by: JEEVIKA R

RegisterNumber: 24900508

**RTL Schematic**
**Full Adder**
![image](https://github.com/user-attachments/assets/71384764-ab89-430d-b8c1-c28f73e38f01)

**Full Subtractor**
![image](https://github.com/user-attachments/assets/db26c434-e6d4-4fcd-9f35-100d54ecc450)

**Output Timing Waveform**
**Full Adder**
![image](https://github.com/user-attachments/assets/4743f238-4990-411a-bab0-8758d47d36e5)
**Full Subtractor**
![image](https://github.com/user-attachments/assets/9b6bc27e-fafb-4ede-850b-9a1cb85b811c)

**Result:**

Thus the Full Adder and Full Subtractor circuits are designed and the truth tables is verified using Quartus software.



