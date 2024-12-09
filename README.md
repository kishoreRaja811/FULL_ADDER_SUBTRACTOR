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

**TruthtableFull adder**

![Screenshot 2024-12-09 141638](https://github.com/user-attachments/assets/8024aca9-7f0a-409a-9367-917514d0813e)

**Full subractor**


![Screenshot 2024-12-09 141800](https://github.com/user-attachments/assets/e0d08b0b-3063-4d92-ac0f-78778c386b82)




**Procedure**

Write the detailed procedure here

**Program:**

/* Program to design a half subtractor and full subtractor circuit and verify its truth table in quartus using Verilog programming. Developed by:kishore.r RegisterNumber:24900772
*/


/* Program to design a half subtractor and full subtractor circuit and verify its truth

Full adder




    module fa(a,b,cin,sum,carry);
    input a,b,cin;
    output sum,carry;
    assign sum=( (a ^ b)^cin);
    assign carry= ( (a & b)| ( cin &(a ^ b )));
    endmodule

Full subractor




    module fs(a,b,bin,difference,borrow);
    input a,b,bin;
    output difference,borrow;
    assign difference= ( (a ^ b)^bin);
    assign borrow= ( ( ~a & b)| ( bin & (~(a ^ b ))));
    endmodule


**RTL Schematic**


![Screenshot 2024-12-09 142125](https://github.com/user-attachments/assets/8c9da2c7-1569-49be-b2fe-d8995fcd3daf)



**Output Timing Waveform**


![Screenshot 2024-12-09 142155](https://github.com/user-attachments/assets/ff67befb-6f0c-4563-acd0-4fd237b141e2)



**Result:**

Thus the Full Adder and Full Subtractor circuits are designed and the truth tables is verified using Quartus software.



