# GitHub Actions Workflows

This repository contains reusable GitHub Actions workflows that can be referenced in other repositories.

## Usage

To reuse a workflow from this repository in another repository, follow these steps:

1. **Reference the Workflow:**
   In your repository, create a YAML file in the `.github/workflows/` directory. Use the `uses` keyword to reference the workflow from this repository.

   Example:
   ```yaml
   name: Reused CI Workflow

   on:
     push:s
       branches:
         - main

   jobs:
     build:
       uses: mdnahidmondol/shared-github-actions/.github/workflows/java-spring-build-push-dockerhub.yml@main
