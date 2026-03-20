## Q1.Suppose you are working in a team and have to create a branching strategy where only the release branch goes to the UAT environment. Can you walk me through the commands you would use from cloning to pushing? 

In our team, we use different branches for different stages. First, I clone the project and create a feature branch to work on my task. After completing it, I push it and merge it into the develop branch.

When everything is ready for testing, we create a release branch from develop. Only this release branch is connected to the UAT environment. So when we push this branch, it automatically gets deployed to UAT.

If any bugs are found, we fix them in the release branch itself. Once everything is approved, we merge the release branch into the main branch.

```bash
⚙️ Super Simple Command Flow (Easy to Remember)

👉 Just remember this story:

1. Clone project
git clone repo-url
cd repo
2. Create feature branch
git checkout -b feature/login
3. Push your work
git add .
git commit -m "done"
git push origin feature/login

👉 Merge into develop

4. Create release branch (for UAT)
git checkout develop
git checkout -b release/v1
git push origin release/v1

👉 This goes to UAT

5. Fix bugs (if any)
git add .
git commit -m "fix bug"
git push origin release/v1

6. Final merge after approval
git checkout main
git merge release/v1
git push origin main

```

---
