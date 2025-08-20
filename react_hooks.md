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

## 📌 Optimizing Performance with useMemo
# How does useMemo improve performance?
useMemo improves performance by memoizing a value or calculation result. It only recalculates the value when its dependencies change. This prevents expensive calculations from running on every render, especially useful when working with large lists or heavy computations.

# When should you avoid using useMemo?
You should avoid useMemo if the calculation is cheap, the component renders infrequently, or if the value isn’t needed for optimizing performance. Using it unnecessarily can make the code more complex without any real benefit.

# What happens if you remove useMemo from your implementation?
Without useMemo, the expensive calculation will run on every render, even if the input data hasn’t changed. This can slow down your app, particularly when dealing with large datasets or heavy computations.

I created a component with a numbers array and an expensive calculation. I used useMemo to memoize the result so it only recalculates when numbers changes. I tested the component by updating unrelated state like count and saw that the calculation did not re-run, confirming that useMemo prevents unnecessary re-computation. When I removed useMemo, the calculation ran on every render, slowing down the component, which showed how useful useMemo is for performance optimization.
<img width="955" height="837" alt="image" src="https://github.com/user-attachments/assets/e8fd3d80-34c0-4e8e-ae34-a4061a2504e8" />
<img width="967" height="939" alt="image" src="https://github.com/user-attachments/assets/f73a676a-f8cd-413c-a279-ffb82a672cbe" />

## 📌 Understanding React Hooks: useEffect

# When should you use useEffect instead of handling logic inside event handlers?
useEffect should be used when you need to handle side effects tied to the component lifecycle, like fetching data on mount, subscribing to events, or updating the DOM. Unlike event handlers, which only run when a user interacts with the component, useEffect ensures that certain logic runs automatically at the right time—on mount, update, or unmount—without manual triggers.

# What happens if you don’t provide a dependency array?
If the dependency array is omitted, the effect will run after every render, which can lead to repeated API calls, unnecessary re-renders, and wasted resources. By providing dependencies, you control when the effect runs, preventing unwanted or expensive repeated executions.

# How can improper use of useEffect cause performance issues?
Improper use—like running expensive logic on every render without dependencies, or not cleaning up subscriptions/timers—can slow down your app, cause memory leaks, or trigger duplicate network requests. Using useEffect correctly ensures efficient, predictable side effect management and keeps your app responsive.

I created a React component that demonstrates the use of the useEffect hook. When the component mounts, it logs a message to the console, and when it unmounts, the cleanup function logs another message. I also added a Fetch Data button that calls an API using Axios and displays the post title dynamically in the component. This setup allowed me to observe how useEffect handles side effects tied to the component lifecycle and how cleanup functions prevent memory leaks or unwanted behavior. I tested the component by mounting, clicking the button, and unmounting it, confirming that all functionality worked as expected.
<img width="939" height="779" alt="image" src="https://github.com/user-attachments/assets/afccc007-e3be-4af0-8649-e46c9ccb3a9a" />
<img width="1038" height="798" alt="Screenshot 2025-08-20 174932" src="https://github.com/user-attachments/assets/fb8df696-d1e5-438f-bd89-be9bbfa120eb" />
<img width="799" height="480" alt="Screenshot 2025-08-20 174936" src="https://github.com/user-attachments/assets/4a1151ec-25c0-4872-a888-32716a8d3dd0" />

