## NAME : AVINASH T
## ROLL NO : 23014109 


# Exp-02 Implementation of Half Adder and Full Adder circuit

### AIM:
To design a half adder and full adder circuit and verify its truth table in Quartus using Verilog programming.

### Equipments Required:
Hardware – PCs, Cyclone II , USB flasher

Software – Quartus prime

Theory

Adders are digital circuits that carry out addition of numbers.

## THEORY

### Half Adder
Half adder is a combinational circuit that performs simple addition of two binary numbers. The input variables designate the augend and addend bits; the output variables produce the sum and carry. It is necessary to specify two output variables because the result may consist of two binary digits.

Sum = A’B+AB’ =A ⊕ B Carry = AB

### Full Adder
Full adder is a digital circuit used to calculate the sum of three binary bits. It consists of three inputs and two outputs. Two of the input variables, denoted by A and B, represent the two significant bits to be added. The third input, Cin, represents the carry from the previous lower significant position. Two outputs are necessary because the arithmetic sum of three binary digits ranges in value from 0 to 3, and binary 2 or 3 needs two digits. The two outputs are sum and carry.

Sum =A’B’Cin + A’BCin’ + ABCin + AB’Cin’ = A ⊕ B ⊕ Cin Carry = AB + ACin + BCin

![image](https://user-images.githubusercontent.com/36288975/163552156-a13e5a56-c638-4110-97d9-8896907c8d25.png)
![image](https://user-images.githubusercontent.com/36288975/163552057-b3547877-6d07-45b4-b7e0-bcfebfad9e1d.png)

### Procedure

Connect the supply (+5V) to the circuit
Switch ON the main switch
If the output is 1, then the led glows.

### PROGRAM

 ## HALF ADDER
module experiment3(A,B,sum,carry);

input A,B;

output sum,carry;

xor(sum, A,B);

or(carry,A,B);

endmodule

 ## FULL ADDER
module experiment3(a,b,c,Sum,Carry);

input a,b,c;

output Sum,Carry;

assign Sum = ((a^b)^c);

assign Carry = ((a&b) | (b&c) | (c&a));

endmodule

## RTL REALIZATION

  HALF ADDER
  
 ![image](https://github.com/AVINASH05T/Exp-02-Implementation-of-Half-Adder-and-Full-Adder-circuit/assets/151514286/16d874c8-00e3-48b5-8ce8-326d550f4e69)
 
  FULL ADDER
  
 ![image](https://github.com/AVINASH05T/Exp-02-Implementation-of-Half-Adder-and-Full-Adder-circuit/assets/151514286/904700e6-9641-461a-896b-42e942a59b73)
 

### TRUTH TABLE 

  HALF ADDER
  
 ![image](https://github.com/AVINASH05T/Exp-02-Implementation-of-Half-Adder-and-Full-Adder-circuit/assets/151514286/b509b16a-f8b8-4460-888a-ce026019c597)
 
  FULL ADDER
  
 ![image](https://github.com/AVINASH05T/Exp-02-Implementation-of-Half-Adder-and-Full-Adder-circuit/assets/151514286/a130a41c-de74-4b09-b6c8-c5a258eeb9cb)


### TIMING DIAGRAM

  HALF ADDER
  
 ![image](https://github.com/AVINASH05T/Exp-02-Implementation-of-Half-Adder-and-Full-Adder-circuit/assets/151514286/3bd5f337-1b4e-437d-a680-f6e8f26b68cd)
 
  FULL ADDER
  
 ![image](https://github.com/AVINASH05T/Exp-02-Implementation-of-Half-Adder-and-Full-Adder-circuit/assets/151514286/30361308-c9d6-4852-9bb9-cba500bbcd61)


### Result:

Half Adder is a combinational logic circuit that adds two 1-bit digits. The half adder produces a sum of the two inputs. A full adder is a combinational logic circuit that performs an addition operation on three one-bit binary numbers. The full adder produces a sum of the three inputs and carry value.
