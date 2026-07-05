# JIT Compilation

**JIT (Just-In-Time) compilation** is the "secret sauce" that transformed JavaScript from a slow, "toy" language into a powerhouse capable of running 3D games and complex servers.

To understand it, we have to look at the **V8 Engine** (used in Chrome and Node.Js). It doesn’t just choose between an Interpreter and a Compiler; it uses a **Multi-Tier Pipeline**.

### 1. The "Ignition" Interpreter
When you first run a script, the engine wants to start execution _immediately_. It uses an interpreter called **Ignition** to turn your source code into **Bytecode**.

- **The Benefit:** Fast startup time.

- **The Problem:** Bytecode is slower to execute repeatedly.

### 2. The Profiler (The "Watcher")
While the Bytecode is running, a **Profiler** sits in the background. It counts how many times a function is called and what types of data (integers, strings, objects) are being passed into it.

- If a function is called many times, it’s marked as **"Hot."**

### 3. The "TurboFan" Optimizing Compiler
Once a function is "Hot," the engine passes it to **TurboFan**. This compiler takes the Bytecode and transforms it into **Highly Optimized Machine Code** (binary) that the CPU can execute directly at blazing speeds.

---

### The "Small Detail": Speculative Optimization

Here is the detail that will increase your knowledge base: **Deoptimization.**

JIT compilers make "speculative" guesses. If you call a function `add(a, b)` 1,000 times with integers, TurboFan assumes `a` and `b` will _always_ be integers and produces machine code specifically for integer math.

**The "Gotcha":** If, on the 1,001st call, you pass a string— `add("1", 2)` —the optimized machine code fails because it doesn't know how to handle strings. The engine has to **"Deoptimize"**: it throws away the fast machine code and falls back to the slow Bytecode interpreter.

> **Pro-Tip:** This is why "Type Stability" matters. Writing functions that always receive the same shapes of data helps the JIT compiler keep your code in the "fast lane."

---
