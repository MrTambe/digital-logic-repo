
# ⚡ The Digital Logic Handbook ⚡
### *A Modular Component Blueprint & Guide for Sebastian Lague's Digital Logic Simulator*

---

<video src="Chapter_01_Introduction_And_Setup/media/simulator_walkthrough.mp4" controls="controls" style="max-width: 100%;">
  Your browser does not support the video tag.
</video>

---

## 💡 Overview

This repository provides detailed technical documentation, architectural breakdowns, and schematics for digital logic components built within Sebastian Lague's *Digital Logic Simulator*.

Learn how computers are built bottom-up, starting from two basic primitives (`AND` and `NOT` gates) and scaling step-by-step to an 8-bit calculator, a full-fledged 8-bit CPU, and eventually 16-bit, 32-bit, and 64-bit architectures.

---

## 🌟 Key Features of This Repository

* 🎬 **Video Demonstrations:** Every component folder includes `.mp4` video recordings showing signal propagation, pin toggling, and real-time execution.
* 🔀 **Multiple Implementation Methods:** Complex circuits feature sub-folder variants (e.g., `Method_01_Ripple_Carry` vs. `Method_02_Carry_Lookahead`) to highlight trade-offs between logic simplicity and gate propagation speed.
* 📐 **Wire & Gate Blueprints:** Clear wire-by-wire connection specs and signal paths designed for manual layout inside the simulator.

---

## 📚 Master Index / Table of Contents

### 🟢 Chapter 01: Introduction & Simulator Mechanics
* [1.0 Welcome & Architecture Roadmap](Chapter_01_Introduction_And_Setup/1.0_Welcome_And_Course_Overview.md)
* [1.1 Sebastian Lague Simulator Mechanics Guide](Chapter_01_Introduction_And_Setup/1.1_Sebastian_Lague_Simulator_Guide.md)

---

### 🟢 Chapter 02: Primitive Logic Gates
> *Building all fundamental logic operations strictly from starting AND and NOT primitives.*

* **[2.1 NOT Gate (Inverter)](Chapter_02_Primitive_Gates/2.1_NOT_Gate/)** — *Signal inversion*
* **[2.2 AND Gate](Chapter_02_Primitive_Gates/2.2_AND_Gate/)** — *Conjunction logic*
* **[2.3 OR Gate](Chapter_02_Primitive_Gates/2.3_OR_Gate/)**
  * 🔹 [Method 01: Basic NAND-Derived](Chapter_02_Primitive_Gates/2.3_OR_Gate/Method_01_Basic_NAND_Derived/) — *Standard DeMorgan build*
  * ⚡ [Method 02: Low Propagation Delay](Chapter_02_Primitive_Gates/2.3_OR_Gate/Method_02_Low_Propagation_Delay/) — *Optimized gate depth*
* **[2.4 NAND Gate](Chapter_02_Primitive_Gates/2.4_NAND_Gate/)** — *Universal logic gate*
* **[2.5 NOR Gate](Chapter_02_Primitive_Gates/2.5_NOR_Gate/)** — *Inverted OR gate*
* **[2.6 XOR Gate (Exclusive OR)](Chapter_02_Primitive_Gates/2.6_XOR_Gate/)** — *Difference detector & addition foundation*
* **[2.7 XNOR Gate](Chapter_02_Primitive_Gates/2.7_XNOR_Gate/)** — *Equality detector*

---

### 🟡 Chapter 03: Combinational Logic & Data Routing
> *Directing, switching, and translating data streams without clock memory.*

* **3.1 Multiplexers (MUX)**
  * [3.1.1 Basic 2-to-1 MUX](Chapter_03_Combinational_Logic/3.1_Multiplexers_MUX/3.1.1_Basic_2to1_MUX/)
    * 🔹 [Method 01: Standard Logic Gates](Chapter_03_Combinational_Logic/3.1_Multiplexers_MUX/3.1.1_Basic_2to1_MUX/Method_01_Standard_Logic_Gates/)
    * ⚡ [Method 02: Tristate-Optimized Routing](Chapter_03_Combinational_Logic/3.1_Multiplexers_MUX/3.1.1_Basic_2to1_MUX/Method_02_Tristate_Optimized/)
  * [3.1.2 Cascaded 4-to-1 MUX](Chapter_03_Combinational_Logic/3.1_Multiplexers_MUX/3.1.2_Cascaded_4to1_MUX/)
  * [3.1.3 8-Bit Wide Bus MUX](Chapter_03_Combinational_Logic/3.1_Multiplexers_MUX/3.1.3_8Bit_Wide_Bus_MUX/)
