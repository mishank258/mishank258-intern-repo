## 📌 Handling Forms with Formik
<img width="916" height="970" alt="Screenshot 2025-08-20 170349" src="https://github.com/user-attachments/assets/3bed0bf7-c3a4-4bc2-83e0-ef56a2187360" />
<img width="886" height="824" alt="Screenshot 2025-08-20 170357" src="https://github.com/user-attachments/assets/59a8910e-a231-43b7-bb56-b1b7943733a2" />
<img width="833" height="488" alt="Screenshot 2025-08-20 170407" src="https://github.com/user-attachments/assets/a7147743-09a2-45b0-b97a-0b6f1f67918a" />
<img width="621" height="301" alt="Screenshot 2025-08-20 170452" src="https://github.com/user-attachments/assets/4d369bbd-e665-4b93-89e7-5a2a5703f4a6" />
<img width="813" height="503" alt="Screenshot 2025-08-20 170502" src="https://github.com/user-attachments/assets/85296f76-6fbb-4efb-bf67-61d912924552" />

# How does Formik simplify form management compared to handling state manually?
Formik automatically manages form state (values, touched fields, errors) so you don’t have to manually write useState for each input. It also handles onChange, onBlur, and onSubmit events, which reduces boilerplate code and makes the form easier to maintain.

# What are the benefits of using Formik’s validation instead of writing validation logic manually?
Formik works well with Yup, allowing you to define schema-based validation. This keeps validation consistent, reusable, and readable. Without Formik/Yup, you would need to manually check each field, manage error messages, and handle edge cases, which can be error-prone and hard to maintain.

# My Experience
In this experiment, I created a React form using Formik to manage form state and validation efficiently. I started by installing Formik and Yup, then created a form component with Name and Email fields. Using Formik’s useFormik hook, I set up initial values, submission handling, and validation rules. Yup was used to define a validation schema that ensures the Name is required and the Email is in a valid format. I then integrated this form component into App.js and ran the app. During testing, I verified that validation errors appear when inputs are empty or invalid, and that submitting valid data works correctly. This experiment helped me understand how Formik simplifies form state management, validation, and submission in React.
