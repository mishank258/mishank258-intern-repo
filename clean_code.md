# Unit Testing Reflection
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

