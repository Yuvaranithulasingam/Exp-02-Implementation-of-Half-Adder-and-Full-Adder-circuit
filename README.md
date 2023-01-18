# Exp-02-Implementation-of-Half-Adder-and-Full-Adder-circuit

# Implementation-of-Half-Adder-and-Full-Adder-circuit
### AIM:
To design a half adder and full adder circuit and verify its truth table in Quartus using Verilog programming.

### Equipments Required:
Hardware – PCs, Cyclone II , USB flasher
Software – Quartus prime
Theory
Adders are digital circuits that carry out addition of numbers.

### Half Adder
Half adder is a combinational circuit that performs simple addition of two binary numbers. The input variables designate the augend and addend bits; the output variables produce the sum and carry. It is necessary to specify two output variables because the result may consist of two binary digits.

Sum = A’B+AB’ =A ⊕ B Carry = AB

### Full Adder
Full adder is a digital circuit used to calculate the sum of three binary bits. It consists of three inputs and two outputs. Two of the input variables, denoted by A and B, represent the two significant bits to be added. The third input, Cin, represents the carry from the previous lower significant position. Two outputs are necessary because the arithmetic sum of three binary digits ranges in value from 0 to 3, and binary 2 or 3 needs two digits. The two outputs are sum and carry.

Sum =A’B’Cin + A’BCin’ + ABCin + AB’Cin’ = A ⊕ B ⊕ Cin Carry = AB + ACin + BCin

 ![image](https://user-images.githubusercontent.com/36288975/163552156-a13e5a56-c638-4110-97d9-8896907c8d25.png)

#### Figure -01 HALF ADDER 


![image](https://user-images.githubusercontent.com/36288975/163552057-b3547877-6d07-45b4-b7e0-bcfebfad9e1d.png)

#### Figure -02 FULL ADDER 

### Procedure

Connect the supply (+5V) to the circuit
Switch ON the main switch
If the output is 1, then the led glows.
### 
Program:
```
module halfadder(a,b,sum,carry);
input a,b;
output sum,carry;
xor(sum,a,b);
and(carry,a,b);
endmodule
```
```
module fulladder(a,b,c,sum,carry);
inputs a,b,c;
outputs sum,carry;
assign sum=((a^b)^c);
assign carry=((a&b)|(b&c)|(c&a));
endmodule
```
/*
Program to design a half adder and full adder circuit and verify its truth table in quartus using Verilog programming.

Developed by: Yuvarani T

RegisterNumber:  22009033
*/
 Truthtable

HALF ADDER

![half add truthtable](https://user-images.githubusercontent.com/121418522/213155894-d0ce5c3f-74aa-47f8-9000-184a933b630f.png)

FULL ADDER

![full add truthtable](https://user-images.githubusercontent.com/121418522/213155976-04b98b6c-20d1-4c7f-93df-4a4341cd5570.png)
 
RTL realization

HALF ADDER

![Screenshot (11)](https://user-images.githubusercontent.com/121418522/211793440-90b0d800-6112-4100-9c37-52166866db60.png)

FULL ADDER

![FULL ADD RTL](https://user-images.githubusercontent.com/121418522/213156336-4835c18e-829e-49ef-90e1-21bf44f3088e.png)

### TIMING DIAGRAM

HALF ADDER
![Screenshot (20)](https://user-images.githubusercontent.com/121418522/211792436-fdcd781f-1b81-449a-bc8c-92445ff46227.png)

FULL ADDER
![FULL ADD TIMING](https://user-images.githubusercontent.com/121418522/213156500-3203f455-fde7-4a7a-b7b6-ef794f82ad34.png)

### Result:
thus the output for the half adder and full adder are successfully done
