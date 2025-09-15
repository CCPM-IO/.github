
[CCPM IO SOPs](../../CCPM%20IO%20SOPs.md) > [Github SOPs](../Github%20SOPs.md)

# Github Repo Maintenance SOP

- 1 [Purpose](#purpose)
- 2 [Roles and responsibilities](#roles-and-responsibilities)
  - 2.1 [Repository creation](#repository-creation)
    - 2.1.1 [Naming](#naming)
    - 2.1.2 [Permissions](#permissions)
    - 2.1.3 [Basic requirements](#basic-requirements)
    - 2.1.4 [High level structure](#high-level-structure)
    - 2.1.5 [Rule set](#rule-set)
  - 2.2 [Repository deprecation](#repository-deprecation)
  - 2.3 [Management](#management)
    - 2.3.1 [General guidelines](#general-guidelines)
    - 2.3.2 [Releases](#releases)
  - 2.4 [Structure](#structure)
    - 2.4.1 [Style guides](#style-guides)
- 3 [Issues](#issues)
  - 3.1 [Issue templates](#issue-templates)
  - 3.2 [Issue guidelines](#issue-guidelines)
    - 3.2.1 [Title](#title)
    - 3.2.2 [Description](#description)
    - 3.2.3 [Assignees](#assignees)
    - 3.2.4 [Labels/Type](#labels-type)
    - 3.2.5 [Projects](#projects)
    - 3.2.6 [Milestone](#milestone)
    - 3.2.7 [Relationships](#relationships)
- 4 [PRs](#prs)
  - 4.1 [PR template](#pr-template)
  - 4.2 [PR guidelines](#pr-guidelines)
    - 4.2.1 [Merge strategy](#merge-strategy)
    - 4.2.2 [Title](#title)
    - 4.2.3 [Description](#description)
    - 4.2.4 [Reviewers](#reviewers)
    - 4.2.5 [Assignees](#assignees)
    - 4.2.6 [Labels](#labels)
    - 4.2.7 [Projects](#projects)
    - 4.2.8 [Milestones](#milestones)
    - 4.2.9 [Development](#development)
- 5 [Contribution structure](#contribution-structure)
  - 5.1 [Branching vs. Forking](#branching-vs-forking)
    - 5.1.1 [Branching](#branching)
    - 5.1.2 [Forking](#forking)
  - 5.2 [Branch deletion](#branch-deletion)
  - 5.3 [Branch naming](#branch-naming)

# Purpose

This document serves as the standard operating procedure (SOP) for any and all aspects of maintaining GitHub repositories within the CCPM-IO organization GitHub. Any question that you feel is not addressed here should be opened as an issue on the [CCPM-IO .github](https://github.com/CCPM-IO/.github/issues) repo following this template (link to .github issue creation template), assigned to the “CCPM SOP Development” project, and assigned to a team member (who is not the director).

# Roles and responsibilities

|  **Task**                                                        |  **Responsible**                        |  **Accountable**                |  **Consulted**                          |  **Informed**    |  **Comments**                                                                                                                                                                                                                                                                      |
|:-----------------------------------------------------------------|:----------------------------------------|:--------------------------------|:----------------------------------------|:-----------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Repository creation                                              | Primary repository maintainer           | Secondary repository maintainer | IO team                                 |                  | Internal members may add repos under the organization header after discussion with IO team                                                                                                                                                                                         |
| Team creation and permission management for CCPM-IO organization | Director                                |                                 |                                         | IO team          | The director is responsible for maintaining teams on GitHub and assigning roles and permissions to all individuals that have access to the CCPM-IO organization                                                                                                                    |
| Repository deprecation                                           | Director                                |                                 | IO team                                 |                  | Repositories will be selected for deprecation/archival on a yearly basis. Original maintainer will be informed unless they are no longer with the team.                                                                                                                            |
| Creating PRs                                                     | Issue assignee                          |                                 | Primary/Secondary repository maintainer | Director         | PRs should be created by the individual who addressed the issue that the PR is related to. IO peers should be set as reviewers, director informed                                                                                                                                  |
| Milestone creation                                               | Primary repository maintainer           | Secondary repository maintainer | Director                                | IO team          | The project lead is responsible for creating and maintaining milestones on their respective repositories. The director and other contributing members should be informed about what the milestone is intended to track and how it is to be used.                                   |
| Issue creation                                                   | IO team member                          |                                 |                                         | IO team          |                                                                                                                                                                                                                                                                                    |
| Project creation                                                 | IO team member                          | Director                        |                                         |                  |                                                                                                                                                                                                                                                                                    |
| Epic creation                                                    | Primary/secondary repository maintainer |                                 | Director                                | IO team          |                                                                                                                                                                                                                                                                                    |
| Creating releases                                                | Primary repository maintainer           | Secondary repository maintainer | Director                                | IO team          | The repository maintainer is responsible for releases in each respective repository. Secondary contributors to that repository will be accountable for releases. Director should be consulted prior to release, and the entire IO team (and maybe external stakeholders) informed. |

## Repository creation

Generally anyone who is on the IO team are permitted to create repositories under the CCPM-IO organization. However, it is required to have a discussion with the IO team and be granted approval prior to creating a repository under the CCPM-IO organization GitHub. It is generally recommended to create a repository under your personal account first, then discuss with the IO regarding moving it to the CCPM-IO GitHub. The CCPM-IO organization will be the ultimate owner and admin for all repositories contributed to by the IO team as a whole.

### Naming

Repositories that will belong in the CCPM-IO organization should follow these naming conventions:

- All lowercase letters, save for acronyms (ie. CART, PGx, etc.)
- Names of companies or organizations should follow their naming conventions (eg. DNAnexus)
- No spaces are allowed in names
- If a name should contain multiple words, they should be delimited with hyphens (underscores and other delimiters are not allowed)
- Names should be kept to 20 characters or less, barring special circumstances to be approved on an ad-hoc basis by the IO team

### Permissions

Permissions will be managed by the IO director at the level of the organization using the tools created by GitHub for team management. Generally, anyone working on the IO team may be granted permissions to any repository under the CCPM-IO organization by anyone with permissions to do so.

For individuals outside of the CCPM-IO team (eg. UCHealth, CU researchers, etc.), the director of IO should be consulted prior to granting anyone permissions to repositories maintained by the CCPM-IO team. The director of IO holds the final discretionary power to permit or deny permissions to any repository maintained by the CCPM-IO team. Requests for granting permissions to a repository may be made through email or slack. The director is responsible for creating teams on GitHub and assigning roles and permissions to all individuals that have access to the CCPM-IO organization.

The director is also responsible for revoking permissions to repositories or the CCPM-IO organization as a whole. By default, permission should be treated as a “need-to-know” basis. Permissions will be only be granted on an ad-hoc basis. For example, a contributor who solely needs to read a piece of documentation regarding a codebase may be sent a document, but not granted permissions to the repo as a whole. Using GitHub’s built in permission management tools, the director will maintain organization permissions as a whole.

Revocation causes:

- Leaving the CCPM - permissions will be immediately revoked and granted back on an ad-hoc basis
- Failing to follow the guidelines outlined in this document
- A guest that was granted temporary access

### Basic requirements

Repositories will follow a template outlined in the: [ccpm-template-repo](https://github.com/CCPM-IO/ccpm-template-repo). It is strongly advised to use this repository as a template for creating any repository that will be included under the CCPM-IO organization. Otherwise, all components will need to be created from scratch. Language specific frameworks will govern project structure on a more granular level (see [Github Repo Maintenance SOP](Github%20Repo%20Maintenance%20SOP.md)). However, each repository in the CCPM-IO organization will adhere to the following high-level template:

### High level structure

- README.md

  - Title
  - Background

    - Provide relevant context for the CCPM project
  - Structure

    - Explanation of the repository architecture
  - Usage instructions

    - Instructions to install and use the software or pipeline in the repository
  - Additional resources

    - Provide links to other documentations in the docs folder in the repository
- docs/
- .github/

### Rule set

- Force push to main disabled
- Merge commits disabled
- Pull request required before merging
- Default GitHub issue and PR labels will be available in all repositories

## Repository deprecation

The CCPM-IO team as a whole will evaluate repositories on a yearly cadence, generally at the end of the calendar year. The CCPM-IO team will evaluate all repositories under the organization and archive those that are no longer being used. Rather than renaming and keeping repositories in an active state, they will be deprecated and archived so that information is retained, but does not clutter the organization repository list.

## Management

### General guidelines

- All repositories in the CCPM-IO organization will have branch protection rules for main, preventing direct merges or force pushes
- All pull requests (PRs) require at least one approval prior to merge
- Branch restrictions may be set in place on an ad-hoc basis for repositories with external stakeholders
- Use relative paths for links to documents inside repository, refrain from using absolute paths
- For forks

  - Org → personal repo, NEVER personal repo → org

### Releases

The CCPM-IO uses [Semantic Versioning (SemVer)](https://semver.org/), [GitHub flow](https://docs.github.com/en/get-started/using-github/github-flow) and [Release drafter](https://github.com/release-drafter/release-drafter) for versioning and release management. Repository releases, including new features, bug fixes, and other updates, are managed through Pull Requests (PRs) to the main branch. Each release involves determining the type of release (major, minor, or patch), creating a PR, testing the release, and deploying the code to the production environment. A new GitHub release will be tagged with the appropriate version number and will include all changes in the main branch up to the commits in the PR. This information is more thoroughly described in the CCPM-IO [RELEASE.md](https://github.com/CCPM-IO/cart/blob/main/resources/RELEASE.md).

High-Level Release Process:

1. Create a Pull Request (PR) for the release incorporating your changes.
2. Update the PR with test details and obtain approvals.
3. Merge the PR to the main branch.
4. Deploy the updated code to the production environment.

## Structure

The top level structure and overall architecture of each repository will follow the conventions outlined in the style guide for each respective project type. These will generally follow language or framework specific style guides. (TODO: Create list with links to each style guide here)

### Style guides

- Python
- R
- Shell/bash
- Front-end web dev: HTML/Javascript/CSS
- Nextflow
- Sbatch (extension of shell/bash guidelines)

# Issues

Every repository in the CCPM-IO organization will use issues to track progress on projects. Every piece of development that is done for a project should be tracked through one or more issue(s). It is standard practice and always recommended to open an issue prior to making any changes to code. An issue may be opened retroactively after a branch has been created or code has been altered, but it is never acceptable to create a PR prior to creating the related issue. All issues will be addressed by PRs and therefore need to be opened prior to creating a merge/pull request.

## Issue templates

In general, issues will fall into one of three categories: bug, task, or feature. The CCPM-IO follows templates for each of these issue types:

- Bug
- Task
- Feature

## Issue guidelines

### Title

Issue titles will always begin with an action verb to describe what type of issue it is. They are as follows:

- Bug = Fix/Resolve …
- Task = Do/Make …
- Feature = Add/Create …

This format ensures that it is immediately apparent to all contributors what type of issue this is, without having to read the description. The title should be kept short enough that it is visible in it’s entirety on the “title line” on the issue page.

### Description

Issue descriptions will follow the templates linked in this section. Descriptions should be thorough but concise. Ensure to add relevant context so far as it gives the assignee of what the problem is without being too verbose. Each section in the template description should be filled out with only relevant information.

In general, issue descriptions will contain:

- Links to the line, methods, or files related to the issue being opened
- Screenshots and reproducibility steps to provide context where relevant
- Links to documentation that may provide more context about the issue

### Assignees

Issues should be assigned to the relevant parties upon creation. If the issue is opened before that determination has been made, the issue should be assigned to the creator. This indicates that the creator will take responsibility for identifying the proper assignees and assigning the issue to them.

### Labels/Type

Labels and type should be assigned upon issue creation. The type is used to clarify the high-level status of the issue and is reserved for only bug, task, and feature. Labels will be used to provide more context to what the issue specifically concerns. More than one label is allowed as long as they are all relevant. A core set of labels will be shared across all repositories that follow GitHub’s base set of issue labels. Additional labels will be created on an ad-hoc basis for each individual repository. Label creation will follow the GitHub conventions (all lowercase, limited to two words, etc.).

### Projects

All issues should be assigned to a project, orphan issues are not allowed. This is because the CCPM-IO team routinely tracks issues that are tied to multiple repositories. If an issue is created and does not have a relevant project to assign it to, it should be brought up during the internal IO sync, so that one may be created.

### Milestone

Milestones will be used to track large features that contain multiple sub-tasks. Milestones are intended to be used to track serial steps during development. In other words, once completed, a milestone removes blockers before the next steps of a project can continue. Not every issue will be assigned to a milestone. Examples of things that do NOT require milestones are hotfixes, CI/CD changes, and documentation changes. Generally milestones WILL be utilized for things like releases, refactors, and major components of pre-release steps.

### Relationships

Issue relationships are not required to be assigned upon issue creation. However, they may be assigned some time after issue creation. Issues may be assigned to parent issues if they are related to the resolution of it. Generally the CCPM-IO team uses parent issues to track the progress of multiple tasks. Each issue should reflect the resolution of a single task. A task is the smallest unit of work that can be tested individually.

# PRs

In the CCPM-IO organization, we follow a [GitHub flow](https://docs.github.com/en/get-started/using-github/github-flow) for branching and pull request (PR) creation. CCPM-IO use a strategy of merging all PRs to main, then creating releases and tagged versions for production. Pull requests (PRs) will be used prior to merging any code to main branch of a repository.

## PR template

TODO: Link to PR template

## PR guidelines

In general, one PR should close one issue. Each issue should contain a single task, the smallest unit of development that can be tested. A PR should be made to address each and every issue that is created. This generally means each PR will change a relatively small amount of code and will not be overly cumbersome to review. This may not always be the case for new features, and a reviewer always reserves the right to request a PR be split into multiple PRs.

A single PR may be used to resolve multiple issues if it is not possible to test each issue independently.

### Merge strategy

The CCPM-IO organization follows a squash merge strategy for merging code. More regarding the standard can be found in [GitHub’s documentation](https://graphite.dev/blog/pull-request-merge-strategy).

Commit messages for individual commits should follow [conventional commit guidelines](https://www.conventionalcommits.org/en/v1.0.0/). Eg. `<type>[optional scope]: <description>`. This is a helpful VSCode [extention](https://marketplace.visualstudio.com/items?itemName=vivaxy.vscode-conventional-commits).

After approval has been given by all requested reviewers, the PR creator or repository maintainer may merge a PR into the main branch.

### Title

PR titles will follow the conventional commit message syntax, `<type>[optional scope]: <description>`. The CCPM-IO organization uses conventional commit messages and squash-merge for creating PRs, so the PR titles should follow this format. More about conventional commits can be found later in this section.

### Description

Descriptions should follow the format outlined in the [Github Repo Maintenance SOP](Github%20Repo%20Maintenance%20SOP.md) in this section. In general, descriptions should be a thorough and detailed explanation of what changes were made, and why they’re relevant. They should always include a link to the issue it is addressing and how the PR resolves it. [GitHub convention](https://docs.github.com/en/issues/tracking-your-work-with-issues/using-issues/linking-a-pull-request-to-an-issue) should be followed to ensure PRs close issues.

### Reviewers

PRs require at least one reviewer’s approval, and will generally be the secondary maintainer for that repository. In special circumstances, additional reviewers may be needed as well as director approval, but this is not the standard practice.

It is expected that reviews will occur in no more than three business days after assignment. If a review cannot be completed in three business days, a comment should be made regarding expected timelines for review. Reviews should be constructive and address specific issues if they exist.

If a reviewer feels that a PR contains too many changes, they always reserve the right to request the PR be split into more than one.

### Assignees

This should always be the creator.

### Labels

This will follow the same set of labels described in the [Github Repo Maintenance SOP](Github%20Repo%20Maintenance%20SOP.md) of this document. PR labels should match the issue they address.

### Projects

All PRs should be assigned to the same project that the issue originated from.

### Milestones

All PRs should be assigned to the milestone that the issue it’s addressing is assigned to (if applicable).

### Development

This section should be automatically filled in when linking a related issue in the PR description.

# Contribution structure

## Branching vs. Forking

For contributing code to a repository, there are two main strategies, cloning the repository and creating branches or forking the repository, creating branches, and creating PRs from the forked repository to the main repository. At the CCPM-IO, we use both conventions depending on the project type. Generally, it is up to the personal preference of the developer which strategy to use, either is okay. However, some work will necessitate using one strategy over the other.

### Branching

Several of the CCPM-IO maintained repositories have GitHub workflows, which use GitHub secrets defined in our CCPM repository. Pull requests from forked repositories are not given access to GitHub secrets. In this instance, branches must be made directly on the main repository.

### Forking

Forks are necessitated in repositories where the CCPM-IO develops GitHub workflows themselves. Changes could not be made and compared against the main repository since the changes are what dictate the tests (GitHub actions).

## Branch deletion

Branches will be deleted from the main repository, regardless of whether it is a direct branch or a forked branch, after each release. The goal for each release is to clean up the repository and start fresh for development of the next release.

## Branch naming

Branches should be named according to the following convention:

`{type}/{issue}-{description}`

- type → feature, bugfix, docs
- issue → GitHub issue no, eg. GH-238
- Description → “fix-gene-static”

  - The description should be kept under 30 characters and delimited with hyphens
