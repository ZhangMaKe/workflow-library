# GitHub Actions Workflow Library

This repository contains a collection of reusable GitHub Actions workflows.

## Available Workflows

### 1) Terraform Test

This workflow scans your Terraform code for security issues using Trivy.

**Usage:**

To use this workflow, you need to call it from your own workflow.

```yaml
jobs:
  test-terraform:
    uses: <your-org>/workflow-library/.github/workflows/terraform-test.yml@main
    with:
      # The path to the directory containing your terraform code.
      scan-ref: '.'
```

**Inputs:**

- `scan-ref` (required): The path to the directory containing your Terraform code to be scanned. 

### 2) Semantic Release

This workflow manages semantic releases for a repository

**Usage:**

To use this workflow, you need to call it from your own workflow.
 ```yaml
 jobs:
  test-terraform:
    uses: <your-org>/workflow-library/.github/workflows/semantic-release.yml@main
```