# ACL Enforcement Tool

Developed by:
Brandon Black - branblac@cisco.com

Global Infrastructure Services - Cisco IT

## Introduction

The end application will use this data to enforce that the entered ACL is in fact on the selected interfaces.
We want to be able to easily add device/interface pairs to a given ACL to have applied.

The high level service/data model is as follows:

```
      ACL Name, ACL Direction
          |
          |
  Device(s)
      |
      |
  Interfaces
      |
      |
  Int Type, Int Number

```

The service allows for us to run compliance checks and remediate for ACL that are missing from a specified interface. ie if a support engineer removed for trouble shooting, but forgot to re-apply.

## Walkthough

The repo has 3 markdown files that walk through how to replicate this package and was built as a training course lab. Please go through and feel free to make issues with any desired improvements.

The service is built with pure YANG/XML Templates, it could be re-factored to leverage Java or Python and remove the complexity for the templates, however the intention was to show the power and flexibility given through pure NSO templates.

## Installation

Install this package as any other NSO Package. Either place in the running directory packages folder or sym-link. issue `make` in the src/ directory then reload the packages from the NSO CLI. There are no dependencies.

## Usage

For usage please see the usage_guide.md file for a detailed walkthrough.
