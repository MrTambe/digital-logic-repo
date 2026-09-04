\# 🖥️ Digital Logic Design: From Gates to a Full 8-Bit Computer



> \*\*An interactive, open-source course and component library built for Sebastian Lague's Digital Logic Simulator.\*\*



Welcome to the master repository. This is not just a collection of files; it is a \*\*comprehensive, interactive book\*\* designed to take you from the absolute basics of boolean logic (0s and 1s) to the complete architectural design of a functioning 8-bit computer. 



Whether you are a beginner trying to understand how an `AND` gate works, or an advanced engineer looking for highly optimized, low-propagation-delay carry lookahead adders, you will find it here.



\---



\## 📖 How to Read This "Book"



Every component in this repository has its own dedicated chapter and sub-directory. We have moved away from heavy, boring text blocks. Instead, inside each chapter you will find:



1\. \*\*Deep-Dive Theory:\*\* The \*why\* and \*how\* behind the circuit, written clearly by industry veterans.

2\. \*\*Compact Truth Tables:\*\* 5x2 formatted tables to quickly reference input/output states without scrolling for days.

3\. \*\*Multiple Design Methods:\*\* Because in digital logic, there is rarely just one way to build something. We provide the "Beginner/Readable" method and the "Optimized/High-Speed" method.

4\. \*\*Live Video Demonstrations:\*\* Embedded `.mp4` files showing the circuit running live in the simulator. 



\---



\## 🚀 Getting Started



1\. \*\*Download the Simulator:\*\* If you haven't already, grab \[Sebastian Lague's Digital Logic Simulator](https://github.com/SebLague/Digital-Logic-Sim).

2\. \*\*Navigate the Index:\*\* Use the Table of Contents below to jump straight into a chapter.

3\. \*\*Replicate \& Experiment:\*\* Watch the embedded videos, read the theory, and try to build the components yourself. 



\---



\## 📚 Table of Contents



\### Part I: The Fundamentals

\* \*\*\[Chapter 01: Introduction \& Setup](./Chapter\_01\_Introduction\_And\_Setup/)\*\*

&#x20; \* 1.0 Welcome \& Course Overview

&#x20; \* 1.1 Sebastian Lague Simulator Guide

&#x20; \* 1.2 How to Read Compact Truth Tables

\* \*\*\[Chapter 02: Primitive Gates](./Chapter\_02\_Primitive\_Gates/)\*\*

&#x20; \* 2.1 NOT Gate

&#x20; \* 2.2 AND Gate

&#x20; \* 2.3 OR Gate \*(Derived vs. Optimized)\*

&#x20; \* 2.4 NAND Gate

&#x20; \* 2.5 NOR Gate

&#x20; \* 2.6 XOR \& XNOR Gates



\### Part II: Traffic Control \& Routing

\* \*\*\[Chapter 03: Combinational Logic](./Chapter\_03\_Combinational\_Logic/)\*\*

&#x20; \* 3.1 Multiplexers (MUX) \*(2-to-1 up to 8-Bit Wide Buses)\*

&#x20; \* 3.2 Demultiplexers (DEMUX)

&#x20; \* 3.3 Decoders

&#x20; \* 3.4 Encoders \& Priority Encoders



\### Part III: Doing The Math

\* \*\*\[Chapter 04: Arithmetic Logic Unit (ALU)](./Chapter\_04\_Arithmetic\_Logic\_Unit/)\*\*

&#x20; \* 4.1 Half Adder \& Full Adder

&#x20; \* 4.2 8-Bit Adder \*(Ripple Carry vs. Carry Lookahead)\*

&#x20; \* 4.3 8-Bit Two's Complement Subtractor

&#x20; \* 4.4 8-Bit Magnitude Comparator

&#x20; \* 4.5 The Full 8-Bit ALU \*(Basic vs. Extended Flag Design)\*



\### Part IV: Memory \& State

\* \*\*\[Chapter 05: Sequential Logic \& Memory](./Chapter\_05\_Sequential\_Logic\_And\_Memory/)\*\*

&#x20; \* 5.1 SR Latch \& D Latch

&#x20; \* 5.2 Edge-Triggered D Flip-Flop

&#x20; \* 5.3 8-Bit Register \*(Standard vs. Gated Clock)\*

&#x20; \* 5.4 8-Bit Shift Register

&#x20; \* 5.5 1-Bit RAM Cell to 16-Byte RAM Bank



\### Part V: Human Interfaces

\* \*\*\[Chapter 06: Display \& I/O Modules](./Chapter\_06\_Display\_And\_IO\_Modules/)\*\*

&#x20; \* 6.1 Hex to 7-Segment Decoder

&#x20; \* 6.2 Binary to BCD (Double Dabble Algorithm)

&#x20; \* 6.3 3-Digit Base-10 Display Driver



\### Part VI: The Architecture

\* \*\*\[Chapter 07: 8-Bit Calculator System](./Chapter\_07\_8Bit\_Calculator\_System/)\*\*

&#x20; \* 7.1 Control Unit \& Clock Generator

&#x20; \* 7.2 Bus Routing \& Tri-State System

\* \*\*\[Chapter 08: Control Logic \& Microcode](./Chapter\_08\_Control\_Logic\_And\_Microcode/)\*\*

&#x20; \* 8.1 Instruction Decoder

&#x20; \* 8.2 Microcode ROM Matrix

\* \*\*\[Chapter 09: Bus Architecture \& Timing](./Chapter\_09\_Bus\_Architecture\_And\_Timing/)\*\*

&#x20; \* 9.1 Shared System Bus Mechanics

\* \*\*\[Chapter 10: Full-Fledged 8-Bit Computer](./Chapter\_10\_Full\_Fledged\_8Bit\_Computer/)\*\*

&#x20; \* 10.1 Fetch-Decode-Execute Cycle

&#x20; \* 10.2 Program Counter \& Memory Mapper

&#x20; \* 10.3 Integrated Execution Unit



> \*Note: Chapters 11 through 100+ detailing 16-bit, 32-bit, and 64-bit architectures are currently in development. See `IDEAS\_AND\_REQUESTS.md` to vote on the roadmap.\*



\---



\## 🤝 How to Contribute



This is a living, breathing course. We want your optimizations, your alternative designs, and your brain-power. 



Found a way to shave 2 ticks off a propagation delay? Built a component we don't have yet? 

1\. Check our \*\*\[CONTRIBUTING.md](./CONTRIBUTING.md)\*\* guide to see how to format your chapter and truth tables.

2\. Submit a PR using the templates in `.github/ISSUE\_TEMPLATE/`.

3\. Drop your component wishlists in \*\*\[IDEAS\_AND\_REQUESTS.md](./IDEAS\_AND\_REQUESTS.md)\*\*.



\---



\## 📜 License



This repository is open-sourced under the MIT License. You are free to copy, modify, distribute, and use these designs in your own educational or personal projects. See the \[LICENSE](./LICENSE) file for full details.

