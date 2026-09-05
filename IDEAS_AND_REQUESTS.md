# 💡 Ideas & Component Requests

Welcome to the **Ideas & Component Requests** board! 

This page serves as a community wishlist for new circuit designs, architectural optimizations, and documentation requests for the **Digital Logic Handbook** repository.

Whether you want to build a missing component, propose an optimization for an existing sub-circuit, or request a specific architecture for Sebastian Lague's *Digital Logic Simulator*, this is where to track it.

---

## 🚦 Request Status Legend

* 🔴 **Unassigned:** Open for anyone to claim and build.
* 🟡 **In Progress:** Currently being designed/tested by a contributor.
* 🟢 **Completed:** Merged into the main repository.

---

## 📌 Active Request Board

### 1. Primitive & Combinational Logic
| Status | Topic / Feature | Description | Priority |
| :---: | :--- | :--- | :---: |
| 🔴 | **Transmission Gate MUX** | Alternative 2-to-1 MUX design using transmission gate logic to reduce gate depth. | Low |
| 🔴 | **16-to-1 Multiplexer** | High-density 16-channel MUX for large bus selection. | Medium |
| 🟡 | **Priority Encoder (8-to-3)** | Expanded priority encoder with active-low/active-high toggle pins. | Medium |
| 🔴 | **Parity Generator & Checker** | 8-bit even/odd parity circuit for error detection. | Low |

---

### 2. Arithmetic & Mathematical Units
| Status | Topic / Feature | Description | Priority |
| :---: | :--- | :--- | :---: |
| 🔴 | **8-Bit Array Multiplier** | Pure combinational 8x8 bit unsigned multiplier. | High |
| 🔴 | **Booth's Algorithm Multiplier** | Sequential signed 8-bit multiplier using Booth's hardware algorithm. | High |
| 🔴 | **8-Bit Restoring Divider** | Iterative hardware division circuit generating Quotient and Remainder. | High |
| 🟡 | **Carry-Skip Adder (CSkA)** | Alternative 8-bit adder bridging Ripple Carry and Carry Lookahead performance. | Medium |
| 🔴 | **Floating Point Unit (16-bit)** | Simplified IEEE-754 half-precision FPU (Adder/Subtractor module). | Critical |

---

### 3. Sequential Logic & Memory Systems
| Status | Topic / Feature | Description | Priority |
| :---: | :--- | :--- | :---: |
| 🔴 | **Dual-Port RAM (16x8)** | Memory bank allowing simultaneous read and write operations on separate buses. | High |
| 🔴 | **Hardware Stack (LIFO)** | 8-byte Hardware Push/Pop stack register with Full and Empty flag outputs. | High |
| 🔴 | **FIFO Circular Queue Buffer** | 16-byte Ring buffer with Read/Write pointers for I/O streaming. | Medium |
| 🟡 | **JK Flip-Flop Master-Slave** | Pulse-triggered master-slave JK flip-flop module preventing race conditions. | Medium |

---

### 4. Display, Input & I/O Interfacing
| Status | Topic / Feature | Description | Priority |
| :---: | :--- | :--- | :---: |
| 🔴 | **Matrix Keypad Decoder** | 4x4 matrix keypad scanner with key-press debouncing circuit. | Medium |
| 🔴 | **ASCII Character Display Driver** | 7-bit ASCII decoder for driving alphanumeric dot-matrix displays. | Low |
| 🔴 | **VGA Signal Generator (Concept)** | Basic horizontal/vertical sync pulse timing generator for display testing. | Low |

---

### 5. CPU Architecture & Control Logic
| Status | Topic / Feature | Description | Priority |
| :---: | :--- | :--- | :---: |
| 🔴 | **Pipelined 8-Bit CPU Core** | 2-stage (Fetch-Execute) overlapped pipeline version of the Chapter 10 CPU. | Critical |
| 🔴 | **Hardware Branch Predictor** | 1-bit dynamic branch history table for instruction prefetching. | High |
| 🟡 | **Interrupt Controller (APIC)** | Priority interrupt handling unit with 4 vector inputs and acknowledge lines. | High |

---

## 🛠️ How to Claim an Open Request

1. **Pick an Unassigned Item (🔴):** Find a request you want to work on.
2. **Open an Issue:** Submit an issue titled `[Claim] - <Component Name>` to let others know you are building it.
3. **Build & Test:** Implement the circuit in Sebastian Lague's simulator and create the documentation/media files.
4. **Submit a PR:** Submit your pull request following our [CONTRIBUTING.md](CONTRIBUTING.md) process.

---

## 💡 How to Suggest a New Idea

Have an idea for a component that isn't listed here?

1. **Open an Issue:** Use the issue template titled `[Idea] - <Your Idea Name>`.
2. **Provide Details:**
   * **Component Purpose:** What does the circuit do?
   * **Category:** Which chapter or architecture level does it belong to?
   * **Key Inputs & Outputs:** Pin definitions and bus widths.
   * **Why it helps:** How it expands the handbook or improves existing builds.

---
*Got a question about a design layout? Feel free to start a discussion in the repository Issues page!*

