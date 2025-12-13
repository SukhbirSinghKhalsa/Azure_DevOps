# Azure_DevOps
Contains Different Yaml files used in Azure Devops, additionally having CI CD pipelines, Security checkup using tools like tflint, tfsec, checkov

### File Structure
```bash
root/
│
├── .pipeline/
│   └── Application_Pipeline.yml
│
```

#### Application_Pipeline.yaml file
- It is a simple pipeline which generates the artifact for React Based  MFEs
```bash
[ Install Node ] --> [ Check Version ] --> [ npm install ] --> [ Build ] --> [ Publish Artifact ]
```

#### Linting.yaml file
- These file will consist of different linting tools used to check formatting, syntax of different Langauges, Frameworks
```bash

```
