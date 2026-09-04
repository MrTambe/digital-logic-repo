```markdown

\# Contributing to the Digital Logic Course



Welcome, student of logic! If you are reading this, you are ready to move from a consumer of knowledge to a contributor. This repository is structured as a living, growing textbook for Sebastian Lague's Digital Logic Simulator. 



Whether you have discovered a highly optimized way to build a 64-bit carry-lookahead adder, or you simply want to fix a typo in the Chapter 2 documentation, your contributions are welcome.



\---



\## Table of Contents

1\. \[What We Are Looking For](#what-we-are-looking-for)

2\. \[The "Book" Philosophy](#the-book-philosophy)

3\. \[How to Submit a New Circuit or Component](#how-to-submit-a-new-circuit-or-component)

4\. \[How to Submit an Alternative Method](#how-to-submit-an-alternative-method)

5\. \[Media \& Video Guidelines](#media--video-guidelines)

6\. \[Pull Request (PR) Process](#pull-request-pr-process)

7\. \[Formatting Standards](#formatting-standards)



\---



\## What We Are Looking For



We welcome contributions in the following areas:

\*   \*\*New Components:\*\* Missing logic gates, advanced ALU designs, new I/O drivers, or computer architecture components (16-bit, 32-bit, 64-bit).

\*   \*\*Alternative Methods:\*\* Found a way to build a circuit with fewer gates? Less propagation delay? Submit it as a new `Method\_XX# Contributing to the Digital Logic Course Repository



First off, welcome! Thank you for your interest in contributing to the \*\*Digital Logic Course Repo\*\*. This repository serves as a living, open-source educational resource for students and educators worldwide. 



Whether you are fixing a typo, adding a complex sequential circuit, or writing a tutorial on a logic simplification method, your contributions help make learning digital logic accessible to everyone.



This document is a comprehensive guide to help you submit new methods, circuits, and testbenches correctly.



\---



\## Table of Contents



