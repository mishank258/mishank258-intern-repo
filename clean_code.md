# Unit Testing Reflection
### How do unit tests help keep code clean?
Unit tests verify that individual functions work as expected, catching bugs early before they affect the whole program. They make refactoring safer and encourage writing modular, maintainable code. In my case, the tests quickly revealed that my `add` and `subtract` functions were incorrect, helping me fix them before further use.

### What issues did you find while testing?
During testing, I discovered that the `add` function was actually subtracting, and the `subtract` function was adding numbers. These logical errors were caught by the unit tests, demonstrating how important it is to test code even if it seems simple.
As you can see clearly in the screenshots about the failed and passed checks. 
<img width="1919" height="1008" alt="Screenshot 2025-08-12 175223" src="https://github.com/user-attachments/assets/7688443e-abbb-49fa-8067-e212bafd30b1" />
<img width="1273" height="578" alt="Screenshot 2025-08-12 175231" src="https://github.com/user-attachments/assets/a7db1907-e3f4-417a-9517-f80a0591ddd9" />
<img width="1821" height="932" alt="Screenshot 2025-08-12 175327" src="https://github.com/user-attachments/assets/2274fcb2-13f7-4c30-b871-ed857b6fb4f3" />

