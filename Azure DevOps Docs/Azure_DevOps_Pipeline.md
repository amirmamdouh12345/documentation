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

### Azure DevOps Pipelinee Connections with other Resources
- **Connecting to Azure Artifacts** <br>
Publish or consume application packages like .jar files 

- **Deploying to Azure App Service**  <br>
Azure App Services are commonly used for deploying Web Apps, APIs, and Java/Spring Boot services.

**NOTE:**
Any Connection between Azure DevOps Pipeline and any other Resources needs permissions attached to this Pipeline.


## Environments
An Environment represents a target where your app or code gets deployed. <br>
It could be:     
- A set of virtual machines (VMs)
- An Azure resource (Web App, AKS, Function App)
- A Kubernetes namespace

## Library
A Library is where you store and manage variables, variable groups, and secure secrets used across multiple pipelines.

``` bash
variables:
- group: 'my-variable-group'   # refers to a Library group

steps:
- script: echo "Deploying to $(ENV)"

```




