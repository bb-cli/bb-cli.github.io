---
layout: page
title: Autocomplete Arguments
permalink: /autocomplete/
nav_order: 5
---

# Autocomplete Arguments
{: .no_toc }

You may add something like this to add auto completion feature.
{: .fs-6 .fw-300 }

## Definition

```
_bb_autocomplete() {
    local pipeline_commands="get latest wait"
    local pr_commands="list diff commits approve no-approve request-changes no-request-changes decline merge create"
    local branch_commands="list user name"
    local auth_commands="save show"

    _arguments "1: :(pr pipeline branch auth)" "2: :(help $pipeline_commands $pr_commands $branch_commands $auth_commands)"
}

compdef _bb_autocomplete bb
```
