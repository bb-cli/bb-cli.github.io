---
layout: default
title: Pull Request
parent: Commands
---

# Pull Request
{: .no_toc }

PR commands.
{: .fs-6 .fw-300 }

## List
`bb pr list [branch]` list pull request for repository, You may add optional `brach` parameter to see pull request that made for given branch. For example can can use this command to see pull request that destination is dev branch `bb pr list dev`.

## Merge 
`bb pr merge <pr-id>` merge pull request.

## Diff 
`bb pr diff <pr-id>` Get pull request diff.

## Commits 
`bb pr commits <pr-id>` Get pull request commits.

## Approve
`bb pr approve <pr-id>` Approve pull request.

## Not Approve
`bb pr no-approve <pr-id>` Revert pull request to not approved status.

## Request Changes
`bb pr request-changes <pr-id>` Request changes for pull request.

## Not Request Changes
`bb pr no-request-changes <pr-id>` Revert pull request to not request changes status.

## Declime
`bb pr decline <pr-id>` Decline pull request.

## Create
`bb pr create dev test` Create pull request from dev to test branch.
