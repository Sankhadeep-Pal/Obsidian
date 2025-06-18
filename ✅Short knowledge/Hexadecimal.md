# Hexadecimal Number System
The **hexadecimal number system** (or **hex**) is a **base-16** number system. That means each digit can represent **16 different values**, unlike the decimal system (base-10), which only uses 10 digits (0–9).

### Digits in Hexadecimal:
Hex uses the following **16 symbols**:
**HEX** -> 0, 1, 2, 3, 4, 5, 6, 7, 8, 9, A, B, C, D, E, F
So, after 9 comes A (10), B (11), ... up to F (15).

### Why Use Hexadecimal?
Hex is used in **computing and electronics** because:

- It's shorter and easier than writing long binary numbers.
 
- It's easy to convert between hex and binary.

- It's commonly used in **memory addresses**, **machine code**, **color codes**, and **error codes**.

### Counting in Hex:
Here’s how counting looks in hexadecimal (with decimal equivalents):

|Decimal|Hex|
|---|---|
|0|0|
|1|1|
|...|...|
|9|9|
|10|A|
|11|B|
|12|C|
|13|D|
|14|E|
|15|F|
|16|10|
|17|11|
|18|12|
|...|...|
|31|1F|
|32|20|

Just like **decimal 10** means 1 ten and 0 ones, **hex 10** means 1 sixteen and 0 ones (i.e., 16 in decimal).

---

### 🔹 Converting Between Decimal and Hex

#### 🧮 To Convert Decimal to Hex:

1. Divide the decimal number by 16.

2. Record the **remainder** (0–F).

3. Divide the **quotient** by 16.

4. Repeat until the quotient is 0.

5. Write the **remainders in reverse** order.

**Example:** Convert 26 to hex  
26 ÷ 16 = 1 remainder **10** → **A**  
1 ÷ 16 = 0 remainder **1**  
Answer: **1A**

#### 🔁 To Convert Hex to Decimal:
Multiply each hex digit by **16 to the power of its position**, from right to left.

**Example:** Convert `1A` to decimal  
`1 × 16¹` = 16  
`A × 16⁰` = 10  
Total = 16 + 10 = **26**

---