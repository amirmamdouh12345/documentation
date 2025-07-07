# Azure Repo Overview 
Azure Repos is Azure DevOps' version control system, supporting Git (distributed) and TFVC (centralized).

## Azure Repo Side bar Structure 
Repos → Files | Commits | Pushes | Branches | Tags | Pull Requests

1. **Files**
- View current code base
- Browse folders and files
- See commit history for a file
- Create/edit/delete files (if permitted)

2. **Commits** <br>
Shows all commit history on a selected branch.  <br>
NOTE:  <br>
You can click on any commit to see the updates/diff from the commit commit 

3. **Branches**  <br>
Shows all branches in the repo.  <br>
You can protect branches Branch Policies. you can decide the permissions of each User/Group on your Branch.

4. Tags
Git tags are human-readable names that point to a specific commit ID , often used to mark release versions, such as v1.0.0, v2.1.5, beta-release, etc.



6. **Pull Requests (PRs)** <br>
Workflow for reviewing and merging code from one branch into another

Real Example 
``` bash
# Clone you Azure Devops Repo
git clone https://dev.azure.com/amir-team/shop-api/_git/shop-api

# Create new branch
git checkout -b feature/add-cart

# Make changes and commit
git add CartController.java
git commit -m "Add cart controller"

# Push branch
git push origin feature/add-cart
```
Next you can create a Pull request to merge between feature/add-cart and master branch.

7. Security

there are two main Security options:          !!!Chargable!!!
1. Secret Protection Plan
Protects your branches from accidentally committing secrets, like API keys, passwords, or tokens.
2. Code Security Plan
Offers full code scanning and dependency analysis, focused on identifying security vulnerabilities.

## Repository Permissions
Main Permissions : <br>
- Read           
- Contribute
- Colaborate

| **Permission** | **Can View** | **Can Push**            | **Can Configure** | **Who Gets It?**  |
|----------------|--------------|--------------------------|--------------------|--------------------|
| `Read`         | ✅ Yes       | ❌ No                   | ❌ No              | Viewers, QA        |
| `Contribute`   | ✅ Yes       | ✅ Yes (with PR)        | ❌ No              | Developers         |
| `Collaborate`  | ✅ Yes       | ✅ Yes                  | ✅ Yes             | Admins, Leads      |


### You can assign permissions to:
- Users
- Groups
- Service accounts (for pipelines)





