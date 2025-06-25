# 8085 Assembly Program – Exponentiation by Repeated Addition

This project demonstrates how to compute the power of a number (`Base^Exponent`) using **8085 Assembly Language**. The program simulates multiplication through repeated addition, and exponentiation through repeated multiplication.

It is intended for educational purposes and can be tested on [Sim8085 Online Simulator](https://www.sim8085.com/).

---

## Program Overview

Given:
- Register **B** stores the **base**
- Register **C** stores the **exponent**
- The goal is to compute `B^C` and store the result in **A** (accumulator)

The approach is:
1. Repeatedly add `B` to simulate multiplication
2. Repeatedly multiply to simulate exponentiation
3. Use flags and conditional jumps to handle base cases (like exponent 0 or 1) and overflow (carry)

---

## How It Works

- `MVI A,01`: Initializes result to 1
- `MVI B,03` / `MVI C,01`: Set base and exponent
- Logic checks if exponent is 0 or 1
- Uses registers **D**, **E**, and **H** for intermediate values during multiplication and power loops
- Handles overflow by jumping to the `CARRY` label and returning 0
- Result is stored in register **A** after computation

---

## Try It Out

You can test this program directly in your browser using the [Sim8085 Simulator](https://www.sim8085.com/):

1. Paste the code into the Sim8085 editor
2. Assemble and run the code
3. Check the output in register **A**

---

## Notes

- This algorithm works for small integer values only (due to 8-bit limits)
- Overflow is handled by checking the **Carry** flag
- Program halts at the `END` label with the final result in **A**

---

