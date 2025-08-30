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

# 📌 Mocking API Calls in Jest
## Why is it important to mock API calls in tests?
Mocking API calls is important because it lets me test how my components behave without actually hitting a real server. This makes tests faster, more reliable, and safe, especially when dealing with sensitive data or when the API isn’t ready yet.

## What are some common pitfalls when testing asynchronous code?
Some common pitfalls when testing asynchronous code are forgetting to wait for the data to load, not handling promises correctly, or tests passing before the async code finishes. This can lead to flaky tests that sometimes fail even if the code works fine.

For the demo, I created a React component that fetches data from a fake API. In the test, I used jest.mock() to replace the real API call with a mock function that returns sample data. Then I checked that the component correctly displayed the mocked data without making an actual network request. This way, I verified the component’s behavior safely and quickly.
<img width="868" height="251" alt="Screenshot 2025-08-30 144806" src="https://github.com/user-attachments/assets/4df3af19-faf4-4857-b5af-5abda1929c97" />
<img width="1099" height="771" alt="Screenshot 2025-08-30 144816" src="https://github.com/user-attachments/assets/e7f276e2-a288-4337-91ae-5ede88349b17" />
<img width="982" height="626" alt="Screenshot 2025-08-30 144837" src="https://github.com/user-attachments/assets/a2c584ed-afa4-4847-a6da-2ff461f93e92" />

# 📌 Introduction to Unit Testing with Jest
## Why is automated testing important in software development?
Automated testing is super important because it helps catch bugs early, prevents breaking existing features when updating code, and makes sure the app stays stable. It also saves time in the long run since you don’t have to manually check everything every time you make a change.

## What did you find challenging when writing your first Jest test?
The trickiest part was figuring out how to structure the test properly, especially understanding how Jest expects functions and values to be tested. It took some trial and error to write tests that actually check what they are supposed to, like verifying return values or mocking functions correctly.

Demo of what I did:
I created a simple utility function that adds two numbers and then wrote a Jest test to check if it returns the correct sum. I ran the test in the terminal and confirmed that it passes, showing that my first unit test works as expected.
<img width="867" height="408" alt="Screenshot 2025-08-30 145728" src="https://github.com/user-attachments/assets/a153bf75-086c-4e16-8c90-263410815807" />
<img width="679" height="458" alt="Screenshot 2025-08-30 145735" src="https://github.com/user-attachments/assets/06c54181-1a67-4b80-bc3d-588e6b6757ff" />
<img width="763" height="345" alt="Screenshot 2025-08-30 145743" src="https://github.com/user-attachments/assets/d6df92b8-bc7f-4802-8728-8d36a590e0eb" />

