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
`bb pr create <target-branch> [source-branch] [options]` Create pull request. If `source-branch` is omitted, the current branch is used as source.

### Options

| Flag | Description |
|---|---|
| `-i` | Interactive mode — prompts for missing title and/or description |
| `--title "..."` | Set the PR title (non-interactive) |
| `--description "..."` | Set the PR description (non-interactive) |

### Usage Examples

**Fully non-interactive (CI-safe, default behavior):**
```bash
bb pr create develop
```

**Interactive mode — prompts for title and description:**
```bash
bb pr create develop -i
```

**Non-interactive with custom title and description:**
```bash
bb pr create develop --title "Fix login bug" --description "Resolves timeout issue on auth endpoint"
```

**Mixed — provide some flags, prompt for the rest:**
```bash
bb pr create develop -i --title "Fix login bug"
```
Uses the provided title and only prompts for the missing description.

**Multiple target branches:**
```bash
bb pr create develop,staging,main
```

Default reviewers are added automatically. Pass `0` as third parameter to skip: `bb pr create develop test 0`.

## Show
`bb pr show <pr-id> [unresolved]` View pull request comments including both general and inline code comments. Add `unresolved` (or `true`) as second parameter to show only unresolved inline comments.

```bash
# Show all comments
bb pr show 42

# Show only unresolved inline comments
bb pr show 42 true
```
