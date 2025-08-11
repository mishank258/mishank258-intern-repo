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

<img width="640" height="674" alt="image" src="https://github.com/user-attachments/assets/9447b805-9383-486c-8641-5439068d7e5e" />
As seen in this image the commit message is overly detailed. 

<img width="660" height="671" alt="image" src="https://github.com/user-attachments/assets/79ed79e3-3f38-43fd-b454-0678d646323f" />
In this image we can see the message is clearly well structured and too the point and can be easily understood with just one look.

<img width="653" height="667" alt="image" src="https://github.com/user-attachments/assets/e7cfb97a-1a6f-420f-adec-6ad65c847b50" />
In this image we can see that the commit message is vague and not able to understand that what has happend or edited in the file.

**How does a clear commit message help in team collaboration?**  
Clear commit messages make it easier for team members to read the history of the project and understand what has happened without opening every file. This helps during reviews, debugging, and discussions because everyone knows what each commit is for.

**How can poor commit messages cause issues later?**  
Bad or vague commit messages like “updated” or “fixed stuff” don’t give any real information. This makes it hard in the future to understand what was changed, why it was changed, or when a bug was added. That can waste a lot of time when other people (or even I myself later) try to track down problems or understand the code history.

<img width="860" height="460" alt="image" src="https://github.com/user-attachments/assets/2508cbef-eff4-47ef-b251-d6ab60e45b30" />
On the open source repo I found these commit messages as good as one can easily understand what is happening here and giving clear instructions on each commit. 

<img width="874" height="178" alt="image" src="https://github.com/user-attachments/assets/0d81995b-a552-461e-bfce-47b6a3afaf2b" />
Although I am not able to find a perfectly bad commit message in the repo, but according to me this commit message should be more clear and better.


### 📌 Branching & Team Collaboration

### My Branch and PR Practice
 created a branch called `pr-practice` where I made these changes. I am currently waiting to get approval to merge this branch into the main branch. Once the changes are merged and approved, I will delete the `pr-practice` branch to keep the repository clean.

### Why is pushing directly to the main branch problematic?
Pushing directly to the main branch can cause problems because it may introduce bugs or errors straight into the main code. This can affect everyone who is working on the project and cause issues for the whole team.

### How do branches help with reviewing code?
Branches allow us to work on bugs or new features separately without affecting the main code. They let team members review the changes through commit messages and pull requests before merging. This way, the main code stays safe and stable.

### What happens if two people edit the same file on different branches?
If two people edit the same file on different branches, their changes stay separate until the branches are merged. When merging, Git will check for conflicts and ask the developers to fix any overlapping changes so everything works together properly.

### 📌 Debugging with git bisect

## What does git bisect do?
Git bisect helps find the exact commit where a bug was introduced by using binary search. It asks you to mark commits as good or bad and narrows down the problem quickly.

## When would you use it in a real-world debugging situation?
You use git bisect when you know a bug exists but don't know which commit caused it. It helps find the buggy commit fast, especially when there are many commits.

## How does it compare to manually reviewing commits?
Manually checking each commit one by one takes a lot of time. Git bisect cuts the number of checks needed by half each time, so it is much faster and easier.

## Testing I Did
I created a simple Python script for addition and subtraction.  
I made several commits, then introduced bugs deliberately in these functions.  
Using git bisect, I marked commits as good or bad, tested the script output, and found the exact commit where the bug was added.  
This showed me how git bisect helps quickly find bugs in code history.
![Commit list](<Screenshot 2025-08-07 235107.png>)
![Bug found](<Screenshot 2025-08-07 235100.png>)


### 📌 Advanced Git Commands & When to Use Them
# Git Commands Reflection

## git checkout main -- <file>  
This command restores a single file from the main branch, undoing any local changes I made to that file in my current branch.  
**When to use:** If I mess up a file and want to get back the last committed version from main without touching other files.  
**Surprise:** It’s really handy to fix just one file without resetting the whole branch.

## git cherry-pick <commit>  
This applies one specific commit from another branch onto my current branch without merging all changes from that branch.  
**When to use:** When I want a bug fix or feature from a feature branch, but don’t want to merge the entire branch yet.  
**Surprise:** It creates a new commit with a different hash but same changes — and can cause conflicts like merges.
<img width="956" height="992" alt="image" src="https://github.com/user-attachments/assets/7111f28c-b01d-46fe-9c30-d347881e8127" />
As you can see here I first added a new line on file on a new branch, and then cherry picked it on the main branch. 


## git log  
Shows commit history of the current branch, including commit IDs, authors, dates and messages.  
**When to use:** To understand project history, find when changes happened, or grab commit hashes for other commands.  
**Surprise:** There are so many options to filter and format the output, which makes it really flexible.

## git blame <file>  
Shows who last changed each line in a file, including commit, author, and date info.  
**When to use:** When I want to find who wrote or last touched a specific line of code, especially useful in debugging or understanding old code.  
**Surprise:** It’s super precise and fast even on big files, and really helps track down history line by line.

---

Overall, these commands are super important for teamwork and maintaining code over time. They help manage changes carefully, avoid unnecessary merges, and understand exactly what’s happening in the codebase.

This is my testing example 
![](<Screenshot 2025-08-07 235444.png>)
![](<Screenshot 2025-08-08 133936.png>)
![](<Screenshot 2025-08-08 134544.png>)

### 📌 Merge Conflicts & Conflict Resolution
## Merge Conflicts & Conflict Resolution

**What caused the conflict?**  
Conflict was caused by commits from different branches changing the same part of the same file, so Git didn't know which change to keep.

**How did you resolve it?**  
I solved it by selecting one commit and not selecting the other using VS Code's merge conflict tools. The Git desktop client took me to VS Code to solve the conflict.

**What did you learn?**  
Merge conflicts happen when changes overlap. Using tools like VS Code makes it easy to pick which change to keep and fix conflicts quickly.

here are the screenshots of the testing.
![](<Screenshot 2025-08-08 144642.png>)
![](<Screenshot 2025-08-08 144652.png>)

### 📌 Git Concepts: Staging vs. Committing
## Staging vs Committing in Git

**What is the difference between staging and committing?**  
Staging is preparing the file with content and code for the next commit. Committing is saving those staged changes in the main repo.

**Why does Git separate these two steps?**  
Git does it in two steps to let me double check and change things before commit, so I can carefully review what goes in.

**When would you want to stage changes without committing?**  
When I’m working on many tasks at once and want to commit only some changes, or when I want to review changes before committing.

I have already attached many screenshots which shows the that I am stagging and committing the files using vs code terminal
![](<Screenshot 2025-08-08 152525.png>)
  