1\. \[Code of Conduct](#code-of-conduct)

2\. \[Contribution Workflow](#contribution-workflow)

3\. \[Repository Structure](#repository-structure)

4\. \[How to Submit New Circuits](#how-to-submit-new-circuits)

5\. \[How to Submit New Methods \& Tutorials](#how-to-submit-new-methods--tutorials)

6\. \[Testing \& Validation Requirements](#testing--validation-requirements)

7\. \[Commit Guidelines](#commit-guidelines)

8\. \[Pull Request (PR) Process](#pull-request-pr-process)



\---



\## Code of Conduct

By participating in this project, you agree to abide by our Code of Conduct. We expect all contributors to maintain a respectful, inclusive, and collaborative environment. Constructive feedback on PRs is highly encouraged; academic elitism is not.



\---



\## Contribution Workflow



We follow the standard GitHub "Fork and Pull" workflow:



1\. \*\*Fork\*\* the repository to your own GitHub account.

2\. \*\*Clone\*\* the project to your local machine:

&#x20;  ```bash

&#x20;  git clone \[https://github.com/your-username/digital-logic-course-repo.git](https://github.com/your-username/digital-logic-course-repo.git)



```



3\. \*\*Create a Branch\*\* for your feature or fix. Use a descriptive name:

```bash

git checkout -b feat/add-carry-lookahead-adder



```





4\. \*\*Develop\*\* your circuit, testbench, or documentation.

5\. \*\*Test\*\* your logic to ensure it simulates correctly.

6\. \*\*Commit\*\* your changes following our \[Commit Guidelines](https://www.google.com/search?q=%23commit-guidelines).

7\. \*\*Push\*\* to your fork:

```bash

git push origin feat/add-carry-lookahead-adder



```





8\. \*\*Open a Pull Request\*\* from your fork to the `main` branch of our repository.



\---



\## Repository Structure



Before contributing, please familiarize yourself with the directory layout:



```text

├── circuits/

│   ├── combinational/    # Adders, Multiplexers, Decoders, Encoders, ALUs

│   └── sequential/       # Flip-Flops, Counters, Registers, FSMs

├── methods/              # Markdown tutorials (K-Maps, Quine-McCluskey, etc.)

├── testbenches/          # Verilog/VHDL testbenches corresponding to circuits

├── logisim\_files/        # .circ files for visual learners

└── assets/               # Images, GTKWave screenshots, truth tables



```



\---



\## How to Submit New Circuits



We accept circuit implementations in \*\*Verilog (.v)\*\*, \*\*VHDL (.vhd)\*\*, and \*\*Logisim (.circ)\*\*. To submit a new circuit, you must meet the following requirements:



\### 1. Naming Conventions



\* File names must be `snake\_case`.

\* Examples: `full\_adder.v`, `d\_flip\_flop.vhd`, `mod\_10\_counter.circ`.



\### 2. Required Files



Every new circuit submission \*\*must\*\* include:



\* The source file (e.g., `circuits/combinational/alu\_4bit.v`).

\* A corresponding testbench (e.g., `testbenches/alu\_4bit\_tb.v`).

\* A local `README.md` inside the specific circuit's folder, or an update to the section's main README.



\### 3. Code Documentation



Include a header block at the top of your source code:



```verilog

/\*

&#x20;\* Module: 4-Bit ALU

&#x20;\* Author: \[Your Name/Handle]

&#x20;\* Description: Performs AND, OR, ADD, and SUB operations.

&#x20;\* Inputs: A\[3:0], B\[3:0], opcode\[1:0]

&#x20;\* Outputs: Result\[3:0], CarryOut

&#x20;\*/



```



\---



\## How to Submit New Methods \& Tutorials



Theoretical methods (e.g., Boolean algebra proofs, Karnaugh map walkthroughs, state reduction algorithms) live in the `/methods/` directory.



\### Guidelines for Markdown Tutorials:



1\. \*\*Clear Objectives:\*\* Start with a brief paragraph explaining what the method achieves.

2\. \*\*Visual Aids:\*\* Use standard Markdown tables for Truth Tables and State Tables.

```markdown

| A | B | Cin | Sum | Cout |

|---|---|-----|-----|------|

| 0 | 1 |  0  |  1  |  0   |



```





3\. \*\*Step-by-Step Logic:\*\* Break down math or algorithms into numbered steps.

4\. \*\*Math Formatting:\*\* Use LaTeX formatting for Boolean algebra where supported, or standard text notation (e.g., `Y = A'B + AB'`).

5\. \*\*Practical Example:\*\* Every method must conclude with a worked-out example.



\---



\## Testing \& Validation Requirements



We do not accept broken circuits. You must prove your circuit works.



\### For Hardware Description Languages (Verilog/VHDL):



1\. \*\*Write a Testbench:\*\* Your testbench must cover edge cases, not just happy paths.

2\. \*\*Include Assertions (Optional but Recommended):\*\* Make your testbench self-checking using `$monitor` or `$display`.

3\. \*\*Provide Proof:\*\* In your Pull Request, include a screenshot of the waveform (from GTKWave, ModelSim, or Vivado) showing the successful simulation.



\### For Logisim:



1\. Ensure there are no floating pins (use pull-up/pull-down resistors or constants where necessary).

2\. Label all inputs and outputs clearly in the UI.

3\. Test all states before saving the `.circ` file.



\---



\## Commit Guidelines



We enforce the \[Conventional Commits](https://www.google.com/search?q=https://www.conventionalcommits.org/) standard to maintain a readable project history.



\*\*Format:\*\* `<type>(<scope>): <subject>`



\*\*Allowed Types:\*\*



\* `feat`: A new circuit, method, or tutorial.

\* `fix`: A bug fix in existing logic or typos in docs.

\* `docs`: Documentation only changes.

\* `test`: Adding missing testbenches.

\* `refactor`: Rewriting code without changing its behavior (e.g., structural to behavioral Verilog).



\*\*Examples:\*\*



\* `feat(combinational): add 16-bit carry lookahead adder`

\* `docs(methods): add tutorial on Quine-McCluskey method`

\* `fix(sequential): resolve race condition in JK flip flop`



\---



\## Pull Request (PR) Process



When you open a PR, a template will automatically populate. Please fill it out completely.



\*\*PR Checklist (Make sure you can check these off):\*\*



\* \[ ] I have read the `CONTRIBUTING.md` guidelines.

\* \[ ] My code follows the repository's naming conventions.

\* \[ ] I have included a testbench for my circuit (if applicable).

\* \[ ] I have verified that my testbench passes locally.

\* \[ ] I have updated the documentation / READMEs to reflect my changes.



\*\*Review Process:\*\*



\* Course maintainers will review your PR within 3-5 business days.

\* We may request changes (e.g., "Please add comments explaining the state transitions"). Don't be discouraged! This is part of the engineering process.

\* Once approved, a maintainer will merge your PR into `main`.



Thank you for contributing to the education of future computer engineers!