* **[3.2 Demultiplexers (DEMUX)](Chapter_03_Combinational_Logic/3.2_Demultiplexers_DEMUX/)** — *Single line to multiple channel dispatch*
* **[3.3 Decoders (2-to-4, 3-to-8)](Chapter_03_Combinational_Logic/3.3_Decoders/)** — *Memory line selection & control line decoding*
* **[3.4 Encoders & Priority Encoders](Chapter_03_Combinational_Logic/3.4_Encoders_And_Priority_Encoders/)** — *Active line conversion to binary address*

---

### 🟠 Chapter 04: Arithmetic & Logic Unit (ALU)
> *The mathematical engine: Binary addition, subtraction, comparison, and bitwise manipulation.*

* **[4.1 Half Adder](Chapter_04_Arithmetic_Logic_Unit/4.1_Half_Adder/)** — *Sum & Carry out without Carry-In*
* **[4.2 Full Adder](Chapter_04_Arithmetic_Logic_Unit/4.2_Full_Adder/)** — *3-bit addition building block*
* **4.3 8-Bit Adders**
  * 🔹 [Method 01: Ripple Carry Adder](Chapter_04_Arithmetic_Logic_Unit/4.3_8Bit_Adder/Method_01_Ripple_Carry_Beginner/) — *Linear delay setup*
  * ⚡ [Method 02: Carry Lookahead Adder](Chapter_04_Arithmetic_Logic_Unit/4.3_8Bit_Adder/Method_02_Carry_Lookahead_Advanced/) — *High-speed parallel carry computation*
