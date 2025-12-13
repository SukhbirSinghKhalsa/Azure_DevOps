# Azure_DevOps
Contains Different Yaml files used in Azure Devops, additionally having CI CD pipelines, Security checkup using tools like tflint, tfsec, checkov

### File Structure
```bash
root/
│
├── .pipeline/
│   └── Application_Pipeline.yml
│   └── Linting.yml
```
---

### Useful Links
#### 🔧 Azure DevOps Pipeline Variables

This pipeline uses built-in Azure DevOps variables such as:

- `$(System.DefaultWorkingDirectory)`
- `$(Agent.ToolsDirectory)`
- `$(Build.ArtifactStagingDirectory)`

These variables are automatically provided by Azure DevOps and help standardize paths, agent behavior, and pipeline execution.

👉 **Learn more about Azure DevOps predefined and custom variables:**  
[Azure DevOps Pipeline Variables – Official Documentation](https://learn.microsoft.com/en-us/azure/devops/pipelines/build/variables?view=azure-devops&tabs=yaml)

---

### Application_Pipeline.yaml file
- It is a simple pipeline which generates the artifact for React Based  MFEs
```bash
[ Install Node ] --> [ Check Version ] --> [ npm install ] --> [ Build ] --> [ Publish Artifact ]
```
---

### Linting.yaml file
- These file will consist of different linting tools used to check formatting, syntax of different Langauges, Frameworks
#### 🔍 Lint Tools Used

| File Type | Tool | Purpose |
|----------|------|--------|
| JavaScript / TypeScript | **Biome** | Fast, modern JS/TS linter |
| CSS | **Stylelint** | Enforces consistent CSS styling |
| YAML | **yamllint** | Validates YAML syntax and formatting |
| Markdown | **markdownlint** | Ensures Markdown best practices |

#### 🔁 Lint Job Flow Diagram
```bash
[ Start Lint Job ]
        |
        v
[ Lint JavaScript (Biome) ]
        |
        v
[ Lint CSS (Stylelint) ]
        |
        v
[ Lint YAML (yamllint) ]
        |
        v
[ Lint Markdown (markdownlint) ]
        |
        v
[ Lint Job Complete ]
```


