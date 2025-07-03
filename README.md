# Azure DevOps Overview
Azure DevOps is a cloud-based platform provided by Microsoft that offers a complete set of tools for software development and DevOps practices. It helps teams plan work, collaborate on code development, build and deploy applications, and manage the entire application lifecycle.

## Organization
- The top-level container in Azure DevOps (e.g., contoso.visualstudio.com).
- Represents your company, team, or department.
- Can contain multiple projects.

### Key Features:
- **User Management:**
Controls access for all projects under it (e.g., Azure AD integration).

- **Billing/Subscriptions:**
Manages licenses (e.g., Azure Pipelines parallel jobs).

- **Shared Resources:**
Organization-wide settings: Policies, extensions, agent pools.
Cross-project visibility: Users with access can switch between projects.

## Project 
- A sub-container within an organization for a specific initiative (e.g., "E-Commerce App").
- Isolates work, code, and artifacts for a single team or product.

## Core Services in Azure DevOps Projects:
1. Azure Boards
2. Azure Repos
3. Azure Pipelines
4. Azure Test Plans
5. Azure Artifacts
   
### Azure Boards <br>
**Purpose:** Project management. <br>
**Tools:** Work items, Kanban boards, backlogs, sprints. <br>
**Used for:** Tracking tasks, bugs, user stories, features.<br>
### Azure Repos         <br>
**Purpose:** Source code version control.   <br>
**Tools:** Git repositories or Team Foundation Version Control (TFVC).  <br>
**Used for:** Collaborating on code with pull requests, branching, and versioning. <br>
### Azure Pipelines    <br>
**Purpose:** Continuous Integration / Continuous Deployment (CI/CD).  <br>
**Supports:** Multi-platform (Linux, Windows, macOS) and multi-language (Java, .NET, Node.js, Python, etc.). <br>
**Used for:** Automating build, test, and deployment workflows. <br>
### Azure Test Plans  <br>
**Purpose:** Manual and exploratory testing.  <br>
**Used for:** Planning, executing, and tracking tests to improve software quality. <br>
### Azure Artifacts  <br>
**Purpose:** Package management.    <br>
**Supports:** NuGet, npm, Maven, Python packages.  <br>
**Used for:** Hosting and sharing packages across teams and projects.  <br>


## Azure DevOps Permissions & Security:
Azure DevOps provides flexible, multi-layered security to control access at the organization, project, and individual resource levels.

### Permission Structure Overview:
Azure DevOps permissions are managed through:
- Security Groups (Predefined/Custom roles)
- Access Levels (Stakeholder, Developer, etc.) 
- Fine-Grained Permissions (Repos, Pipelines, Work Items, etc.)

### Security Groups
- Default Security Groups ( Project Admins -> DevOps/IT  , Contributers -> Developers,QA , Reader -> Stackholder )
- Custom Security Groups: Create groups for specific needs

### Fine-Grained Permissions
Edit in Security configurations and Override defaults for specific resources:
- **Repositories**: <br>
Branch-level control: Restrict who can push to main.  <br>
Repo-level control: Hide sensitive repos.  <br>

- **Pipelines**:
Limit who can edit/run pipelines.

