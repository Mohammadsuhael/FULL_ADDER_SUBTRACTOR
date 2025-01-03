# FULL_ADDER_SUBTRACTOR
DATE:8/12/2024
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
FULL ADDER
![Screenshot 2024-12-08 152342](https://github.com/user-attachments/assets/391f2c28-0d9f-4549-b763-342d4c3923e2)







FULL SUBTRACTOR
![Screenshot 2024-12-08 152400](https://github.com/user-attachments/assets/c983b445-a7d5-43a2-8603-7c8029e4f820)




**Procedure**
```
Full Adder:
1.Open Quartus II and create a new project.
2.Use schematic design entry to draw the full adder circuit. 
3.The circuit consists of XOR, AND, and OR gates. 
4.Compile the design, verify its functionality through simulation. 
5.Implement the design on the target device and program it.

```

```

Full Subtractor:
1.Follow the same steps as for the full adder. 
2.Draw the full subtractor circuit using schematic design. 
3.The circuit includes XOR, AND, OR gates to perform subtraction. 
4.Compile, simulate, implement, and program the design similarly to the full adder.

```

**Program:**
```
full adder
module fa(a, b, cin, sum, carry);
    input a, b, cin;
    output sum, carry;

    assign sum = (a ^ b) ^ cin;         
    assign carry = (a & b) | (cin & (a ^ b)); 
endmodule
```


```
full subtractor

module fs(a, b, bin, difference, borrow);
    input a, b, bin;
    output difference, borrow;

    assign difference = (a ^ b) ^ bin; 
    assign borrow = (~a & b) | (bin & (~(a ^ b))); 
endmodule


```
/* Program to design a half subtractor and full subtractor circuit and verify its truth table in quartus using Verilog programming. Developed by: MOHAMMAD SUHAEL RegisterNumber: 24007235
*/

**RTL Schematic**

full adder
![Screenshot 2024-12-08 152841](https://github.com/user-attachments/assets/17534df1-2ab9-4005-be5d-3941abe94df9)


full subtractor

![Screenshot 2024-12-08 152849](https://github.com/user-attachments/assets/d321b248-509e-4e2f-8e51-af672572fd2f)


**Output Timing Waveform**


full adder
![Screenshot 2024-12-08 152954](https://github.com/user-attachments/assets/1c42a293-a6df-40ff-9a28-73fd6c781a66)


full subtractor
![Screenshot 2024-12-08 153001](https://github.com/user-attachments/assets/0e8aa249-569a-4218-a2f7-ddbfe2de781b)



**Result:**

Thus the Full Adder and Full Subtractor circuits are designed and the truth tables is verified using Quartus software.



