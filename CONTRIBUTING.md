Contributing to the Digital Logic Course Repository

First off, welcome! Thank you for your interest in contributing to the Digital Logic Course Repo. This repository serves as a living, open-source educational resource for students and educators worldwide. 

Whether you are fixing a typo, adding a complex sequential circuit, or writing a tutorial on a logic simplification method, your contributions help make learning digital logic accessible to everyone.

This document is a comprehensive guide to help you submit new methods, circuits, and testbenches correctly.

---

CODE OF CONDUCT
By participating in this project, you agree to abide by our Code of Conduct. We expect all contributors to maintain a respectful, inclusive, and collaborative environment. Constructive feedback on pull requests is highly encouraged; academic elitism is not.

---

CONTRIBUTION WORKFLOW
We follow the standard GitHub "Fork and Pull" workflow:

1. Fork the repository to your own GitHub account.
2. Clone the project to your local machine.
3. Create a Branch for your feature or fix. Use a descriptive name (e.g., feat/add-carry-lookahead).
4. Develop your circuit, testbench, or documentation.
5. Test your logic to ensure it simulates correctly.
6. Commit your changes following our Commit Guidelines below.
7. Push to your fork.
8. Open a Pull Request from your fork to the main branch of our repository.

---

HOW TO SUBMIT NEW CIRCUITS
We accept circuit implementations in Verilog (.v), VHDL (.vhd), and Logisim (.circ). To submit a new circuit, you must meet the following requirements:

1. Naming Conventions:
File names must be snake_case (Examples: full_adder.v, d_flip_flop.vhd, mod_10_counter.circ).

2. Required Files:
Every new circuit submission must include:
* The source file in the correct directory.
* A corresponding testbench.
* A local README.md inside the specific circuit's folder explaining the theory.

3. Code Documentation:
Include a header block at the top of your source code listing the Module Name, Author, Description, Inputs, and Outputs.

---

HOW TO SUBMIT NEW METHODS & TUTORIALS
Theoretical methods (e.g., Boolean algebra proofs, Karnaugh map walkthroughs) live in the /methods/ directory. 

Guidelines for Tutorials:
* Clear Objectives: Start with a brief paragraph explaining what the method achieves.
* Visual Aids: Use text tables for Truth Tables and State Tables.
* Step-by-Step Logic: Break down math or algorithms into numbered steps. 
* Practical Example: Every method must conclude with a worked-out example.

---

TESTING & VALIDATION REQUIREMENTS
We do not accept broken circuits. You must prove your circuit works.

For Logisim:
* Ensure there are no floating pins (use pull-up/pull-down resistors or constants where necessary).
* Label all inputs and outputs clearly in the UI.
* Test all states before saving the file.

---

PULL REQUEST (PR) PROCESS
When you open a PR, a template will automatically populate. Please fill it out completely.

Before submitting, ensure you have:
* Followed the naming conventions.
* Included a testbench for your circuit.
* Verified that your simulation passes locally.
* Updated the documentation to reflect your changes.

Course maintainers will review your PR within 3 to 5 business days. We may request changes—don't be discouraged, this is part of the engineering process! Once approved, a maintainer will merge your PR into the main branch.

Thank you for contributing to the education of future computer engineers!