* **[4.4 8-Bit Subtractor (2's Complement)](Chapter_04_Arithmetic_Logic_Unit/4.4_8Bit_Subtractor_Twos_Complement/)** — *Invert and Add-1 subtraction core*
* **[4.5 8-Bit Magnitude Comparator](Chapter_04_Arithmetic_Logic_Unit/4.5_8Bit_Magnitude_Comparator/)** — *Greater-Than, Less-Than, Equal-To evaluation*
* **4.6 Full 8-Bit ALU Sub-System**
  * 🔹 [Design 01: Basic Calculator ALU](Chapter_04_Arithmetic_Logic_Unit/4.6_Full_8Bit_ALU/Design_01_Basic_Calculator_ALU/) — *ADD, SUB, AND, OR functions*
  * ⚡ [Design 02: Extended Flag ALU](Chapter_04_Arithmetic_Logic_Unit/4.6_Full_8Bit_ALU/Design_02_Extended_Flag_ALU/) — *Includes Zero (Z), Carry (C), and Overflow (V) status flags*

---

### 🔵 Chapter 05: Sequential Logic & Memory Systems
> *Introducing feedback loops, clocks, and state preservation.*

* **[5.1 SR Latch](Chapter_05_Sequential_Logic_And_Memory/5.1_SR_Latch/)** — *NOR/NAND cross-coupled memory*
* **[5.2 D Latch](Chapter_05_Sequential_Logic_And_Memory/5.2_D_Latch/)** — *Gated data storage*
* **[5.3 Edge-Triggered D Flip-Flop](Chapter_05_Sequential_Logic_And_Memory/5.3_Edge_Triggered_D_FlipFlop/)** — *Single clock cycle state change*
* **5.4 8-Bit Registers**
  * 🔹 [Method 01: Standard D Flip-Flop Array](Chapter_05_Sequential_Logic_And_Memory/5.4_8Bit_Register/Method_01_Standard_D_FlipFlop_Array/)
  * ⚡ [Method 02: Gated Clock Enable Register](Chapter_05_Sequential_Logic_And_Memory/5.4_8Bit_Register/Method_02_Gated_Clock_Enable/)
* **[5.5 8-Bit Shift Register](Chapter_05_Sequential_Logic_And_Memory/5.5_Shift_Register_8Bit/)** — *Serial-to-Parallel & bit-shift arithmetic*
* **[5.6 1-Bit RAM Cell](Chapter_05_Sequential_Logic_And_Memory/5.6_RAM_Cell_1Bit/)** — *Selectable read/write matrix node*
* **[5.7 16-Byte RAM Bank](Chapter_05_Sequential_Logic_And_Memory/5.7_16Byte_RAM_Bank/)** — *Matrix decoding for byte storage*

---

### 🟣 Chapter 06: Display & I/O Modules
> *Interfacing binary state data with human-readable outputs.*

* **[6.1 Hexadecimal to 7-Segment Decoder](Chapter_06_Display_And_IO_Modules/6.1_Hex_To_7Segment_Decoder/)** — *Direct 4-bit to 0-F digit driving*
* **6.2 Binary to BCD (Double Dabble Algorithm)**
  * 🔹 [Method 01: Combinational Shift-Add-3](Chapter_06_Display_And_IO_Modules/6.2_Binary_To_BCD_Double_Dabble/Method_01_Combinational_Shift_Add3/) — *Pure gate cascade*
  * ⚡ [Method 02: Sequential Clocked Dabble](Chapter_06_Display_And_IO_Modules/6.2_Binary_To_BCD_Double_Dabble/Method_02_Sequential_Clocked_Dabble/) — *Iterative register shift*
* **[6.3 3-Digit Base-10 Display Driver](Chapter_06_Display_And_IO_Modules/6.3_3Digit_Base10_Display_Driver/)** — *Complete 0-255 output module*

---

### 🔴 Chapter 07: Integrated 8-Bit Calculator System
> *Combining ALU, Data Bus, Registers, and BCD Displays into a functional desktop calculator.*

* **[7.1 Control Unit & Clock Generator](Chapter_07_8Bit_Calculator_System/7.1_Control_Unit_And_Clock_Generator/)** — *State machine step counter*
* **[7.2 Bus Routing & Tri-State System](Chapter_07_8Bit_Calculator_System/7.2_Bus_Routing_And_TriState_System/)** — *Shared data line isolation*
* **[7.3 Full Integrated Calculator Assembly](Chapter_07_8Bit_Calculator_System/)** — *Master integration chapter*

---

### 🟤 Chapter 08: Control Logic & Microcode
* **[8.1 Instruction Decoder](Chapter_08_Control_Logic_And_Microcode/8.1_Instruction_Decoder/)** — *Opcode demuxing*
* **[8.2 Microcode ROM Matrix](Chapter_08_Control_Logic_And_Microcode/8.2_Microcode_ROM_Matrix/)** — *Control signal lookup tables*

---

### ⚪ Chapter 09: System Bus Architecture & Timing
* **[9.1 Shared System Bus & Tri-State Buffers](Chapter_09_Bus_Architecture_And_Timing/9.1_Shared_System_Bus/)** — *Preventing signal contention*

---

### 🟣 Chapter 10: Full-Fledged 8-Bit Computer
> *A complete general-purpose stored-program computer architecture.*

* **[10.1 Fetch-Decode-Execute Cycle Unit](Chapter_10_Full_Fledged_8Bit_Computer/10.1_Fetch_Decode_Execute_Cycle/)**
* **[10.2 Program Counter (PC) & Memory Address Register (MAR)](Chapter_10_Full_Fledged_8Bit_Computer/10.2_Program_Counter_And_Memory_Mapper/)**
* **[10.3 Integrated Execution Computer Unit](Chapter_10_Full_Fledged_8Bit_Computer/)**

---

### 🚀 Scaling Beyond (Future Chapters Roadmap)

```text
├── Chapter_11_To_20  -> 16-Bit Architecture & Expanded Instruction Set
├── Chapter_21_To_40  -> 32-Bit RISC-style CPU Architecture & Pipelining
└── Chapter_41_To_100 -> 64-Bit System Design, Floating Point Units (FPU), & Cache Memory

---

## 🤝 Community & Contributions

Contributions, circuit optimizations, and documentation fixes are welcome!

* Read our [CONTRIBUTING.md](https://www.google.com/search?q=CONTRIBUTING.md) guide to submit new component designs, optimized methods, or updates.
* Check out the [IDEAS_AND_REQUESTS.md](https://www.google.com/search?q=IDEAS_AND_REQUESTS.md) board to see what circuits are currently requested.

---

*Happy wiring! Let's build a computer.* 🔌💡

```

```
