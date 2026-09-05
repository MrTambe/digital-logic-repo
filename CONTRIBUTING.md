```markdown
# 🌟 Contributing to the Digital Logic Course 🌟

First off, welcome! Thank you for your interest in contributing to the **Digital Logic Course Repository**. 

This repository is built as a living, open-source educational "book" for **Sebastian Lague's Digital Logic Simulator**. Whether you are fixing a typo, adding a complex sequential circuit, or writing a tutorial on a new optimization method, your contributions help make learning digital logic accessible to everyone.

---

## 📑 Table of Contents

1. [📜 Code of Conduct](#-code-of-conduct)
2. [📖 The "Book" Philosophy](#-the-book-philosophy)
3. [🔍 What We Are Looking For](#-what-we-are-looking-for)
4. [🛠️ How to Submit a New Circuit](#️-how-to-submit-a-new-circuit)
5. [🎥 Media & Video Guidelines](#-media--video-guidelines)
6. [🚀 Pull Request (PR) Process](#-pull-request-pr-process)

---

## 📜 Code of Conduct

By participating in this project, you agree to maintain a respectful, inclusive, and collaborative environment. Constructive feedback on Pull Requests is highly encouraged; academic elitism is not. We are all here to learn and build cool computers! 🤝

---

## 📖 The "Book" Philosophy

Unlike standard code repositories, this project is structured like an **interactive textbook**. 

> **Our Golden Rule:** 
> *Do not just drop a circuit file and leave. Every component must have a beautifully formatted `README.md` that explains the theory, shows the truth table, and provides a live video demonstration.*

*   **Readability First:** Text goes at the bottom. Start with a quick hook, the visual video demo, the truth table, and *then* the deep-dive text. 
*   **Progressive Difficulty:** Chapters go from simple gates (Chapter 2) all the way up to full computer architectures (Chapter 10+). Put your contribution in the correct difficulty tier.

---

## 🔍 What We Are Looking For

We are actively accepting contributions for:

*   **🧩 New Components:** Missing logic gates, advanced ALU designs, new I/O drivers, or computer architecture components (16-bit, 32-bit, 64-bit).
*   **⚡ Alternative Methods:** Did you find a way to build a circuit with fewer gates? Less propagation delay? Submit it as a new `Method_02_...` folder alongside the standard design!
*   **📝 Documentation Fixes:** Typos, better explanations, or cleaner truth tables.

---

## 🛠️ How to Submit a New Circuit

If you have built a new component in the simulator, follow these steps to add it to the course:

### Step 1: Fork & Clone
Fork the repository to your GitHub account and clone it to your local machine.
```bash
git clone [https://github.com/your-username/digital-logic-course-repo.git](https://github.com/your-username/digital-logic-course-repo.git)

```

### Step 2: Create a Branch

Create a new branch for your circuit. Use a descriptive name!

```bash
git checkout -b feat/add-carry-lookahead-adder

```

### Step 3: Create the Folder Structure

Navigate to the correct Chapter and create a folder for your component. If there are multiple ways to build it, use the `Method_` subfolder structure.

```text
├── 4.3_8Bit_Adder/
│   ├── Method_01_Ripple_Carry/
│   │   ├── README.md
│   │   ├── circuit.json
│   │   └── media/
│   │       └── demo.mp4

```

### Step 4: Write the `README.md`

Every circuit MUST have a local `README.md`. It should include:

1. **A short introduction** (What does this chip do?)
2. **Embedded Video Demo** (See media guidelines below).
3. **The 5x2 Compact Truth Table** (Use the template in `/templates`).
4. **In-depth Theory** (How does the wiring actually work? Why did you design it this way?)

### Step 5: Commit & Push

Commit your changes with a clear message and push to your fork.

```bash
git commit -m "feat(Chapter 4): Added 8-Bit Carry Lookahead Adder method"
git push origin feat/add-carry-lookahead-adder

```

---

## 🎥 Media & Video Guidelines

We prefer **live action over static images**. Whenever possible, record a short `.mp4` video showing you toggling the inputs in the simulator and the outputs lighting up.

### 🎬 Video Rules:

* **Format:** `.mp4` only.
* **Length:** Keep it under 60 seconds. Show the most important truth-table states.
* **Framing:** Zoom in on the chip/circuit. Don't record your whole desktop.

### 🖼️ Embedding in Markdown:

Do not use raw markdown links for videos. Use the HTML `<video>` tag so it plays seamlessly inside the GitHub book:

```html
<video src="media/your_demo_video.mp4" controls="controls" style="max-width: 100%;">
  Your browser does not support the video tag.
</video>

```

---

## 🚀 Pull Request (PR) Process

Ready to submit? Head over to the main repository and open a Pull Request!

### ✅ PR Checklist (Make sure you can check these off):

* [ ] I have placed my component in the correct Chapter folder.
* [ ] I have included the simulator save file (`circuit.json`).
* [ ] I have written a detailed `README.md` following the book philosophy.
* [ ] I have included a `.mp4` video demonstrating the circuit working.
* [ ] I have included a Truth Table.

### ⏱️ Review Process:

* Maintainers will review your PR within **3-5 business days**.
* We might ask for tweaks (e.g., "Could you explain the wire routing in paragraph 2 a bit more?"). Don't be discouraged! This is how we make the book perfect.
* Once approved, your circuit will be officially merged into the course! 🎉

---

*Thank you for helping us build the ultimate digital logic guide! Happy wiring!* 🔌💡

```

```
