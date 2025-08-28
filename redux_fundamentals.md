# 📌 Using Selectors in Redux Toolkit

## Benefits of using selectors instead of directly accessing state
Using selectors makes it easier and cleaner to access Redux state. Instead of having every component figure out the state structure, the selector knows exactly where the data lives. This helps in reusing the same logic in multiple components and keeps your code more organized. If the state structure changes later, you only need to update the selector instead of changing every component that uses the state. It also makes your components simpler because they just call the selector without worrying about the store details.

# My Demo
In my demo, I created a counter slice with a selectCount selector to get the current counter value from Redux. Then, in my Counter component, I used useSelector(selectCount) to access the counter value and display it. I also added an increment button that updates the value in the Redux store. This way, the component automatically re-renders whenever the counter value changes, showing how selectors and useSelector work together in a real app.

<img width="665" height="617" alt="Screenshot 2025-08-28 161012" src="https://github.com/user-attachments/assets/bfeb414c-3125-4938-a77e-998e92f4a3fe" />
<img width="846" height="677" alt="Screenshot 2025-08-28 161032" src="https://github.com/user-attachments/assets/2230bcc1-0109-46de-908f-816efd3c64e7" />
<img width="875" height="851" alt="Screenshot 2025-08-28 161054" src="https://github.com/user-attachments/assets/cfdd20ad-011a-4c9f-8e81-6459dd4cb64b" />
<img width="951" height="901" alt="Screenshot 2025-08-28 161143" src="https://github.com/user-attachments/assets/0ed72696-881b-42c2-b2c9-df82c25f8e9e" />
<img width="951" height="972" alt="Screenshot 2025-08-28 161335" src="https://github.com/user-attachments/assets/ddd31c3e-37da-4baa-9637-31d4117ebf87" />
