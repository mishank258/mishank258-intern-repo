# Git Pull Request Reflection

## Why are PRs important in a team workflow?

Pull Requests are important in a team because they allow the code or documents to be reviewed and discussed before they are permanently added to the main branch. This helps team members find mistakes, clear doubts, and suggest improvements. PRs make sure that more than one person looks at the changes, which improves the final quality of the project and keeps everyone aware of what is being added.

## What makes a well-structured PR?

A good PR:
- Has a clear, meaningful title
- Includes a description that explains what was changed and why
- Contains small and focused changes (not too many different things in one PR)
- Passes automated checks like builds, linting and tests
- Has clean commits and helpful extras such as screenshots or examples when needed

These elements help reviewers understand the changes easily and speed up the approval process.

## What I learned from reviewing an open-source PR

While reviewing a PR from a public project (React), I observed there are multiple tabs like **Conversation**, **Commits**, **Checks**, and **Files changed**. Reviewers leave suggestions or point out issues in the Conversation tab. The author then responds by updating their code and pushing new commits. If any checks fail (for example, tests or builds), the PR cannot be merged until the problems are fixed. I realised that this review process is very systematic and is focused on collaboration, code quality, and ensuring that everything works perfectly before it becomes part of the main project.
![alt text](image.png)

**What makes a good commit message?**  
A good commit message is short, clear, and tells exactly what was changed and why. It usually starts with an action word like *Add*, *Fix*, *Update*, or *Remove*, and gives enough information so others can quickly understand the change.

**How does a clear commit message help in team collaboration?**  
Clear commit messages make it easier for team members to read the history of the project and understand what has happened without opening every file. This helps during reviews, debugging, and discussions because everyone knows what each commit is for.

**How can poor commit messages cause issues later?**  
Bad or vague commit messages like “updated” or “fixed stuff” don’t give any real information. This makes it hard in the future to understand what was changed, why it was changed, or when a bug was added. That can waste a lot of time when other people (or even I myself later) try to track down problems or understand the code history.