Integer Arithmetic Overflow Explorer

An interactive browser-based visualization designed to help students understand integer arithmetic overflow and the behavior of fixed-width integers.

Overview

Computers store integers using a fixed number of bits. Because the number of bits is limited, there is a maximum and minimum value that can be represented.

For example, an 8-bit unsigned integer can represent values from:

0 to 255


If the program calculates:

255 + 1 = 256


the mathematical result requires 9 bits:

256 = 100000000₂


However, an 8-bit integer only has room for:

00000000


The extra bit is discarded, causing the stored value to wrap around to 0.

This project provides an interactive way to visualize that process.

Features

Interactive addition of two integer values.

Support for 4-bit, 8-bit, and 16-bit integers.

Unsigned integer interpretation.

Signed two's-complement interpretation.

Visual representation of the underlying binary bits.

Automatic detection of arithmetic overflow.

Side-by-side comparison of:

The mathematical result.

The stored unsigned result.

The stored signed result.

Preset examples such as 255 + 1.

Explanation of why 255 + 1 becomes 0 in an 8-bit unsigned integer.

Interactive quiz to test understanding.

Fully self-contained HTML file with no external libraries or dependencies.

How to Run

No installation or web server is required.

Download or clone this repository.

Open index.html in a modern web browser.

Enter two values.

Select the integer width and interpretation.

Observe the mathematical result, stored result, and binary representation.

For the clearest demonstration, select:

Integer width: 8-bit
Interpretation: Unsigned
First value: 255
Value to add: 1


Then click Try 255 + 1.

The visualization will show:

255 + 1 = 256


Mathematically, the answer is 256. However, an 8-bit unsigned integer can only store values from 0 through 255. The binary calculation is:

  11111111
+ 00000001
-----------
100000000


Only eight bits can be stored, so the leading 1 is discarded:

00000000


Therefore:

255 + 1 → 0


This is integer arithmetic overflow.

Signed vs. Unsigned Integers

The application also demonstrates that the same binary bits can represent different values depending on whether they are interpreted as signed or unsigned.

For an 8-bit integer:

Unsigned
0 through 255

Signed two's complement
-128 through 127


For example:

Binary:   11111111

Unsigned: 255
Signed:   -1


This demonstrates why programmers need to understand both the bit representation and the interpretation of those bits.

Learning Objectives

After using this visualization, a learner should be able to:

Explain what a fixed-width integer is.

Calculate the range of values representable with a given number of bits.

Explain why arithmetic overflow occurs.

Demonstrate how an integer can wrap around after reaching its maximum value.

Convert simple integer values to binary.

Explain the difference between signed and unsigned integer interpretation.

Explain how the same bit pattern can represent different numerical values.

Technologies

This project uses:

HTML5

CSS3

JavaScript

Standard web browser APIs

There are no external packages, frameworks, APIs, or dependencies.

Project Structure
.
├── index.html
├── README.md
└── reflection.md


index.html contains the complete interactive visualization.

README.md provides information about the project and how to use it.

reflection.md contains the development reflection required for the assignment.

Safety

This application is intended solely as an educational visualization.

It does not contain:

Exploit code

Shellcode

Attack tools

Vulnerability exploitation

Network attacks

Malware

Credential collection

Access to real systems

The goal is to demonstrate the underlying computer-science concept of integer overflow in a safe environment.

AI-Assisted Development

AI assistance was used during development to help design the user interface, generate and refine HTML/CSS/JavaScript, explain integer overflow concepts, and improve the educational presentation.

The resulting application was reviewed and adjusted to ensure that the interaction demonstrates the intended concept clearly and safely.

Example Experiment

Try the following experiment:

Integer width: 4-bit
Interpretation: Unsigned
First value: 15
Value to add: 1


A 4-bit unsigned integer can represent:

0 through 15


The calculation is:

15 + 1 = 16


Binary:

  1111
+ 0001
------
10000


The result requires five bits, but only four are available:

0000


Therefore:

15 + 1 → 0


This is the same fundamental behavior demonstrated by the 8-bit 255 + 1 example.

License

This project was created for educational purposes as part of a course assignment.
