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
<img width="344" height="251" alt="image" src="https://github.com/user-attachments/assets/56c91233-3464-4415-902d-0c6f1efd0f99" />
<img width="505" height="520" alt="image" src="https://github.com/user-attachments/assets/dc313ed4-ad02-49d6-a7f2-cd16718615ce" />


**Procedure**

Write the detailed procedure here
 1.Type the program in Quartus software.
 2.Compile and run the program.
 3.Generate the RTL schematic and save the logic diagram.
 4.Create nodes for inputs and outputs to generate the timing diagram.
 5.For different input combinations generate the timing diagram
 
**Program:**
 i)FULL ADDER
 
 module fa(a,b,cin,sum,carry);
 input a,b,cin;
 output sum,carry;
 assign sum=( (a ^ b)^cin);
 assign carry= ( (a & b)| ( cin &(a ^ b )));
 endmodule
 
/* Program to design a half subtractor and full subtractor circuit and verify its truth table in quartus using Verilog programming. Developed by: RegisterNumber:
*/
 ii)FULL SUBTRACTOR
 
 module fs(a,b,bin,difference,borrow);
 input a,b,bin;
 output difference,borrow;
 assign difference= ( (a ^ b)^bin);
 assign borrow= ( ( a & b)| ( bin & ((a ^ b ))));
 endmodule
 
**RTL Schematic**
<img width="792" height="303" alt="image" src="https://github.com/user-attachments/assets/78a8fe89-ca90-4e84-8a74-fca7f2b3e9a3" />
<img width="783" height="250" alt="image" src="https://github.com/user-attachments/assets/47d6dc00-ac05-4f38-98f3-5a6b46c0ec0e" />



**Output Timing Waveform**
<img width="823" height="472" alt="image" src="https://github.com/user-attachments/assets/0dc020c1-9bd4-455e-9824-e5d297f67847" />
<img width="817" height="477" alt="image" src="https://github.com/user-attachments/assets/4c5e5e3d-d4ac-4ef9-b09a-def1e9f72cc0" />


**Result:**

Thus the Full Adder and Full Subtractor circuits are designed and the truth tables is verified using Quartus software.



