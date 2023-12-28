# Experiment--04-Half-Subtractor-and-Full-subtractor
## Implementation-of-Half-subtractor-and-Full-subtractor-circuit
## AIM:
To design a half subtractor and full subtractor circuit and verify its truth table in Quartus using Verilog programming.

## Equipments Required:
## Hardware – PCs, Cyclone II , USB flasher
## Software – Quartus prime
## Theory
Subtractor circuits take two binary numbers as input and subtract one binary number input from the other binary number input. Similar to adders, it gives out two outputs, difference and borrow (carry-in the case of Adder). There are two types of subtractors.

## Half Subtractor Full Subtractor
## Half Subtractor
The half-subtractor is a combinational circuit which is used to perform subtraction of two bits. It has two inputs, X (minuend) and Y (subtrahend) and two outputs D (difference) and B (borrow). To perform x - y, we have to check the relative magnitudes of x and y. If x ;;, y, we have three possibilities: 0 - 0 = 0, 1 - 0 = 1, and 1 - I = 0. The result is called the difference bit. If x < y, we have 0 - I, and it is necessary to borrow a 1 from the next higher stage. The I borrowed from the next higher stage adds 2 to the minuend bit, just as in the decimal system a borrow adds 10 to a minuend digit. With the minuend equal to 2, the difference becomes 2 - I = 1. The half-subtractor needs two outputs. One output generates the difference and will be designated by the symbol D. The second output, designated B for borrow, generates the binary signal that informs the next stage that a I has been borrowed.
![half-subtractor9](https://user-images.githubusercontent.com/36288975/166112538-58c3bc7c-ee5d-4e6a-ac8d-8e8328efe27a.png)


Sum = X'Y+XY' = X ⊕ Y
Carry=X'Y

## Full Subtractor
A full subtractor is a combinational circuit that performs subtraction involving three bits, namely minuend, subtrahend, and borrow-in . It accepts three inputs: minuend, subtrahend and a borrow bit and it produces two outputs: difference and borrow. 
![full-subtractor6](https://user-images.githubusercontent.com/36288975/166112541-24c68359-3de8-4674-ae22-8272ffc385ed.png)


Diff = A ⊕ B ⊕ Bin B = A'Bin + A'B + BBin

## Procedure



Write the detailed procedure here 


## Program:
/*
Program to design a half subtractor and full subtractor circuit and verify its truth table in quartus using Verilog programming.
Developed by: v.sanjay
RegisterNumber:  23012749
## Half subtractor:
module half_sub(a,b,difference,borrow);
input a,b;
output difference,borrow;
wire x;
xor (difference,a,b);
not (x,a);
and (borrow,x,b);
endmodule

## Full subrtractor:
module Full_sub(a,b,bin,difference,borrow);
input a,b,bin;
output difference,borrow;
wire p;
assign difference=((a^b)^bin);
not (p,a);
assign borrow=((p&b)|(p&bin)|(b&bin));
endmodule
*/

## Output:

## Truthtable
## Half subtractor:
![image](https://github.com/sanjayy2431/Experiment--03-Half-Subtractor-and-Full-subtractor/assets/149365143/a02df687-88b1-44d4-9e93-1223d1dd2a26)


## Full subtractor:
![image](https://github.com/sanjayy2431/Experiment--03-Half-Subtractor-and-Full-subtractor/assets/149365143/b1473e6a-79cd-4e31-9a13-8a1988231aff)





##  RTL realization
## Half sub:
![image](https://github.com/sanjayy2431/Experiment--03-Half-Subtractor-and-Full-subtractor/assets/149365143/62e59135-4479-45b7-b1b6-f60adc7c53b1)

## Full subtractor:
![image](https://github.com/sanjayy2431/Experiment--03-Half-Subtractor-and-Full-subtractor/assets/149365143/c333e304-9836-4fb9-a5ba-9b8b8ffe0ae2)



## Timing diagram 
## Half sub:
![image](https://github.com/sanjayy2431/Experiment--03-Half-Subtractor-and-Full-subtractor/assets/149365143/129d8d0e-c242-4ff1-92f1-3b04bf59b1fb)


## Full sub:
![image](https://github.com/sanjayy2431/Experiment--03-Half-Subtractor-and-Full-subtractor/assets/149365143/6a783f0e-7426-40c1-825d-731180cb06e5)



## Result:
Thus the half subtractor and full subtractor circuits are designed and the truth tables is verified using quartus software.
