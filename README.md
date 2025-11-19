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

Full Adder

<img width="500" height="281" alt="image" src="https://github.com/user-attachments/assets/7f6e118b-dc4b-45ac-a3c6-d7efb2890f86" />

Full Subtractor

<img width="361" height="236" alt="image" src="https://github.com/user-attachments/assets/a0f263c2-e0ce-47dd-995e-6177dcc464bc" />



**Procedure**

1.Type the program in Quartus software.

2.Compile and run the program.

3.Generate the RTL schematic and save the logic diagram.

4.Create nodes for inputs and outputs to generate the timing diagram.

5.For different input combinations generate the timing diagram.
**Program:**

Full Adder

```

module fa(a,b,c,sum,carry);
input a,b,c;
output sum,carry;
assign sum=(a^b^c);
assign carry=(a&b)|(b&c)|(c&a);
endmodule
```
Full Subtractor
```

module fs(a,b,bin,dif,bout);
input a,b,bin;
output dif,bout;
assign dif=a^b^bin;
assign bout=(a&b)|(bin&(a^b));
endmodule
```
**RTL Schematic**
Full Adder

<img width="990" height="634" alt="ex3 1" src="https://github.com/user-attachments/assets/d4930687-9cc4-4a19-a96e-33f921891b93" />

Full Subtractor

<img width="1183" height="705" alt="ex4 1" src="https://github.com/user-attachments/assets/b3afaff7-dbc8-41e3-95a1-0e9563276167" />



**Output Timing Waveform**

Full Adder

<img width="1920" height="1080" alt="ex 3 1" src="https://github.com/user-attachments/assets/c6c97dbd-8eee-4e7e-90c5-75a5ae58dd8f" />

Full Subtractor

<img width="1920" height="1080" alt="ex 4 1" src="https://github.com/user-attachments/assets/dd7748ff-5029-4ecf-b84c-cb5e3828f762" />



**Result:**

Thus the Full Adder and Full Subtractor circuits are designed and the truth tables is verified using Quartus software.



