# Azure DevOps Artifacts
Azure Artifacts is a package management service in Azure DevOps.

## Different Package Types
| Package Type           | Description                 |
| ---------------------- | --------------------------- |
| **NuGet**              | .NET packages               |
| **npm**                | JavaScript/Node.js packages |
| **Maven**              | Java/Android                |
| **Python**             | Python wheels and libraries |

## Core Components
1. Feeds
A Feed is a collection of packages. You can create multiple feeds per project or org.

### Feeds control:
- What packages are stored
- Who can read/publish
- Upstream sources (e.g. npmjs, nuget.org)

2. Packages
These are the actual libraries, components, tools, or bundles you publish.

3. Upstream Sources
Upstream sources in Azure Artifacts allow your feed to automatically fetch and cache packages from external (or other internal) sources. <br>
Azure DevOps can automatically download and cache packages from public sources — securely and reliably.

## Azure Artifacts Integration with Other Azure DevOps Services
1. Azure Repos (Code)
You write code in Azure Repos

2. Azure Pipelines (CI/CD)
Artifacts works directly with Azure Pipelines in two ways:
- CI Pipelines (Build)
Publish packages to Azure Artifacts feed.
``` bash
      - task: Npm@1
        inputs:
          command: 'publish'
          workingDir: './nodejs_app/'
          customRegistry: 'useFeed'
          customFeed: '4c33b7d7-5a25-424e-b681-97cc46090a1e/fd42167c-3667-4943-806b-a017155326a2'
```
- CD Pipelines (Release)
Download published packages from a feed <br>
Use them to deploy to App Service, AKS, VMs, etc.4. Artifacts Feeds

3. Artifacts Feeds
You can create feeds scoped to:
- Organization-wide
- Project-level        <br>
Developers and pipelines publish and install packages from these feeds 

4. Permissions & Security Integration
You can manage access through:
- Users/Groups like Developers, QA, Viewers
- Build Service (for pipelines)

Use Azure DevOps security groups to control:
- Who can publish packages
- Who can install them

