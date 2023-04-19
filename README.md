# Experiment--03-Half-Subtractor-and-Full-subtractor
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
Developed by:VAISHNAVI S
RegisterNumber: 212222230165
*/

#CHALF SUBRACTOR:
```
module subractor(A,b,diff,borrow);
input A,b;
output diff,borrow;
wire X;
xor(diff,A,b);
not(X,A);
and(borrow,X,b);
endmodule
```
# FULL SUBRACTOR:
```
module fullsub(A,B,C,Diff,Borrow);
input A,B,C;
output Diff,Borrow;
wire p;
assign Diff = ((A^B)^C);
not(p,A);
assign Borrow = ((p&B)|(p&C)|(B&C));
endmodule
```
# Output:
# HALF SUBRACTOR:
# Truthtable:
![Screenshot 2023-04-19 134304](https://user-images.githubusercontent.com/118541897/233013485-946b4d5e-736c-435b-ab15-1c559280fd72.png)

# LOGIC SYMBOL:
![Screenshot 2023-04-19 134310](https://user-images.githubusercontent.com/118541897/233013674-e5fc9a65-a2fb-48a6-9ded-722a60ee7d73.png)

# RTL realization
![Screenshot 2023-04-19 134314](https://user-images.githubusercontent.com/118541897/233013755-d67baa2c-0184-4faa-8ba2-05c0c442b5c3.png)

# Timing diagram
![Screenshot 2023-04-19 134331](https://user-images.githubusercontent.com/118541897/233013799-c15a5376-91f3-4e6e-86ec-fded3986aaa1.png)

# FULL SUBRACTOR:
# TRUTHTABLE:
![Screenshot 2023-04-19 134340](https://user-images.githubusercontent.com/118541897/233013831-5b0f0b47-0441-40c6-a6f1-13dffb5637eb.png)

# LOGIC SYMBOL:
![Screenshot 2023-04-19 134345](https://user-images.githubusercontent.com/118541897/233013871-b2e5ffd1-241c-4ea7-bcd8-ae3fc2996afa.png)

# RTL REALIZATION:
![Screenshot 2023-04-19 134351](https://user-images.githubusercontent.com/118541897/233013908-5ca7c04f-f337-4a7c-ac0c-81c5cbfc0caa.png)

# TIMING DIAGRAM:
![Screenshot 2023-04-19 134358](https://user-images.githubusercontent.com/118541897/233013958-04f0ee31-3bff-4ba6-9121-6b67f3be6cde.png)

# Result:
Thus the half subtractor and full subtractor circuits are designed and the truth tables is verified using quartus software.
