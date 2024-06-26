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

**Program:**
```
/* Program to design a half subtractor and full subtractor circuit and verify its truth table in quartus using Verilog programming. 
Developed By:Adhl Hameed
Registration no: 212223050002
*/
module EX04(a,b,c,sum,carry);
input a,b,c;
output sum,carry;
//FULL ADDER
assign sum = a^b^c;
assign carry = (a&b) | (b&c) | (a&c);
endmodule

module EX04(a,b,c,BO,DIFF);
input a,b,c;
output BO,DIFF;
wire a0;
not (a0,a);
//FULL SUBTRACTOR
assign DIFF = a^b^c;
assign BO = (a0&b) | (b&c) | (a0&c);
endmodule
```
**RTL Schematic**

![image](https://github.com/adhlhameed/FULL_ADDER_SUBTRACTOR/assets/168260238/425afa74-081e-4ae2-93aa-b394ad8fe424)
![image](https://github.com/adhlhameed/FULL_ADDER_SUBTRACTOR/assets/168260238/209461b8-34b4-47d4-9d4b-82ea1d6f80dd)




**Output Timing Waveform**

![image](https://github.com/adhlhameed/FULL_ADDER_SUBTRACTOR/assets/168260238/f8bc39d0-7976-45b7-8cbe-ecfcc67a3b7c)
![image](https://github.com/adhlhameed/FULL_ADDER_SUBTRACTOR/assets/168260238/9e5e4535-22c7-4591-9d46-0e350d81f411)



**Result:**

Thus the Full Adder and Full Subtractor circuits are designed and the truth tables is verified using Quartus software.



