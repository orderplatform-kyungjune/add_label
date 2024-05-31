# Create D-5 Label GitHub Action
This GitHub Action automatically creates a "D-5" label on your repository at a specified time.</br> 
If a label starting with "D-" already exists, it will not create the "D-5" label.

## Usage
To use this action, add the following step to your workflow YAML file.

## Example Workflow
Create a file named `add_label.yml` in the `.github/workflows` directory of your repository with the following content

```yaml
name: add D-5 label on pull request opened

on:
  pull_request:
    types: [opened, reopened]

jobs:
  call-workflow:
    runs-on: ubuntu-latest
    steps:
      - name: use add D-5 label action
        uses: torder-lkj/add_label@v1.0.2 # Please make sure to use the latest version.
        with:
          github_token: ${{ secrets.TOKEN }}
```

Please make sure to replace ${{ secrets.TOKEN }} with your actual GitHub token.</br> 
Also, ensure you are using the latest version of this action.