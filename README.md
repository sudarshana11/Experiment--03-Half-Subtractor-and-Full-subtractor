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
Use module projname(input,output) to start the Verilog programmming.

Assign inputs and outputs using the word input and output respectively.

Use defined keywords like wire,assign and required logic gates to represent the boolean expression.

Use each output to represnt onre for differnce and the other for borrow.

End the verilog program using keyword endmodule


Write the detailed procedure here 


## Program:
/*
module project_4_1(a,b,borrow,diff);
input a,b;
output borrow,diff;
assign borrow=~a&b;
assign diff=a^b;
endmodule
Program to design a half subtractor and full subtractor circuit and verify its truth table in quartus using Verilog programming.
Developed by: SUDARSHANA S
RegisterNumber: 212223050054
*/

## Output:

## Truthtable
![image](https://github.com/sudarshana11/Experiment--03-Half-Subtractor-and-Full-subtractor/assets/155507129/92d7091f-cb7a-4fa0-a146-f3bcaf65922f)



##  RTL realization
![image](https://github.com/sudarshana11/Experiment--03-Half-Subtractor-and-Full-subtractor/assets/155507129/151e8aad-5f33-4fc0-ab1f-33abebe2bb5b)

## Timing diagram 
![image](https://github.com/sudarshana11/Experiment--03-Half-Subtractor-and-Full-subtractor/assets/155507129/b8167d2e-da4d-422f-bb77-a93d928279a0)
Full Subtractor
A full subtractor is a combinational circuit that performs subtraction involving three bits, namely minuend, subtrahend, and borrow-in . It accepts three inputs: minuend, subtrahend and a borrow bit and it produces two outputs: difference and borrow. full-subtractor6

Diff = A ⊕ B ⊕ Bin B = A'Bin + A'B + BBin

# Program:
module project_4_2(a,b,bin,borrow,diff);
input a,b,bin;
output diff,borrow;
assign diff=(a^b)^bin;
assign borrow=((~a)&&bin)||(b&&bin)||((~a)&&b);
endmodule

# Truthtable
![image](https://github.com/sudarshana11/Experiment--03-Half-Subtractor-and-Full-subtractor/assets/155507129/4a0b660f-473d-4e73-b4ee-92aeaa0e87d4)


# RTL realization
![image](https://github.com/sudarshana11/Experiment--03-Half-Subtractor-and-Full-subtractor/assets/155507129/2c1be3cb-e77d-497b-9602-d93db6000b5b)


# Timing diagram
![image](https://github.com/sudarshana11/Experiment--03-Half-Subtractor-and-Full-subtractor/assets/155507129/6eb11a9c-dc99-4e23-a122-96e1132d782f)


## Result:
Thus the half subtractor and full subtractor circuits are designed and the truth tables is verified using quartus software.
