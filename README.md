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

FULL ADDER

![Screenshot 2024-11-29 111502](https://github.com/user-attachments/assets/df227008-b29e-4f35-993d-8b667962c4f4)

FULL SUBTRACTOR

![Screenshot 2024-11-29 111514](https://github.com/user-attachments/assets/bbc64cf0-5f2d-49a5-bbb7-f21db7562874)

**Procedure**

 1. Type the program in Quartus software.
 2. Compile and run the program.
 3. Generate the RTL schematic and save the logic diagram.
 4. Create nodes for inputs and outputs to generate the timing diagram.
 5. For different input combinations generate the timing diagram.


**Program:**

/* Program to design a half subtractor and full subtractor circuit and verify its truth table in quartus using Verilog programming.
```
Developed by:S KANUSHA SREE
RegisterNumber:24001268
```
```
FULL ADDER
module fulladd(a,b,cin,sum,carry);
input a,b,cin;
output sum,carry;
assign sum=( (a ^ b)^cin);
assign carry= ( (a & b)| ( cin &(a ^ b )));
endmodule
```
```
FULL SUBTRACTOR
module fullsub(a,b,bin,difference,borrow);
input a,b,bin;
output difference,borrow;
assign difference= ( (a ^ b)^bin);
assign borrow= ( ( ~a & b)| ( bin & (~(a ^ b ))));
endmodule

```
*/

**RTL Schematic**

FULL ADDER

![fulladd](https://github.com/user-attachments/assets/2f970ebe-e29b-4a26-8fd7-1626b8d4eed3)


FULL SUBTRACTOR

![fullsub](https://github.com/user-attachments/assets/8099b64a-11b1-4cb4-ac96-f13a5d948e16)

**Output Timing Waveform**

FULL ADDER
![Screenshot 2024-11-29 110359](https://github.com/user-attachments/assets/b5adea79-a614-47df-b67c-d490e738173c)
FULL SUBTRACTOR
![Screenshot 2024-11-29 111148](https://github.com/user-attachments/assets/1da81fde-3bd5-4947-8eaa-b626e37dcd76)

**Result:**

Thus the Full Adder and Full Subtractor circuits are designed and the truth tables is verified using Quartus software.



