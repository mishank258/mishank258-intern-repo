## 📌 Preventing Unnecessary Renders with useCallback
# What problem does useCallback solve?
useCallback helps prevent unnecessary re-renders in React. Normally, when a parent component updates, any functions inside it are recreated. If a child component receives that function as a prop and is wrapped with React.memo, it will re-render even if nothing actually changed. useCallback keeps the function reference the same across renders, so the child only re-renders when needed.

# How does useCallback work differently from useMemo?
useCallback memoizes a function, keeping its reference stable across renders. useMemo, on the other hand, memoizes a value or the result of a calculation. So useCallback is for functions, and useMemo is for values.

# When would useCallback not be useful?
useCallback is not needed if the function is simple, cheap to recreate, or not passed to a memoized child component. In these cases, using it just adds extra complexity without improving performance.

# My Experiment
I created a parent component with a count state and a child component wrapped with React.memo. I passed a function from the parent to the child as a prop. First, I used useCallback and saw that the child did not re-render when the count changed. Then, I removed useCallback and noticed the child re-rendered every time the parent updated. This showed me how useCallback can prevent unnecessary renders and improve performance in React apps.
<img width="951" height="913" alt="Screenshot 2025-08-20 171943" src="https://github.com/user-attachments/assets/f8337252-dccf-4bb6-b5f0-3a273b00a36a" />
<img width="857" height="874" alt="Screenshot 2025-08-20 172002" src="https://github.com/user-attachments/assets/f7639d21-9b7e-4af1-aa57-5d3f567366a2" />
<img width="933" height="647" alt="Screenshot 2025-08-20 172010" src="https://github.com/user-attachments/assets/370df1ad-59b5-4dda-80e4-76751d713f51" />
