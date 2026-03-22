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
<img width="692" height="488" alt="image" src="https://github.com/user-attachments/assets/9fd89f8a-9bea-4fe8-be29-e650c2c3177c" />


**Program:**
 Program to design a half subtractor and full subtractor circuit and verify its truth table in quartus using Verilog programming. 
 **FULL ADDER**
```
module fulladder(sum, cout, a, b, cin);
    output sum;
    output cout;
    input a;
    input b;
    input cin;

	 wire w1,w2,w3;
	 assign w1=a^b;
	 assign w2=a&b;
	 assign w3=w1&cin;
	 assign sum=w1^cin;
	 assign cout=w2|w3;
endmodule


```
**FULL SUBTRACTOR**
```
module sub(a,b,c,x,y,z,sum,dif,car,bor);
input a,b,c,x,y,z;
output sum,dif,car,bor;
assign sum = a^b^c;
assign car = a&b | a&c | b&c;
assign dif = x^y^z;
assign bor = ~x&z | ~x&y | y&z;
endmodule
```
Developed by: Imesha.s RegisterNumber:212225040131


**RTL Schematic**
**FULL ADDER**
<img width="1047" height="591" alt="image" src="https://github.com/user-attachments/assets/ea98ae39-2b80-4c03-992c-6fe311ecb92f" />
**FULL SUBTRACTOR**
<img width="1050" height="595" alt="image" src="https://github.com/user-attachments/assets/a2af6017-e385-4835-beba-275587caae1d" />

**Output Timing Waveform**
**FULL ADDER**
<img width="1047" height="588" alt="image" src="https://github.com/user-attachments/assets/d8fc3e0e-f7ac-4d22-9bb9-54908fbfedec" />
**FULL SUBTRACTOR**
<img width="1050" height="595" alt="image" src="https://github.com/user-attachments/assets/d4c834a2-e48f-45a3-84db-8c6791f7fb72" />

**Result:**

Thus the Full Adder and Full Subtractor circuits are designed and the truth tables is verified using Quartus software.



