name: "🚀 Project Task"
description: "Create a new issue for a task in the Online Leaderboard + Save Sync project."
title: "[Task] "
labels: ["triage"]
assignees: []
body:
  - type: markdown
    attributes:
      value: |
        Thanks for contributing! Please fill out the task details below.
  - type: input
    id: summary
    attributes:
      label: Task Summary
      description: Short description of what this task does.
      placeholder: e.g., Implement /submit_score endpoint
    validations:
      required: true
  - type: textarea
    id: details
    attributes:
      label: Task Details
      description: Describe the task steps or requirements in detail.
      placeholder: What needs to be done, technologies involved, references, etc.
  - type: dropdown
    id: category
    attributes:
      label: Task Category
      description: Select which part of the project this task belongs to.
      options:
        - backend
        - client
        - infra
        - docs
        - enhancement
    validations:
      required: true
  - type: dropdown
    id: milestone
    attributes:
      label: Milestone
      description: Which milestone does this belong to?
      options:
        - Week 1 – Backend MVP
        - Week 2 – Client + Deployment
        - Stretch Goals
  - type: checkboxes
    id: checklist
    attributes:
      label: Task Checklist
      description: Optional checklist for sub-tasks.
      options:
        - label: Write code
        - label: Test locally
        - label: Write docs / README updates
        - label: Commit + push to GitHub
