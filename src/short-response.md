# Short Response Questions

## Question 1: Promise States

What are the three states of a Promise? For each state, explain what it represents and which Promise method (`.then()` or `.catch()`) is used to handle it.

The 3 states of a promise are `pending`, `resolved`, `rejected`. ***Pending*** represents the function is in progress, ***resolved*** is the operation is fully completed, rejected means the function failed and we got an error. A ***Promise*** starts pending, becomes fulfilled and triggers `.then()` on success, or becomes rejected and triggers `.catch()` on failure.



## Question 2: Callback Hell vs. Promise Chaining

Explain why deeply nested callbacks (callback hell) are problematic, and describe how Promise chaining with `.then()` solves this problem.

The reason `nested callbacks` are problematic is because the functions become messy with the ***indentation***. When we use promise chaining with `.then()`, we optimize our code with less indentations and easy to read and it becomes easier to follow code.



## Question 3: Error Handling with `.catch()`

If you have a chain of three `.then()` calls followed by a single `.catch()`, and the second `.then()` throws an error, what happens? Why is this behavior useful?

**Your Answer:**
If you have a chain of three`then()`'s, the **1st** set of `.then()`'s will be evaluated but the error will be caught but won't cause the whole entire program to crash or terminate. The program stops the rest of the .then() chain and jumps directly to the `.catch()` which handles the error. The last `.then()` doesn't run.
The computer will still complete the program with the beginning parts of the program.

This allows errors to be handled in a **central** place without affecting the rest of the program, keeping asynchronous code clean, predictable, and easier to debug.