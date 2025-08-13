# 📌 Unit Testing Reflection
### How do unit tests help keep code clean?
Unit tests verify that individual functions work as expected, catching bugs early before they affect the whole program. They make refactoring safer and encourage writing modular, maintainable code. In my case, the tests quickly revealed that my `add` and `subtract` functions were incorrect, helping me fix them before further use.

### What issues did you find while testing?
During testing, I discovered that the `add` function was actually subtracting, and the `subtract` function was adding numbers. These logical errors were caught by the unit tests, demonstrating how important it is to test code even if it seems simple.
As you can see clearly in the screenshots about the failed and passed checks. 
<img width="1919" height="1008" alt="Screenshot 2025-08-12 175223" src="https://github.com/user-attachments/assets/7688443e-abbb-49fa-8067-e212bafd30b1" />
<img width="1273" height="578" alt="Screenshot 2025-08-12 175231" src="https://github.com/user-attachments/assets/a7db1907-e3f4-417a-9517-f80a0591ddd9" />
<img width="1821" height="932" alt="Screenshot 2025-08-12 175327" src="https://github.com/user-attachments/assets/2274fcb2-13f7-4c30-b871-ed857b6fb4f3" />

# 📌 Handling Errors & Edge Cases
**What was the issue with the original code?**  
The original code did not check for invalid inputs or handle errors like division by zero. This meant that if the user entered bad data, the program would stop working and show an error.

**How does handling errors improve reliability?**  
By adding error handling, the program can catch problems before they cause a crash. It can then show a helpful message to the user and continue running. This makes the program more stable, easier to use, and less likely to fail unexpectedly.

Here are the screenshots of before and after the error handling:
<img width="943" height="963" alt="Screenshot 2025-08-13 162334" src="https://github.com/user-attachments/assets/9652a3e0-617d-4f18-9c62-a00a5899470a" />
<img width="1010" height="972" alt="Screenshot 2025-08-13 162536" src="https://github.com/user-attachments/assets/86f22e47-afce-44aa-9787-7c2eb0327cb0" />

**Research and techniques used:**  
- **Validation:** Checking inputs before using them.  
- **Guard Clauses:** Stopping execution early if inputs are invalid.  
- **Try-Catch:** Catching exceptions and handling them to avoid crashes.  
- **Fallback Defaults:** Providing safe default values if something is missing. 
These strategies together improve the reliability, readability, and maintainability of the code.

# 📌 Commenting & Documentation
**When should you add comments?**  
Add comments when the code isn’t easy to understand or when you need to explain why something is done. Use docstrings for functions and classes to show how to use them.

**When should you avoid comments and instead improve the code?**  
Skip comments if the code can explain itself with clear variable and function names, or by making the logic simpler. Don’t use comments to fix messy code.

Here are screenshots no comments vs good way of commented 
<img width="1006" height="743" alt="image" src="https://github.com/user-attachments/assets/7cbf786d-8ae4-4d29-96f8-016fb1eaef8d" />
<img width="1919" height="664" alt="image" src="https://github.com/user-attachments/assets/1dfabea0-8a3a-45f7-984d-d24f2b6d8061" />

# 📌 Refactoring Code for Simplicity

**What made the original code complex?**  
The original code had a long function that did many things at once, with unclear variable names and some repeated code. It was hard to read and understand what each part was doing.

**How did refactoring improve it?**  
Refactoring broke the code into smaller, simpler functions, gave variables and functions clear names, and removed duplicate code. Now the code is easier to read, understand, and maintain.

**Research:**  
Refactoring improves code readability and maintainability. Key techniques include:
- Extracting functions to reduce complexity.
- Renaming variables and functions for clarity.
- Removing duplicate code by reusing existing functions.

Example screenshot is here:
<img width="919" height="973" alt="Screenshot 2025-08-13 182448" src="https://github.com/user-attachments/assets/cf8a49e9-1409-418f-a0b1-2d09877d4016" />
<img width="848" height="963" alt="Screenshot 2025-08-13 182527" src="https://github.com/user-attachments/assets/5be532c3-3dbe-4904-82d1-db6fed71c4e6" />

# 📌 Avoiding Code Duplication
**Issues with Duplicated Code:** Repeating the same code in multiple places makes it harder to update, increases the chance of bugs, and reduces readability.

**How Refactoring Improved Maintainability:** By putting repeated logic into functions, the code became shorter, easier to read, and simpler to modify or fix in the future.
DRY Principle: Don’t Repeat Yourself. Instead of writing the same logic multiple times, you put it into a function and call it wherever needed. This makes the code shorter, cleaner, and easier to maintain. Extract Function is one way to implement DRY—you break repeated or complex code into smaller, reusable functions.
Here is the example code screenshot:
<img width="905" height="977" alt="Screenshot 2025-08-13 184417" src="https://github.com/user-attachments/assets/a7bc04aa-299a-48e9-ba82-0caf9a1acd55" />
<img width="931" height="990" alt="Screenshot 2025-08-13 184505" src="https://github.com/user-attachments/assets/f60e9fda-457a-401d-b9ca-36221fc42e8f" />

# 📌 Writing Small, Focused Functions
**Why is breaking down functions beneficial?**  
Breaking the code into smaller parts makes it easier to read, understand, and test. Each function doing a single thing makes it reusable.

**How did refactoring improve the structure of the code?**  
Breaking a long function into smaller ones made the code cleaner, more readable, and allowed individual parts to be modified or tested without affecting the rest.

### Research: Best Practices for Small, Single-Purpose Functions
- **Do one thing at each function (Single Responsibility):** Each function should perform only one task.  
- **Keep it short:** Functions should be concise and focused.  
- **Use clear names:** Function names should explain exactly what they do.  
- **Testable:** Functions should be easy to test independently.  
- **Reuse code:** Avoid duplication by using functions wherever the same logic is needed.
All these practices can be seen I applied into the example.
<img width="1624" height="499" alt="image" src="https://github.com/user-attachments/assets/1d04f341-ccee-4885-a03e-f8789b7e231e" />
<img width="1418" height="761" alt="image" src="https://github.com/user-attachments/assets/a9666dc8-d0f7-4dfd-b5eb-d79480e8c05d" />

# 📌 Naming Variables & Functions
## What makes a good variable or function name?
A good name is descriptive and specific, follows consistent naming conventions, avoids unnecessary abbreviations, uses nouns for variables and verbs for functions, and stays concise yet meaningful.

## What issues can arise from poorly named variables?
They can cause confusion, slow down understanding, increase debugging difficulty, and lead to accidental misuse of code.

## How did refactoring improve code readability?
By replacing unclear names with descriptive ones, the code became easier to read, understand, and maintain without needing to inspect every line.

## Best Practices:
- Be descriptive and specific – names should clearly show intent.
- Follow consistent naming conventions.
- Avoid abbreviations unless they are widely known.
- Use nouns for variables and verbs for functions.
- Keep named concise but meaningful, avoiding cryptic or unnecessarily long names.
Here is an example of a simple code:
<img width="947" height="966" alt="Screenshot 2025-08-13 230200" src="https://github.com/user-attachments/assets/308866dc-3b37-4514-96bd-67fc1b8d3047" />
<img width="943" height="964" alt="Screenshot 2025-08-13 230249" src="https://github.com/user-attachments/assets/79a3116f-e52b-4558-89d9-0b092ebfbc96" />














