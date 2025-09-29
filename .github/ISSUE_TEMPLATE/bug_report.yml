name: 🐛 Bug Report
description: Report an issue or unexpected behavior.
title: "[Bug]: "
labels: ["bug", "triage"]
body:
  - type: markdown
    attributes:
      value: |
        Thanks for taking the time to report this issue! Please provide as much detail as possible.

  - type: textarea
    id: reproduction-steps
    attributes:
      label: Steps to Reproduce
      description: Describe the steps needed to reproduce the bug.
      placeholder: |
        1. Go to '...'
        2. Click on '....'
        3. See error
    validations:
      required: true

  - type: textarea
    id: expected-behavior
    attributes:
      label: Expected Behavior
      description: What did you expect to happen?
    validations:
      required: true

  - type: textarea
    id: actual-behavior
    attributes:
      label: Actual Behavior
      description: What actually happened?
    validations:
      required: true

  - type: input
    id: version
    attributes:
      label: Version
      description: Which version of the project/library are you using? (e.g., v1.0.0 or commit SHA)
      placeholder: "e.g. v1.2.0"
    validations:
      required: true

  - type: checkboxes
    id: environment
    attributes:
      label: Environment & Context
      description: Select relevant environment details.
      options:
        - label: I'm using the latest version.
          required: true
        - label: I have searched existing issues.
          required: true
