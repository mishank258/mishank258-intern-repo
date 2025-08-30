# 📌 Testing Redux with Jest
## What was the most challenging part of testing Redux?
The most challenging part of testing Redux was understanding how reducers work as pure functions. At first, I was thinking in terms of UI, but in Redux you just feed state + action and check the new state. Once I got that, it felt easy.

## How do Redux tests differ from React component tests?
Redux tests differ from React component tests because they don’t involve rendering or the DOM. Component tests are about what shows up on the screen, but Redux tests are only about state changes and making sure actions dispatch correctly.

I tested the counter reducer by checking if state updated when actions like increment and incrementByAmount were dispatched. For async, I mocked dispatch and confirmed that incrementAsync eventually called the right action with the value I passed.

<img width="865" height="766" alt="Screenshot 2025-08-30 142157" src="https://github.com/user-attachments/assets/9b72debd-d899-481d-b6c4-26e30acb060c" />
<img width="844" height="803" alt="Screenshot 2025-08-30 142309" src="https://github.com/user-attachments/assets/8644b15e-0634-41ef-9ea7-34a8b2bc66c4" />
<img width="1099" height="962" alt="Screenshot 2025-08-30 142934" src="https://github.com/user-attachments/assets/9b538604-a0d6-4ecd-8cd2-fe2f81ee4dfe" />
<img width="1113" height="917" alt="Screenshot 2025-08-30 142947" src="https://github.com/user-attachments/assets/11d801b3-9945-4e42-a111-31669c8b26e9" />
