 # 📌 Practise React Debugging in a Test Repo
 ## What was the issue?
 The issue was that the Counter component was directly modifying a state variable instead of using the useState setter function. Specifically, count++ was used, which caused the runtime error.

## What debugging method did you use?
This indicated that a constant value was being reassigned.
Inspected the code:
I looked at the increment function in the Counter component and noticed that the state variable count was being directly modified using count++.
React documentation and DevTools:
I confirmed that state variables returned by useState are immutable and must be updated using the setter function setCount.
Trial and error:
I temporarily added console.log(count) inside the increment function to see the value changes and verify that the state was not updating correctly when modified directly.

## How did you resolve the problem?
Initially, the increment function tried to increase the count variable directly using count++. This caused an error because count is a constant returned by useState and cannot be modified directly.
To fix the problem, I used the setter function setCount provided by useState to update the state: setCount(count + 1). This is the correct way to change state in React, and it ensures the component re-renders with the updated value.

Here are the proof screenshot.
<img width="906" height="980" alt="Screenshot 2025-08-27 185531" src="https://github.com/user-attachments/assets/c7dd18b4-c352-411e-b781-56a2cae8495e" />
<img width="1230" height="978" alt="Screenshot 2025-08-27 185716" src="https://github.com/user-attachments/assets/97a92f41-0be1-468a-a974-a011fca8a1c5" />
<img width="1224" height="981" alt="Screenshot 2025-08-27 185726" src="https://github.com/user-attachments/assets/ff9fc09a-37f8-467f-a3c7-a4055fbfcd59" />
<img width="948" height="982" alt="Screenshot 2025-08-27 185805" src="https://github.com/user-attachments/assets/c5ebf6b7-bd06-4524-8a11-fee807ffa972" />
