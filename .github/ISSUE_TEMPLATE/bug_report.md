name: Bug Report
description: Identified a bug in one Upbound's products?
labels: bug,needs:triage
title: "<bug overview>"
body:
  - type: dropdown
    id: product-area
    attributes:
      label: Product Area
      description: What Product Area is this request for?
      options:
        - Upbound Crossplane (UXP)
        - up (CLI)
        - Upbound SaaS
        - Upbound Marketplace
        - Documentation
        - Functions
    validations:
      required: true
  - type: textarea
    id: problem
    attributes:
      label: Problem
      placeholder: What happened and what did you expect should have happened?
    validations:
      required: true

  - type: textarea
    id: repro
    attributes:
      label: Reproduction
      placeholder: Add the steps needed to reproduce the state you observed.
    validations:
      required: true

  - type: textarea
    id: log
    attributes:
      label: Relevant Error Output Snippet
      description: |
        If possible, provide a relevant log from the error or panic output.
      render: shell
    validations:
      required: false

  - type: textarea
    id: env
    attributes:
      label: Environment
      value: |
          - Cloud provider or hardware configuration: 
          - Kubernetes version (use `kubectl version`): 
          - Kubernetes distribution (e.g. Tectonic, GKE, OpenShift): 
          - OS (e.g. from `/etc/os-release`): 
          - Kernel (e.g. `uname -a`): 
      render: markdown
    validations:
      required: false    
