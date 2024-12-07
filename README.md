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
```
FULL ADDER
```
![WhatsApp Image 2024-12-07 at 21 21 43_2e07b1e0](https://github.com/user-attachments/assets/b777eb51-e0e3-467e-8743-35cc101b13da)
```
FULL SUBTRACTOR
```

![WhatsApp Image 2024-12-07 at 21 21 46_832c58e1](https://github.com/user-attachments/assets/bff2c816-9ba1-4b97-9fbd-f9290d55542d)



**Procedure**
```
1 Type the program in Quartus software.

2 Compile and run the program.

3 Generate the RTL schematic and save the logic diagram.

4 Create nodes for inputs and outputs to generate the timing diagram.

5 For different input combinations generate the timing diagram.
```
**Program:**
```
FULL ADDER
```
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
```
```
Developed by:Vasanth P
RegisterNumber:24900136
```

**RTL Schematic**
```
FULL ADDER
```

![WhatsApp Image 2024-12-07 at 21 21 45_e4859efc](https://github.com/user-attachments/assets/1fac2a04-cbf2-40ef-9b16-eca7bb7f02ae)
```
FULL SUBTRACTOR
```

![WhatsApp Image 2024-12-07 at 21 21 43_1d53f956](https://github.com/user-attachments/assets/e8425389-de4f-4ced-bce2-a5f74002c466)



**Output Timing Waveform**
```
FULL ADDER
```

![WhatsApp Image 2024-12-07 at 21 21 52_922e5c11](https://github.com/user-attachments/assets/36b47031-ef64-4eb9-9c9f-c7e1e2c60546)
```
FULL SUBTRACTOR
```

![WhatsApp Image 2024-12-07 at 21 22 03_ffe32db4](https://github.com/user-attachments/assets/6d962a7f-0a93-4b27-9c7f-9541080b2702)



**Result:**

Thus the Full Adder and Full Subtractor circuits are designed and the truth tables is verified using Quartus software.



