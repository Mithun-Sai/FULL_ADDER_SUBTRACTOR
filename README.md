# FULL_ADDER_SUBTRACTOR
Implementation-of-Full-Adder-and-Full-subtractor-circuit

## AIM:
To design a Full Adder and Full Subtractor circuit and verify its truth table in Quartus using Verilog programming.

## Equipments Required:
Hardware – PCs, Cyclone II , USB flasher

Software – Quartus prime

## Full Adder and Full Subtractor

### Full Adder
Full adder is a digital circuit used to calculate the sum of three binary bits. It consists of three inputs and two outputs. Two of the input variables, denoted by A and B, represent the two significant bits to be added. The third input, Cin, represents the carry from the previous lower significant position. Two outputs are necessary because the arithmetic sum of three binary digits ranges in value from 0 to 3, and binary 2 or 3 needs two digits. The two outputs are sum and carry.

Sum =A’B’Cin + A’BCin’ + ABCin + AB’Cin’ = A ⊕ B ⊕ Cin 

Carry = AB + ACin + BCin

![image](https://github.com/naavaneetha/FULL_ADDER_SUBTRACTOR/assets/154305477/0f30ba51-5ffb-4198-845f-18e054f675e7)

**Figure -1 FULL ADDER**

### Full Subtractor
A full subtractor is a combinational circuit that performs subtraction involving three bits, namely minuend, subtrahend, and borrow-in . It accepts three inputs: minuend, subtrahend and a borrow bit and it produces two outputs: difference and borrow.

![image](https://github.com/naavaneetha/FULL_ADDER_SUBTRACTOR/assets/154305477/02b24f51-ab51-4304-9ad6-7b81ffc1ead5)

**Figure -2 FULL SUBTRACTOR**

Diff = A ⊕ B ⊕ Bin 

Borrow out = A'Bin + A'B + BBin

## Truthtable
### FULL ADDER
<img width="429" height="395" alt="image" src="https://github.com/user-attachments/assets/fbb73298-8832-4494-9bbb-67758f8bfd05" />



### FULL SUBTRACTOR
<img width="438" height="393" alt="image" src="https://github.com/user-attachments/assets/72b582df-4ce4-4b3c-95b9-5daadb26308b" />

## Procedure

Type the program in Quartus software.

Compile and run the program.

Generate the RTL schematic and save the logic diagram.

Create nodes for inputs and outputs to generate the timing diagram.

For different input combinations generate the timing diagram.


## Program:

Program to design a half subtractor and full subtractor circuit and verify its truth table in quartus using Verilog programming.

Developed by: Mithun Sai P
RegisterNumber: 212225100026

```
module exp4(a, b, cin, sum, carry,
            x, y, bin, diff, borrow);

input a, b, cin;
input x, y, bin;

output sum, carry;
output diff, borrow;

// Full Adder
assign sum = a ^ b ^ cin;
assign carry = (a & b) | (b & cin) | (a & cin);

// Full Subtractor
assign diff = x ^ y ^ bin;
assign borrow = (~x & y) | (~x & bin) | (y & bin);

endmodule
```

## RTL Schematic:
<img width="1366" height="728" alt="image" src="https://github.com/user-attachments/assets/0915a2a0-19ea-4463-8338-5273b4ca5097" />

## Output Timing Waveform:
<img width="1366" height="728" alt="image" src="https://github.com/user-attachments/assets/716aecc7-7729-412e-8f5d-c21b5027bf7f" />

## Result:

Thus the Full Adder and Full Subtractor circuits are designed and the truth tables is verified using Quartus software.



