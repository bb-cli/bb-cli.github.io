---
layout: default
title: Environment
parent: Commands
---

# Environment
{: .no_toc }

All commands for pipeline.
{: .fs-6 .fw-300 }

## List
`bb env environments` Lists all environments.

## Variables
`bb env variables <env-uuid>` Lists all environment variables.

## Create Environment Variable
`bb env create-variable <env-uuid> <key> <value> <secured: 0>` Creates a new environment variable.

## Update Environment Variable
`bb env update-variable <env-uuid> <var-uuid> <key> <value> <secured: 0>` Updates an environment variable.

## Example
```bash
env-update() {
    bb env update-variable \
        '{XXXX-YYYY-XXXX-YYYY-environment-uuid}' \
        '{XXXX-YYYY-XXXX-YYYY-variable-uuid}' \
        ENV \
        "$(cat ~/Code/project/.env| base64)" \
        1
}
```