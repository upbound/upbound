name: Feature Request
description: New features and enhancement ideas for the Upbound product.
labels: enhancement
title: "<component name>: <feature overview>"
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
    id: Overview
    attributes:
      label: Overview of the request.
      description: What would you like to see implemented in Upbound?
      placeholder: Tell us about your idea.
    validations:
      required: true