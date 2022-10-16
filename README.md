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

### Program:
Program to design a half adder and full adder circuit and verify its truth table in quartus using Verilog programming.
Developed by: D.vishnu vardhan reddy.
RegisterNumber: 212221230023 
## Half Adder:
```
module exp3(a,b,sum,carry);
input a,b;
output sum,carry;
xor(sum,a,b);
and(carry,a,b);
endmodule 
```
### Full Adder:
```
module exp3(a,b,c,sum,carry);
input a,b,c;
output sum,carry;
assign sum = ((a^b)^c);
assign carry = ((a&b)|(b&c)|(c&a));
endmodule
```
### Output:
### Half Adder:
### RTL:
![image](https://user-images.githubusercontent.com/94175324/196045835-db0380d8-3e8c-4150-80e0-0d301676e5be.png)
### TIMING DIAGRAM:
![image](https://user-images.githubusercontent.com/94175324/196045867-f2992a64-8506-4f62-8b7a-22fbde01f48b.png)
### TRUTH TABLE:
![image](https://user-images.githubusercontent.com/94175324/196045901-85be9f16-5ceb-4ada-bc6c-07c118e7da09.png)
### Full Adder:
### RTL:
![image](https://user-images.githubusercontent.com/94175324/196045936-a44c8bb8-397f-471c-a7c8-c5eb13caf3a6.png)
### TIMING DIAGRAM:
![image](https://user-images.githubusercontent.com/94175324/196045966-02775363-4600-4a38-b110-e53f9c18dd77.png)
### TRUTH TABLE:
![image](https://user-images.githubusercontent.com/94175324/196045996-c1edbc5d-a497-498d-b2d3-6359efc0cf8e.png)
### Result:
Thus, a half adder and full adder circuit is designed to verify its truth table in Quartus using Verilog programming.
