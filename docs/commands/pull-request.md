---
layout: default
title: Pull Request
parent: Commands
---

# Pull Request
{: .no_toc }

All commands for pull request.
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

## Decline
`bb pr decline <pr-id>` Decline pull request.

## Files
`bb pr files <pr-id>` List changed files in a pull request (diffstat).

## Create
`bb pr create <from-branch> <to-branch> [add-default-reviewers]` Create pull request from one branch to another. If only one branch is given, creates PR from current branch to given branch. You can pass multiple destination branches separated by comma: `bb pr create dev test,staging`. Default reviewers are added automatically, pass `0` as third parameter to skip: `bb pr create dev test 0`.

## Show
`bb pr show <pr-id> [unresolved]` View pull request comments including both general and inline code comments. Add `unresolved` (or `true`) as second parameter to show only unresolved inline comments.

```bash
# Show all comments
bb pr show 42

# Show only unresolved inline comments
bb pr show 42 true
```
