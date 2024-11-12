# Github Action Approval System

This is a simple approval system for Github Actions. It allows you to require approval before a workflow can be run. The approval is done by creating a issue with a specific title.

## Science behind the system
1. A new issue is created with the title `Deploy to Staging needs approval - <commit-sha>`. When a push or pull request is merged into dev.
2. Once there is a comment on the issue with the text `approve` or `LGTM`, the deployment workflow will be triggered.

## Why this system?
[Manual Workflow Approval](https://github.com/marketplace/actions/manual-workflow-approval) is a great action for approval system. But it requires to keep the workflow running until the approval is given. So, you need to pay for the minutes the workflow is running. 
This system is free as it uses Github issues to track the approval. And you only pay for the minutes needed for deployment, not for the wait time.