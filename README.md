# Azure DevOps Board
Azure Boards is a work tracking system within Azure DevOps. 
It helps teams manage and track **tasks**, **bugs** or **features** throughout the development lifecycle using Agile, Scrum, or Kanban methodologies.

## Azure DevOps Board Processes types:
There are three different types of processes in Azure DevOps Board which each one of them has different set of work items:
- Basic ( Epic , Issue , Task )
- Agile
- Scrum
- CMMI

## Focus on Basic Processs
The Basic process is the simplest and most lightweight process in Azure Boards. it's used for simple projects. <br>
**Work Item Hierarchy in Basic Process:**
```bash
Epic
 └── Issue
      └── Task
```
### Epic 
A large body of work that can be broken down into smaller parts (issues). <br>
Think of it as a goal or major feature area. 

### Issue
A work item that belongs to an epic and describes a specific feature, bug, or task. <br>
Issues are the main units of work you manage on the Board. <br>
Represents Feature, bug, user story, or general task.
✅ Example Issues (under Epic: "User Management System"):
- “Implement login API”
- “Fix registration validation bug”
- “Design forgot password screen”

### Task
A detailed step required to complete an issue. <br>
Tasks are smaller units of work or technical steps done by a developer or tester. <br>
Represents To-do items inside a feature/bug. <br>

Example Tasks (under Issue: "Implement login API"): <br>
- “Create SQL table for users”
- “Write JWT token generator”
- “Add unit tests for login endpoint”
