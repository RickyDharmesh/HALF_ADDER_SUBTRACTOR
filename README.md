# HALF_ADDER_SUBTRACTOR
Implementation-of-Half-Adder-and-Half Subtractor-circuit

AIM:

To design a half adder and half subtractor circuit and verify its truth table in Quartus using Verilog programming.

Equipments Required:

Hardware – PCs, Cyclone II , USB flasher

Software – Quartus prime Theory Adders are digital circuits that carry out the addition of numbers.

Half Adder

Half adder is a combinational circuit that performs simple addition of two binary numbers. The input variables designate the augend and addend bits; the output variables produce the sum and carry. It is necessary to specify two output variables because the result may consist of two binary digits.

Sum = A’B+AB’ =A ⊕ B Carry = AB


Figure -01 HALF ADDER

<img width="449" height="225" alt="image" src="https://github.com/user-attachments/assets/a289139c-1927-40e2-a6a4-927fe6b3a46f" />


Half Subtractor

The half-subtractor is a combinational circuit which is used to perform subtraction of two bits. It has two inputs, X (minuend) and Y (subtrahend) and two outputs D (difference) and B (borrow). To perform x - y, we have to check the relative magnitudes of x and y. If x ;;, y, we have three possibilities: 0 - 0 = 0, 1 - 0 = 1, and 1 - I = 0. The result is called the difference bit. If x < y, we have 0 - I, and it is necessary to borrow a 1 from the next higher stage. The I borrowed from the next higher stage adds 2 to the minuend bit, just as in the decimal system a borrow adds 10 to a minuend digit. With the minuend equal to 2, the difference becomes 2 - I = 1. The half-subtractor needs two outputs. One output generates the difference and will be designated by the symbol D. The second output, designated B for borrow, generates the binary signal that informs the next stage that a I has been borrowed.


Diff = A’B+AB’ =A ⊕ B Borrow = A’B



Figure -02 HALF Subtractor

<img width="524" height="298" alt="image" src="https://github.com/user-attachments/assets/2f47276c-2517-485e-be52-f68b379f2886" />

#Procedure
Procedure to Design a Half Adder

Identify the two single-bit binary inputs A and B.

Construct the truth table showing Sum (S) and Carry (C) for all input combinations.

From the truth table, derive the Boolean expressions: S = A ⊕ B, C = A · B.

Implement the Sum using an XOR gate and the Carry using an AND gate.

Verify the circuit output for all input combinations using the truth table.

Procedure to Design a Half Subtractor

Identify the two single-bit inputs A (minuend) and B (subtrahend).

Prepare the truth table showing Difference (D) and Borrow (Bo) for all cases.

Derive the Boolean expressions: D = A ⊕ B, Bo = A̅ · B.

Implement the Difference using an XOR gate and the Borrow using NOT and AND gates.

Check the correctness of outputs by comparing them with the truth table.

Type the program in Quartus software.

Compile and run the program.

Generate the RTL schematic and save the logic diagram.

Create nodes for inputs and outputs to generate the timing diagram.

For different input combinations generate the timing diagram.

#Program:
Half Adder
```
// Half Adder in Verilog
module half_adder (
    input  wire a, b,     // Inputs
    output wire sum,      // Sum output
    output wire carry     // Carry output
);

    // Logic equations
    assign sum   = a ^ b;   // XOR for sum
    assign carry = a & b;   // AND for carry

endmodule
```
Half Subtractor 
```
// Half Subtractor in Verilog
module half_subtractor (
    input  wire a, b,         // Inputs
    output wire diff, borrow  // Outputs
);

    // Logic equations
    assign diff   = a ^ b;     // XOR for difference
    assign borrow = ~a & b;    // Borrow when a < b

endmodule
```


Developed by: RICKY DHARMESH P 


RegisterNumber: 25016025

#RTL Schematic
Half- adder
<img width="1920" height="1020" alt="Screenshot 2025-12-13 210945" src="https://github.com/user-attachments/assets/4015cc2c-8816-426d-be5e-298916abe399" />
Half- subtractor
<img width="1920" height="1020" alt="Screenshot 2025-12-13 215731" src="https://github.com/user-attachments/assets/07ca3c88-8968-416f-aff0-9cefa69c03dd" />

Result: designed a half adder and half subtractor circuit and verified its truth table in Quartus using Verilog programming.
