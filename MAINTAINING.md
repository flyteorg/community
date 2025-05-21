# Maintaining Flyte

This page summarizes guidelines to process the issue and PR backlog for Flyte and flytekit in a way it keeps an open dialogue with the user and contributor community, while it helps maintainers to retain focus on the feature work and necessary fixes to support the project goals.

## Labeling issues

We are using [triage-party](https://github.com/google/triage-party?tab=readme-ov-file) to aggregate and analyze the backlog. This tool relies partially on labels. Apply the following labels to help surface and properly categorize the backlog elements:

|  Label | Purpose  |
|---|---|
| `question`  | Issue that includes a question. No feature work is needed to answer. |
| `priority/p0`  | Issues that should be resolved ASAP or PRs that should be prioritized for review and merge  |
|  `priority/p1`   | Important issues or documentation bugs. Estimated time to resolve <= 6 weeks  |
| `triage/discuss` | To be conclusive, it needs discussion with other maintainers  |
|`needs-reproduction`| We have asked the issue author to add context to reproduce the issue or we have the info but couldn't reproduce|
|`do-not-merge`| PRs that are approved but shouldn't be merged yet as they have dependencies.|
|`needs-rebase`| We have asked the author to rebase to the main branch to fix conflicts|

## Pull Requests

Mark in-progress PRs as [Draft](https://docs.github.com/en/pull-requests/collaborating-with-pull-requests/proposing-changes-to-your-work-with-pull-requests/changing-the-stage-of-a-pull-request#converting-a-pull-request-to-a-draft). Adding `WIP` is not enough for this tool. 