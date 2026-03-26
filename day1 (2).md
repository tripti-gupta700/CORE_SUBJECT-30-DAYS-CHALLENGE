# Day 1 — Introduction to Programming: Types of Languages, Memory Management

> **DSA Partner Challenge** | Week 1: Language Basics + Maths for DSA

**Notes Link: https://drive.google.com/file/d/1G1zdQu4eKHAq034zREECFS_Qu6Msr5Wd/view?usp=sharing

---

## 📌 Topic of the Day

**Introduction to Programming — Types of Languages, Memory Management & Flow of Programs**

Before you write a single line of DSA code, you need to know how languages work, how memory is managed, and how your program flows. This is the mental model everything else is built on.

---

## 🎥 Resources

### Part 1 — How Programming Languages Work + Basics
- **Primary (Java):** [Kunal Kushwaha — Introduction & How Java Works](https://youtu.be/wn49bJOYAZM?si=a9WxfRl4gxRHu-VN)
  - Covers: JVM, JDK, JRE, how .java becomes executable, memory basics, syntax intro
- **Python users:** Go through your old notes or a quick Python basics revision video on YouTube
- **C++ users:** Go through your old notes or a quick C++ basics revision video on YouTube

> All three languages share the same concepts — variables, types, conditions. Syntax changes, not the logic.

### Part 2 — Flow of a Program
- **All languages:** [Flow of a Program](https://youtu.be/lhELGQAV4gg?si=L1XVBP-yyFuHMtyg)
  - Covers: how code executes step by step, call stack, what happens inside memory when a program runs

---

## 🧠 What to Learn Today

> Only what's covered in the two videos above. Don't go beyond this today.

### What are Programming Languages
- A way for humans to give instructions to a machine
- Humans can't talk in binary — languages are the bridge
- Gets translated to machine code (0s and 1s) one way or another

### Types of Languages

**Procedural Language**
- Code runs step by step, top to bottom, in a defined procedure
- Examples: C, Pascal
- You tell the computer exactly what to do and in what order

**Functional Language**
- Built around functions — everything is a function call
- Avoids changing state or mutable data
- Examples: Haskell, Erlang (parts of Scala, JavaScript too)

**Object Oriented Languages**
- Organises code around objects — bundles of data + behaviour
- Examples: Java, Python, C++
- Core pillars: Encapsulation, Inheritance, Polymorphism, Abstraction

### Different Languages Can Be of Different Types
- Python is both procedural AND object-oriented
- JavaScript is functional AND object-oriented AND procedural
- A language isn't limited to one paradigm — it's about what it supports

### Static vs Dynamic Languages

**Static Languages**
- Type of a variable is known at compile time
- You must declare the type: `int x = 5;`
- Examples: Java, C, C++
- Errors caught early — before the program runs

**Dynamic Languages**
- Type is figured out at runtime
- No need to declare type: `x = 5` (Python just figures it out)
- Examples: Python, JavaScript, Ruby

### Errors in Static Languages
- Type errors caught at **compile time** — won't even run if types are wrong
- Safer for large codebases — bugs surface early
- Example: assigning a string to an int variable → compiler rejects it

### Errors in Dynamic Languages
- Type errors only appear at **runtime** — when that line actually executes
- More flexible but can fail unexpectedly in production
- Example: passing wrong type to a function — no warning until it crashes

### Stack and Heap Memory
- When a program runs, it gets two regions of memory: Stack and Heap
- **Stack:** stores primitive variables and function call frames — fixed size, very fast, automatically cleaned when function exits
- **Heap:** stores objects and dynamically created data — larger, slower, manually or automatically managed
- Stack is LIFO — last in, first out (like a stack of plates)
- Each function call adds a "frame" to the stack; when function returns, frame is removed

### Objects (Not Primitives!) and Reference Variables
- Primitives (`int`, `char`, `boolean` etc.) are stored directly on the stack
- Objects are stored on the **heap** — the variable on the stack just holds a **reference** (memory address) to where the object lives
- Two reference variables can point to the same object — changing one affects the other
- Example: `int a = 5` → value lives on stack. `Dog d = new Dog()` → Dog object lives on heap, `d` holds its address

### Important Memory Example
- `int a = 10;` → value `10` stored on stack under name `a`
- `int b = a;` → value is **copied** — `b` gets its own `10`
- `Dog d1 = new Dog();` → object on heap, `d1` holds reference
- `Dog d2 = d1;` → `d2` holds the **same reference** — both point to the same Dog
- Change `d2.name` → `d1.name` also changes (same object!)

### Garbage Collection
- In Java/Python: Garbage Collector (GC) automatically frees heap memory when objects are no longer referenced
- When no variable points to an object, GC marks it for deletion
- In C/C++: you are responsible — `free()` / `delete` — no GC
- GC prevents memory leaks but you can't control exactly when it runs

### Flow of Programs
- Code executes top to bottom, left to right unless redirected
- Function call → execution jumps to that function, runs it, returns back
- Call Stack tracks the current chain of function calls — push on call, pop on return
- Only one function is actually "running" at any moment (single-threaded)
- Stack Overflow = call stack grows too large (usually: infinite/deep recursion)
- Conditionals create branches — only one branch executes per run
- Loops redirect flow backwards, repeating a block until condition fails

---

## 💻 Practice Questions

> Today's practice is different — no coding yet. Think like a programmer first.

### Create a flowchart AND write pseudocode for each:

**1. Leap Year Check**
Input a year. Find whether it is a leap year or not.
- Leap year if: divisible by 4, AND (not divisible by 100 OR divisible by 400)

**2. Sum of Two Numbers**
Take two numbers as input and print their sum.

**3. Multiplication Table**
Take a number as input. Print its multiplication table (1 to 10).

**4. HCF and LCM**
Take 2 numbers as input. Find and print both their HCF and LCM.
- Hint: LCM(a, b) = (a × b) / HCF(a, b)

**5. Sum Until 'x'**
Keep taking numbers as input till the user enters `x`. After that, print the sum of all numbers entered.

---

> 💡 **Pseudocode example** for Q2:
> ```
> START
>   READ number1
>   READ number2
>   sum = number1 + number2
>   PRINT sum
> END
> ```

> 💡 **Flowchart shapes:** Oval = start/end, Rectangle = action, Diamond = decision, Arrows = flow

---

## ✅ Checklist Before You Sleep

- [ ] Watched both videos fully
- [ ] I can name at least 3 types of programming languages and give an example of each
- [ ] I understand the difference between static and dynamic languages
- [ ] I know where type errors are caught in each (compile time vs runtime)
- [ ] I can explain the difference between Stack and Heap memory
- [ ] I know why objects use reference variables and primitives don't
- [ ] I understand the d1 = d2 reference trap (both point to same object)
- [ ] I know what Garbage Collection is and which languages have it
- [ ] I can trace the flow of a simple program using the Call Stack mental model

---

## 💬 Community

Share your flowcharts and pseudocode — photo of paper is absolutely fine.

**Done all 5? Drop a 🔥 in the community.**

---

*Next up → Day 2: Writing Your First Programs*
