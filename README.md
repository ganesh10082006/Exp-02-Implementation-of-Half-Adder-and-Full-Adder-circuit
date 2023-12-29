# Exp-03-Implementation-of-Half-Adder-and-Full-Adder-circuit
# NAME: GANESH.G
# REGISTER NUMBER: 212223230059

### AIM:
To design a half adder and full adder circuit and verify its truth table in Quartus using Verilog programming.

### Equipments Required:
~~~
Hardware – PCs, Cyclone II , USB flasher
Software – Quartus prime
~~~
### Procedure

Connect the supply (+5V) to the circuit
Switch ON the main switch
If the output is 1, then the led glows.

### Theory:
Adders are digital circuits that carry out addition of numbers.

### Half Adder
Half adder is a combinational circuit that performs simple addition of two binary numbers. The input variables designate the augend and addend bits; the output variables produce the sum and carry. It is necessary to specify two output variables because the result may consist of two binary digits.

Sum = A’B+AB’ =A ⊕ B Carry = AB

![image](https://user-images.githubusercontent.com/36288975/163552057-b3547877-6d07-45b4-b7e0-bcfebfad9e1d.png)

### Full Adder
Full adder is a digital circuit used to calculate the sum of three binary bits. It consists of three inputs and two outputs. Two of the input variables, denoted by A and B, represent the two significant bits to be added. The third input, Cin, represents the carry from the previous lower significant position. Two outputs are necessary because the arithmetic sum of three binary digits ranges in value from 0 to 3, and binary 2 or 3 needs two digits. The two outputs are sum and carry.

Sum =A’B’Cin + A’BCin’ + ABCin + AB’Cin’ = A ⊕ B ⊕ Cin Carry = AB + ACin + BCin

 ![image](https://user-images.githubusercontent.com/36288975/163552156-a13e5a56-c638-4110-97d9-8896907c8d25.png)

### Program:
~~~
Program to design a half and full adder circuit and verify its truth table in quartus using Verilog programming.
module half_adder(A,B,C,S);
input A,B;
output S,C;
assign c=A&B;
assign S=A^B;
endmodule
module FullAdder(a,b,carryin,sum,carryout);
input a,b,carryin;
output sum,carryout;
wire x,p,q,r;
xor(x,b,carryin);
xor(sum,x,a);
and(p,a,b);
and(q,b,carryin);
and(r,a,carryin);
or(carryout,p,q,r);
endmodule
~~~
### Output:
## Logic symbol & Truth table:
![image](https://github.com/ganesh10082006/Exp-02-Implementation-of-Half-Adder-and-Full-Adder-circuit/assets/151981672/603405d1-6e6a-4e25-9d41-21ee7486e47c)
![image](https://github.com/ganesh10082006/Exp-02-Implementation-of-Half-Adder-and-Full-Adder-circuit/assets/151981672/96ddd1a1-710e-44de-9d4f-0ec40ca49195)

### RTL realization:
![image](https://github.com/ganesh10082006/Exp-02-Implementation-of-Half-Adder-and-Full-Adder-circuit/assets/151981672/eddf84e3-d5bc-4ef5-9a73-ed83e5759da1)
![image](https://github.com/ganesh10082006/Exp-02-Implementation-of-Half-Adder-and-Full-Adder-circuit/assets/151981672/526b9bdd-2746-4236-aefb-2c7cbf2ff453)

### TIMING DIAGRAM:
![image](https://github.com/ganesh10082006/Exp-02-Implementation-of-Half-Adder-and-Full-Adder-circuit/assets/151981672/81757a56-2747-47c2-b7ac-4c1ac8bc3c4c)
![image](https://github.com/ganesh10082006/Exp-02-Implementation-of-Half-Adder-and-Full-Adder-circuit/assets/151981672/36a9174d-ef20-4010-a456-15194746754d)


### Result:
Thus the given logic functions are implemented and their operations are verified using verilog programming
