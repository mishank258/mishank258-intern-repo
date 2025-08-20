## 📌 Making API Calls with Axios
# Here are the screenshot of code and the required testing of axios:
<img width="878" height="857" alt="Screenshot 2025-08-20 153758" src="https://github.com/user-attachments/assets/0fcb9234-95b0-4195-a666-4bd1d1765dcf" />
<img width="927" height="870" alt="Screenshot 2025-08-20 153849" src="https://github.com/user-attachments/assets/9d544612-30ff-4b26-83e8-91c3c5992b38" />
<img width="860" height="787" alt="Screenshot 2025-08-20 153858" src="https://github.com/user-attachments/assets/9134b3e1-0689-4b9d-b7ea-7b168f59571c" />
<img width="945" height="698" alt="Screenshot 2025-08-20 154322" src="https://github.com/user-attachments/assets/bc945225-87dd-4fe4-aab8-078348e1ae3c" />
<img width="942" height="665" alt="Screenshot 2025-08-20 154331" src="https://github.com/user-attachments/assets/3472b0cb-8506-451a-a12a-f2d942b8d4bb" />
<img width="620" height="308" alt="image" src="https://github.com/user-attachments/assets/f7223f55-6710-4596-b1cb-28583fcfc4a2" />

# Reflection
# Why is it useful to create a reusable Axios instance?
Creating a reusable Axios instance is useful because it makes the code cleaner and easier to manage. It centralizes the configuration for all API requests, such as the base URL, default headers, and timeout settings. This way, you don’t have to repeat the same setup in every component, which reduces errors and makes the code more maintainable.

# How does intercepting requests help with authentication?
Request interceptors let you modify API requests before they are sent. In this project, the interceptor retrieves the authentication token from localStorage and automatically attaches it to the Authorization header. This ensures that all requests requiring authentication are handled consistently, without writing the same code in multiple components. Interceptors can also be used for logging requests, adding unique request IDs, or handling errors globally.

# What happens if an API request times out, and how can you handle it?
If an API request takes longer than the configured timeout, Axios throws a timeout error. Without handling it, the app could appear unresponsive. In this project, we handle timeouts in the catch block and display a message like "Request timed out!". This allows the app to fail gracefully, informs the user or developer, and optionally allows retrying the request. Using AbortController also lets us manually cancel requests, which helps free resources and improve performance.
I created a React project and set up a reusable Axios instance to make API calls. I tested a POST request to https://jsonplaceholder.typicode.com/posts using a TestRequest component. I also implemented request cancellation with AbortController and handled timeouts to see how Axios responds. I observed the response data, cancellation logs, and timeout handling in the browser console to understand how Axios works in a real React application.

