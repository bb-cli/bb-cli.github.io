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
    _arguments "1: :(help $(bb autocomplete))" "2: :(help $(bb $words[2] autocomplete))"
}

compdef _bb_autocomplete bb
```
