# CI/CD Reflection

### What is the purpose of CI/CD?
CI/CD helps automate code integration and deployment, allowing errors to be caught early and ensuring the final product is delivered smoothly without issues. Continuous Integration (CI) automatically merges code changes into the repository and verifies them with tests. Continuous Deployment (CD) runs deployment tests before releasing to production or staging environments.
### How does automating style checks improve project quality?
Automated style checks keep code and docs consistent and error-free, reducing manual mistakes and making projects easier to maintain.

### What are some challenges with enforcing checks in CI/CD?
Too many strict checks can slow development and frustrate developers. Managing tool configurations and false positives is also challenging.

### How do CI/CD pipelines differ between small projects and large teams?
Small projects use simple pipelines with basic tests, while large teams have complex workflows with multiple stages, approvals, and integrations.

### My Experience with PR Testing and Commits
I set up Husky pre-commit hooks to run markdown lint and spell checks locally. These hooks prevented commits with errors. I also created a GitHub Actions workflow that runs these checks automatically on pull requests. When I opened a test PR, I reviewed the automated checks and fixed issues before merging. This process helped ensure clean, consistent documentation and improved my confidence in the CI/CD setup.
As in the screenshots.
<img width="1889" height="1009" alt="Screenshot 2025-08-12 173636" src="https://github.com/user-attachments/assets/4750981c-9377-4ba5-ae83-847f21df4d8d" />
<img width="1826" height="1004" alt="Screenshot 2025-08-12 173612" src="https://github.com/user-attachments/assets/43a8fc0c-fdfb-44ce-88b3-3282e60261a0" />
<img width="1904" height="874" alt="Screenshot 2025-08-12 173455" src="https://github.com/user-attachments/assets/00de91fd-1510-43f2-b34f-97b631d1eff3" />

