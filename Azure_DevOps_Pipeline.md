# Azure DevOps Pipelines
Azure Pipelines is a CI/CD (Continuous Integration / Continuous Delivery) service that:
- Builds, tests, and deploys your code
- Works with GitHub, Azure Repos, Bitbucket, etc.
- Supports Windows, Linux, macOS agents

| Type                 | Description                                             |
| -------------------- | ------------------------------------------------------- |
| **Build Pipeline**   | CI: Build, test, and package your code                  |
| **Release Pipeline** | CD: Deploy artifacts to environments (VMs, Azure, etc.) |

## Pipeline Structure
Trigger key triggers specific branches
``` bash
trigger:
  - main
```
Pool key determines what type of machine (agent) should be used to run your pipeline steps.
``` bash
pool:
  vmImage: 'ubuntu-latest'
```

Pipeline is divided into Stages. Each stage is divided into jobs. Each job is divided into steps.
``` bash
Stages
|__ Jobs
     |__ Steps
```

## Azure DevOps Pipelinee Connections with other Resources
- **Connecting to Azure Artifacts** <br>
Publish or consume application packages like .jar files 
- **Deploying to Azure App Service**  <br>
Azure App Services are commonly used for deploying Web Apps, APIs, and Java/Spring Boot services.







