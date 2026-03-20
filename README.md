## Q1.Suppose you are working in a team and have to create a branching strategy where only the release branch goes to the UAT environment. Can you walk me through the commands you would use from cloning to pushing? 

In our team, we use different branches for different stages. First, I clone the project and create a feature branch to work on my task. After completing it, I push it and merge it into the develop branch.

When everything is ready for testing, we create a release branch from develop. Only this release branch is connected to the UAT environment. So when we push this branch, it automatically gets deployed to UAT.

If any bugs are found, we fix them in the release branch itself. Once everything is approved, we merge the release branch into the main branch.

```bash

⚙️ Step-by-Step Commands (From Start to End)
🧩 1. Clone the Repository
git clone https://github.com/org/repo.git
cd repo
🌿 2. Create Feature Branch
git checkout -b feature/login

👉 Work on your code

✅ 3. Commit Changes
git add .
git commit -m "Added login feature"
🚀 4. Push Feature Branch
git push origin feature/login

👉 Create PR → merge into develop

🔀 5. Switch to Develop Branch
git checkout develop
git pull origin develop
🟡 6. Create Release Branch (For UAT)
git checkout -b release/v1.0
📤 7. Push Release Branch
git push origin release/v1.0

👉 This branch is connected to UAT deployment pipeline

🛠️ 8. Bug Fixes in Release
git add .
git commit -m "Fix bug in login"
git push origin release/v1.0

👉 UAT gets updated automatically

🔁 9. After UAT Approval

Merge release → main:

git checkout main
git pull origin main
git merge release/v1.0
git push origin main
🔄 10. Sync Back to Develop
git checkout develop
git merge release/v1.0
git push origin develop

```

---


## Q2. What is git fatch, git revert ,and git pull 

- git fetch is used to download changes from the remote repository without modifying the local code.
- git pull downloads and merges those changes into the current branch.
- git revert is used to undo a specific commit by creating a new commit,

---

## Q3. git reset vs revert

- git reset removes commits from history.

---

Q 1 What is Git?
Git is a version control system used to track changes in source code.
It helps developers manage code, collaborate with teams, and maintain version history efficiently.
Q 2 What is a repository in Git?
A Git repository is a storage location that contains a project’s code and its complete version history.
It allows developers to track changes, collaborate with others, and manage source code efficiently.
Q 3 What is the difference between Git and GitHub?
Git is a version control system used to track changes in code, while GitHub is an online platform
used to host and share Git repositories.
Git works locally, and GitHub helps teams collaborate using Git.
Q 5 What is origin in Git?
In Git, origin is the default name given to the remote repository.
It acts as a shortcut for the repository URL and is commonly used when pushin
Q 6 git fetch vs git pull
git fetch downloads the latest changes from the remote repository without modifying the local
branch, while git pull downloads the changes and automatically merges them into the local branch.
Q7 What is the purpose of the .gitignore file?
The .gitignore file is used to specify which files and directories Git should ignore and not track.
It helps keep the repository clean by excluding unnecessary or sensitive files.
Q 8 What is a version control system (VCS)?
A Version Control System is a tool used to track and manage changes to files over time.
It allows teams to collaborate, maintain version history, and restore previous versions when
needed.
Q 9 What is the git push command?
The git push command is used to upload local commits to a remote repository.
It helps share code with others and keep the remote repository updated.
Q 10 What is a Git conflict? And how do you solve this issue
A Git conflict happens when two people change the same part of a file, and Git cannot decide
which change to keep.

To resolve it, I check the conflicted files using git status, edit the file to keep the correct changes,
remove conflict markers, and then commit the resolved changes.
Q 11 What does git clone do?
The git clone forms a copy of a remote repository upon your local machine.
Q 12 what is merge vs rebase
git merge joins two branches and keeps full history.
git rebase moves your commits on top of another branch. to create a clean, linear history.

Q 13 reset vs revert
git reset removes commits and changes commit history, so it is mainly used for local changes.
git revert is used to undo a commit by creating a new commit.

Q 14 What is the difference between git init and git clone?
git init is used to create a new Git repository in an existing folder.
git clone is used to copy an existing repository from a remote server to your local system.

Q 15 git status
git status is a command used to check the current state of your Git repository.
Q 16 git add
git add is used to stage changes so they are ready to be committed.
Q 17 What is a commit in Git?
A commit is a saved snapshot of your changes in a Git repository.
Q 18 What is git stash?
git stash is used to temporarily save your uncommitted changes without committing them.

Q 19 Difference between Fork and Clone

Fork creates a copy of a repository in your GitHub account, mainly used in open-source projects.
Clone creates a local copy of a repository on your system so you can work on the code.

Q 20 What is the HEAD in Git?
HEAD in Git is a reference that points to the current branch or commit you are working on.
Q 21 Branching in git
Branching in Git allows developers to create separate lines of development so they can work on
features or fixes without affecting the main code.
Q 22 What is a Git bundle?
A Git bundle is a single file that packages a Git repository and its history.
It is used to share or transfer repositories in offline or restricted network environments.
Q 23 What are the advantages of Git over SVN?
Git has advantages over SVN because it is a distributed version control system, which makes it
faster, allows offline work, and provides better branching and merging.
Q 24 what is SVN
SVN (Subversion) is a centralized version control system used to track and manage changes in
source code.
It stores code in a central repository where developers commit their changes, but it is mostly
replaced by Git in modern projects.
Q 25 What is git reflog?
git reflog records all changes made to HEAD in a local Git repository.
It is mainly used to recover lost commits after actions like reset or rebase.
Q 26 recovering deleted branch
If a Git branch is deleted accidentally, it can be recovered using git reflog.
By finding the commit where the branch last existed and recreating the branch from that commit,
the branch can be restored.

Q 27 Git Restore cmd

git restore is used to undo changes in files by restoring them from the staging area or the last
commit, and it can also be used to unstage files.
Read all commands https://github.com/SaimShaikh/Git-GitHub/blob/main/Git/Commands.md
