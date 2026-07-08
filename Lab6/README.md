# Lab 6: VHDL Code for Combinational Circuits: Code Converter

## Objective
* To design and simulate a BCD-to-Excess-3 code converter in VHDL.
* To design and simulate a Binary-to-Gray code converter in VHDL.

## Theory

### BCD to Excess-3
Excess-3 (XS-3) is a non-weighted BCD code obtained by adding 3 (0011) to each BCD digit. It is self-complementing, making it useful in arithmetic circuits.

| Decimal | BCD (DCBA) | Excess-3 (WXYZ) |
| :---:   | :---:      | :---:           |
| 0       | 0000       | 0011            |
| 1       | 0001       | 0100            |
| 2       | 0010       | 0101            |
| 3       | 0011       | 0110            |
| 4       | 0100       | 0111            |
| 5       | 0101       | 1000            |
| 6       | 0110       | 1001            |
| 7       | 0111       | 1010            |
| 8       | 1000       | 1011            |
| 9       | 1001       | 1100            |

### Binary to Gray Code
Gray code is a binary numeral system where two successive values differ by only one bit. It is widely used in rotary encoders and error minimization.

The conversion rule: $G_i = B_i \oplus B_{i+1}$ (MSB of Gray = MSB of Binary).

| Decimal | Binary (DCBA) | Gray Code (WXYZ) |
| :---:   | :---:         | :---:            |
| 0       | 0000          | 0000             |
| 1       | 0001          | 0001             |
| 2       | 0010          | 0011             |
| 3       | 0011          | 0010             |
| 4       | 0100          | 0110             |
| 5       | 0101          | 0111             |
| 6       | 0110          | 0101             |
| 7       | 0111          | 0100             |
| 8       | 1000          | 1100             |
| 9       | 1001          | 1101             |

## Output

### For BCD to XS3:
![alt text](xs3.png)

### For BCS to Gray:
![alt text](Gray.png)

## Discussion and Conclusion: 
This lab successfully verified the design and simulation of a BCD-to-Excess-3 converter and a Binary-to-Gray code converter using VHDL, GHDL, and GTKWave. The BCD-to-Excess-3 module correctly added a binary $3$ (`0011`) to the inputs, confirming its function for arithmetic operations. The Binary-to-Gray module successfully implemented concurrent XOR logic ($G_i = B_{i+1} \oplus B_i$) to produce a unit-distance output where only one bit changes at a time. The final waveforms matched our expected truth tables perfectly, validating that both combinational circuits are logically correct and demonstrating how alternative coding formats efficiently eliminate timing hazards and optimize digital hardware.