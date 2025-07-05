# Azure Repo Overview 
Azure Repos is Azure DevOps' version control system, supporting Git (distributed) and TFVC (centralized).

## Azure Repo Side bar Structure 
Repos → Files | Commits | Pushes | Branches | Tags | Pull Requests

1. **Files**
- View current code base
- Browse folders and files
- See commit history for a file
- Create/edit/delete files (if permitted)

2. **Commits**
Shows all commit history on a selected branch.  <br>
NOTE:  <br>
You can click on any commit to see the updates/diff from the commit commit 

3. **Branches**
Shows all branches in the repo.  <br>
You can protect branches Branch Policies. you can decide the permissions of each User/Group on your Branch.

4. **Pull Requests (PRs)**
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






