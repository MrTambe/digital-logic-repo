# 📤 3.2 Demultiplexers (DEMUX)

A **Demultiplexer (DEMUX)** is the exact opposite of a multiplexer. It is a digital data distributor. Instead of funneling many inputs into one output, a DEMUX takes a single incoming data line and routes it to exactly one of several possible output lines based on the state of its "selector" inputs.

If the MUX is the CPU's funnel for gathering data, the DEMUX is the CPU's delivery system, ensuring that a specific signal (like a clock pulse or a save command) reaches the correct register without activating the others.

---

## 🎛️ 3.2.1 Basic 1-to-2 DEMUX

The 1-to-2 DEMUX has one data input ($D$), one selector input ($S$), and two possible outputs ($Y_0$ and $Y_1$). The data signal is forwarded to the selected output, while the unselected output is forced to remain OFF (`0`).

### 🔹 Component Blueprint (Logic Gates)

Building a 1-to-2 DEMUX from primitives is incredibly straightforward, relying on the fact that an AND gate only allows a signal to pass if its other input is `1`.

* **Wiring:**
1. Invert the Selector $S$ using a NOT gate to create $\overline{S}$.
2. Route $\overline{S}$ and Data $D$ into **AND Gate 1** (Outputs $Y_0$).
3. Route the original Selector $S$ and Data $D$ into **AND Gate 2** (Outputs $Y_1$).


* **Gate Depth:** `2 Ticks` (Inverter $\rightarrow$ AND)

---

## 🌲 3.2.2 The 1-to-4 DEMUX

To route a single signal to four distinct destinations ($Y_0$ through $Y_3$), we must use **two selector bits** ($S_1, S_0$).

Before building it in your logic simulator, you can interact with this visualization to understand how the binary value of the selectors determines the active path:

> **Key Insight:** Notice how changing the data toggle (`D`) *only* affects the single output line chosen by the selectors. The other three lines are locked to `0`, preventing accidental data writes to the wrong memory location.

Just like the multiplexer, a 1-to-4 DEMUX can be built by cascading three 1-to-2 DEMUX chips in a tree structure:

1. **Stage 1 (Top Layer):** The primary data signal $D$ enters **DEMUX A**, which is controlled by the high bit ($S_1$). It splits the path into a "Top Half" and a "Bottom Half".
2. **Stage 2 (Bottom Layer):**
* The "Top Half" path goes into **DEMUX B**, controlled by the low bit ($S_0$). It routes to $Y_0$ and $Y_1$.
* The "Bottom Half" path goes into **DEMUX C**, also controlled by $S_0$. It routes to $Y_2$ and $Y_3$.



---

## 🛠️ 3.2.3 Hardware Applications

### 1. Instruction Decoding

When a CPU reads an instruction like `ADD`, it arrives as a binary opcode (e.g., `1011`). The CPU feeds this opcode into the selector pins of a large demultiplexer (or a specialized decoder). The DEMUX routes an "enable" signal down a single wire that wakes up the Arithmetic Logic Unit (ALU), while keeping the rest of the CPU dormant.

### 2. Serial-to-Parallel Conversion

When data travels over long cables (like USB or Ethernet), it arrives as a single, high-speed serial stream of bits (`1-0-1-1-0...`). A DEMUX takes this single wire and, by rapidly cycling its selector pins in sync with the incoming data clock, sprays those bits into a parallel 8-bit or 16-bit array that the computer's internal buses can process simultaneously.
