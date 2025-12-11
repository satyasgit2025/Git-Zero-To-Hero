Task: Create a New GitHub Repository Using Git Bash & GitHub CLI

This document explains the correct steps to initialize a local Git repository, create a new GitHub repository using GitHub CLI, link them, and push your code. All commands are shown with explanations and sample outputs.

1. Create Project Directory
```
mkdir Git-Zero-To-Hero
cd Git-Zero-To-Hero
pwd
```
Output:
/c/Users/9198746/Git-Zero-To-Hero

Explanation:
A new folder is created for the project, and you move into that directory.

2. Initialize a Local Git Repository
```
git init
```
Output:
Initialized empty Git repository in C:/Users/Git-Zero-To-Hero/.git/

Explanation:
This converts your folder into a Git repository.

3. Create Your First File
```
vi TResolution.txt
```
Explanation:
You create a file to store documentation.

4. Stage and Commit Files
```
git add .
git commit -m "Initial commit - Added TResolution.txt"
```
Output:
[master (root-commit) 2fce731] Initial commit - Added TResolution.txt
 1 file changed, X insertions(+)
 create mode 100644 TResolution.txt

Explanation:
git add . stages all files, and git commit saves them into Git history.

5. Authenticate GitHub CLI
```
gh auth login
```
Questions and answers:
? Where do you use GitHub? GitHub.com
? Preferred protocol? HTTPS
? Authenticate Git with your GitHub credentials? Yes
? How would you like to authenticate? Paste an authentication token

Paste the token you created with required scopes:

Required scopes:

repo

read:org

workflow

public_repo

Output:

✓ Configured git protocol
✓ Logged in as ussrid will be show

Explanation:
GitHub CLI is now authenticated with your GitHub account.

6. Create GitHub Repository via CLI
```
gh repo create Git-Zero-To-Hero --public
```
Output:
✓ Created repository userid/Git-Zero-To-Hero on github.com
  https://github.com/userid/Git-Zero-To-Hero


Explanation:
This command creates the GitHub repository but does not add a remote automatically.

7. Add Remote Origin (Link Local Repo to GitHub)
```
git remote add origin https://github.com/userid/Git-Zero-To-Hero.git
git remote -v
```

Output:
origin  https://github.com/userid/Git-Zero-To-Hero.git (fetch)
origin  https://github.com/userid/Git-Zero-To-Hero.git (push)

Explanation:
Remote origin is now set so your local repo knows where to push.

8. Switch Branch Name to main (optional but recommended)
```
git branch -M main
```
Explanation:
GitHub uses main as default branch.

9. Push Code to GitHub
```
git push -u origin main
```

Output:
Enumerating objects: 3, done.
Counting objects: 100% (3/3), done.
Writing objects: 100% (3/3), 237 bytes | 118.00 KiB/s, done.
Total 3 (delta 0), reused 0 (delta 0)
To https://github.com/userid/Git-Zero-To-Hero.git
 * [new branch]      main -> main
branch 'main' set up to track 'origin/main'.

Explanation:
Your project is now successfully uploaded to GitHub.

Final Summary
Step	Description
1	Created project folder
2	Initialized Git
3	Created documentation file
4	Committed changes
5	Logged in with GitHub CLI
6	Created GitHub repo using CLI
7	Added remote origin
8	Renamed master → main
9	Successfully pushed repository

Your repository is now live at:
https://github.com/userid/Git-Zero-To-Hero
