# GitHub Repository Maintenance SOP

# Purpose

This document serves as the standard operating procedure (SOP) for any and all aspects of maintaining GitHub repositories within the CCPM I/O organization GitHub. Any question that you feel is not addressed here should be opened as an issue on the [CCPM I/O .github](https://github.com/CCPM-IO/.github/issues) repo following one of the issue templates, assigned to the [“CCPM SOP Development” project](https://github.com/orgs/CCPM-IO/projects/25), and assigned to a team member (who is not the director).

# Code of conduct

The CCPM I/O department follows a code of conduct that can be found [here](CODE\_OF\_CONDUCT.md).

# Security

Consult the [security document](SECURITY.md) for details regarding CCPM I/O security expectations.

# Accounts

Each member of the CCPM I/O is required to create an account so that all contributions will be attributable to each member, director included.

## Organizational roles

There is a single, [CCPM I/O organization account](https://github.com/ccpmio), managed by the director, that is used for the overall CCPM I/O GitHub organization management. This account has the highest level permissions and is primarily used to assign permissions to teams and members in the CCPM I/O GitHub organization. This account also has full admin control over creating, deleting, and maintaining all repositories under the CCPM I/O organization. The CCPM I/O account will be primarily managed by the director, but the management responsibility may be offloaded to any other CCPM I/O team member at the director’s discretion (or absence). The CCPM I/O organization account is distinct from the director’s personal account, that will be used for all repository contributions (issue creation, PRs approvals, etc.)

# Roles and responsibilities

|  **Task**                                                         |  **Responsible**                        |  **Accountable**                |  **Consulted**                          |  **Informed**    |  **Comments**                                                                                                                                                                                                                                                                       |
|:------------------------------------------------------------------|:----------------------------------------|:--------------------------------|:----------------------------------------|:-----------------|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Repository creation                                               | Primary repository maintainer           | Secondary repository maintainer | I/O team                                |                  | Internal members may add repos under the organization header after discussion with I/O team                                                                                                                                                                                         |
| Team creation and permission management for CCPM I/O organization | Director                                |                                 |                                         | I/O team         | The director is responsible for maintaining teams on GitHub and assigning roles and permissions to all individuals that have access to the CCPM I/O organization                                                                                                                    |
| Repository deprecation                                            | Director                                |                                 | I/O team                                |                  | Repositories will be selected for deprecation/archival on a yearly basis. Original maintainer will be informed unless they are no longer with the team.                                                                                                                             |
| Creating PRs                                                      | Issue assignee                          |                                 | Primary/Secondary repository maintainer | Director         | PRs should be created by the individual who addressed the issue that the PR is related to. I/O peers should be set as reviewers, director informed                                                                                                                                  |
| Milestone creation                                                | Primary repository maintainer           | Secondary repository maintainer | Director                                | I/O team         | The project lead is responsible for creating and maintaining milestones on their respective repositories. The director and other contributing members should be informed about what the milestone is intended to track and how it is to be used.                                    |
| Issue creation                                                    | I/O team member                         |                                 |                                         | I/O team         | Anyone in I/O may create issues and anyone following the repository will be informed                                                                                                                                                                                                |
| Project creation                                                  | I/O team member                         | Director                        |                                         |                  | Anyone in I/O may create a project, the director holds final judgment about keeping projects in the organization                                                                                                                                                                    |
| Epic creation                                                     | Primary/secondary repository maintainer |                                 | Director                                | I/O team         | Epic should be created by the primary and secondary maintainers of a repository. Director should be consulted to ensure epics align with project goals.                                                                                                                             |
| Creating releases                                                 | Primary repository maintainer           | Secondary repository maintainer | Director                                | I/O team         | The repository maintainer is responsible for releases in each respective repository. Secondary contributors to that repository will be accountable for releases. Director should be consulted prior to release, and the entire I/O team (and maybe external stakeholders) informed. |

## Repository creation

Generally anyone who is on the I/O team are permitted to create repositories under the CCPM I/O organization. However, it is required to have a discussion with the I/O team and be granted approval prior to creating a repository under the CCPM I/O organization GitHub. It is generally recommended to create a repository under your personal account first, then discuss with the I/O regarding moving it to the CCPM I/O GitHub. The CCPM I/O organization will be the ultimate owner and admin for all repositories contributed to by the I/O team as a whole.

### Naming

Repositories that will belong in the CCPM I/O organization should follow these naming conventions:

- All lowercase letters, save for acronyms (proper nouns, common abbreviations, etc.)
- Names of companies or organizations should follow their naming conventions
- No spaces are allowed in names
- If a name should contain multiple words, they should be delimited with hyphens (underscores and other delimiters are not allowed)
- Names should be kept to 20 characters or less, barring special circumstances to be approved on an ad-hoc basis by the I/O team

### Permissions

Permissions will be managed by the I/O director at the level of the organization using the tools created by GitHub for team management. Generally, anyone working on the I/O team may be granted permissions to any repository under the CCPM I/O organization by anyone with permissions to do so.

For individuals outside of the CCPM I/O team (eg. UCHealth, CU researchers, etc.), the director of I/O should be consulted prior to granting anyone permissions to repositories maintained by the CCPM I/O team. The director of I/O holds the final discretionary power to permit or deny permissions to any repository maintained by the CCPM I/O team. Requests for granting permissions to a repository may be made through email or slack. The director is responsible for creating teams on GitHub and assigning roles and permissions to all individuals that have access to the CCPM I/O organization.

The director is also responsible for revoking permissions to repositories or the CCPM I/O organization as a whole. By default, permission should be treated as a “need-to-know” basis. Permissions will be only be granted on an ad-hoc basis. For example, a contributor who solely needs to read a piece of documentation regarding a codebase may be sent a document, but not granted permissions to the repo as a whole. Using GitHub’s built in permission management tools, the director will maintain organization permissions as a whole.

Revocation causes:

- Leaving the CCPM - permissions will be immediately revoked and granted back on an ad-hoc basis
- Failing to follow the guidelines outlined in this document
- A guest that was granted temporary access

### Basic requirements

Repositories will follow a template outlined in the: [ccpm-template-repo](https://github.com/CCPM-IO/ccpm-template-repo). It is strongly advised to use this repository as a template for creating any repository that will be included under the CCPM I/O organization. Otherwise, all components will need to be created from scratch. Language specific frameworks will govern project structure on a more granular level (see [GitHub Repository Maintenance SOP](GitHub%20Repository%20Maintenance%20SOP.md)). However, each repository in the CCPM I/O organization will adhere to the following high-level template:

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

The CCPM I/O team as a whole will evaluate repositories on a yearly cadence, generally at the end of the calendar year. The CCPM I/O team will evaluate all repositories under the organization and archive those that are no longer being used. Rather than renaming and keeping repositories in an active state, they will be deprecated and archived so that information is retained, but does not clutter the organization repository list.

## Management

### General guidelines

- All repositories in the CCPM I/O organization will have branch protection rules for main, preventing direct merges or force pushes
- All pull requests (PRs) require at least one approval prior to merge
- Branch restrictions may be set in place on an ad-hoc basis for repositories with external stakeholders
- Use relative paths for links to documents inside repository, refrain from using absolute paths
- For forks

  - Org → personal repo, NEVER personal repo → org

### Releases

The CCPM I/O uses [Semantic Versioning (SemVer)](https://semver.org/), [GitHub flow](https://docs.github.com/en/get-started/using-github/github-flow) and [Release drafter](https://github.com/release-drafter/release-drafter) for versioning and release management. Repository releases, including new features, bug fixes, and other updates, are managed through Pull Requests (PRs) to the main branch. Each release involves determining the type of release (major, minor, or patch), creating a PR, testing the release, and deploying the code to the production environment. A new GitHub release will be tagged with the appropriate version number and will include all changes in the main branch up to the commits in the PR. This information is more thoroughly described in the CCPM I/O [RELEASE.md](https://github.com/CCPM-IO/cart/blob/main/resources/RELEASE.md).

High-Level Release Process:

1. Create a Pull Request (PR) for the release incorporating your changes.
2. Update the PR with test details and obtain approvals.
3. Merge the PR to the main branch.
4. Deploy the updated code to the production environment.

# Structure

The top level structure and overall architecture of each repository will follow the conventions outlined in the style guide for each respective project type. These will generally follow language or framework specific style guides. (TODO: Create list with links to each style guide here)

## Style guides

### Python

Python code follows [PEP 8](https://www.python.org/dev/peps/pep-0008). R code follows [Google's R Style Guide](https://google.github.io/styleguide/Rguide.xml). We provide instructions on how to automate the linting process [here](https://github.com/CCPM-IO/.github/blob/main/linter_install_tutorial.md).

### R

### Shell/bash

### Front-end web dev: HTML/Javascript/CSS

### Nextflow

### Sbatch (extension of shell/bash guidelines)

# Issues

Every repository in the CCPM I/O organization will use issues to track progress on projects. Every piece of development that is done for a project should be tracked through one or more issue(s). It is standard practice and always recommended to open an issue prior to making any changes to code. An issue may be opened retroactively after a branch has been created or code has been altered, but it is never acceptable to create a PR prior to creating the related issue. All issues will be addressed by PRs and therefore need to be opened prior to creating a merge/pull request.

## Issue templates

In general, issues will fall into one of three categories: bug, task, or feature. The CCPM I/O follows templates for each of these issue types:

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

All issues should be assigned to a project, orphan issues are not allowed. This is because the CCPM I/O team routinely tracks issues that are tied to multiple repositories. If an issue is created and does not have a relevant project to assign it to, it should be brought up during the internal I/O sync, so that one may be created.

### Milestone

Milestones will be used to track large features that contain multiple sub-tasks. Milestones are intended to be used to track serial steps during development. In other words, once completed, a milestone removes blockers before the next steps of a project can continue. Not every issue will be assigned to a milestone. Examples of things that do NOT require milestones are hotfixes, CI/CD changes, and documentation changes. Generally milestones WILL be utilized for things like releases, refactors, and major components of pre-release steps.

### Relationships

Issue relationships are not required to be assigned upon issue creation. However, they may be assigned some time after issue creation. Issues may be assigned to parent issues if they are related to the resolution of it. Generally the CCPM I/O team uses parent issues to track the progress of multiple tasks. Each issue should reflect the resolution of a single task. A task is the smallest unit of work that can be tested individually.

# PRs

In the CCPM I/O organization, we follow a [GitHub flow](https://docs.github.com/en/get-started/using-github/github-flow) for branching and pull request (PR) creation. CCPM I/O use a strategy of merging all PRs to main, then creating releases and tagged versions for production. Pull requests (PRs) will be used prior to merging any code to main branch of a repository.

## PR template

There is a PR template in the .github repository that will be propagated to every repository under the CCPM organization.

## PR guidelines

In general, one PR should close one issue. Each issue should contain a single task, the smallest unit of development that can be tested. A PR should be made to address each and every issue that is created. This generally means each PR will change a relatively small amount of code and will not be overly cumbersome to review. This may not always be the case for new features, and a reviewer always reserves the right to request a PR be split into multiple PRs.

A single PR may be used to resolve multiple issues if it is not possible to test each issue independently.

### Merge strategy

The CCPM I/O organization follows a squash merge strategy for merging code. More regarding the standard can be found in [GitHub’s documentation](https://graphite.dev/blog/pull-request-merge-strategy).

Commit messages for individual commits should follow [conventional commit guidelines](https://www.conventionalcommits.org/en/v1.0.0/). Eg. `<type>[optional scope]: <description>`. This is a helpful VSCode [extention](https://marketplace.visualstudio.com/items?itemName=vivaxy.vscode-conventional-commits).

After approval has been given by all requested reviewers, the PR creator or repository maintainer may merge a PR into the main branch.

### Title

PR titles will follow the conventional commit message syntax, `<type>[optional scope]: <description>`. The CCPM I/O organization uses conventional commit messages and squash-merge for creating PRs, so the PR titles should follow this format. More about conventional commits can be found later in this section.

### Description

Descriptions should follow the format outlined in the [GitHub Repository Maintenance SOP](GitHub%20Repository%20Maintenance%20SOP.md) in this section. In general, descriptions should be a thorough and detailed explanation of what changes were made, and why they’re relevant. They should always include a link to the issue it is addressing and how the PR resolves it. [GitHub convention](https://docs.github.com/en/issues/tracking-your-work-with-issues/using-issues/linking-a-pull-request-to-an-issue) should be followed to ensure PRs close issues.

### Reviewers

PRs require at least one reviewer’s approval, and will generally be the secondary maintainer for that repository. In special circumstances, additional reviewers may be needed as well as director approval, but this is not the standard practice.

It is expected that reviews will occur in no more than three business days after assignment. If a review cannot be completed in three business days, a comment should be made regarding expected timelines for review. Reviews should be constructive and address specific issues if they exist.

If a reviewer feels that a PR contains too many changes, they always reserve the right to request the PR be split into more than one.

### Assignees

This should always be the creator.

### Labels

This will follow the same set of labels described in the [GitHub Repository Maintenance SOP](GitHub%20Repository%20Maintenance%20SOP.md) of this document. PR labels should match the issue they address.

### Projects

All PRs should be assigned to the same project that the issue originated from.

### Milestones

All PRs should be assigned to the milestone that the issue it’s addressing is assigned to (if applicable).

### Development

This section should be automatically filled in when linking a related issue in the PR description.

# Contribution

## Signatures

CCPM I/O expect team members to sign their code, which means that source code contributions are attributable to an individual's account on GitHub. To quote from The Pragmatic Programmer:

> [Craftspeople] of an earlier age were proud to sign their work. You should be, too… People should see your name on a piece of code and expect it to be solid, well written, tested, and documented.

While some code will be proof-of-concept code, it should be of a form that inspires confidence.

## Languages

The CCPM I/O team most often write code for our analyses in Python or R. This allows everyone in the organization to know two languages and understand analytical code.

## Linting

A [linter](https://en.wikipedia.org/wiki/Lint_(software)) is a code analysis tool designed to analyze code and flag for programming errors, bugs and stylistic errors. These tools allow one to drastically improve their productivity when writing code for their research projects as stylistic errors and programming errors will automatically be covered through this setup.

## Pre-commit

CCPM I/O recommends the use of pre-commit with our repositories. Using pre-commit allows users to setup a "git hook" which can check for errors prior to committing changes with git. See [pre-commit installation documentation](https://pre-commit.com/#install) and individual repositories for their unique configurations and potential linting expectations.

## Citing external code

Code taken from elsewhere is properly acknowledged and compatible with the license.

## Branching vs. Forking

For contributing code to a repository, there are two main strategies, cloning the repository and creating branches or forking the repository, creating branches, and creating PRs from the forked repository to the main repository. At the CCPM I/O, we use both conventions depending on the project type. Generally, it is up to the personal preference of the developer which strategy to use, either is okay. However, some work will necessitate using one strategy over the other.

### Branching

Several of the CCPM I/O maintained repositories have GitHub workflows, which use GitHub secrets defined in our CCPM repository. Pull requests from forked repositories are not given access to GitHub secrets. In this instance, branches must be made directly on the main repository.

### Forking

Forks are necessitated in repositories where the CCPM I/O develops GitHub workflows themselves. Changes could not be made and compared against the main repository since the changes are what dictate the tests (GitHub actions).

## Branch deletion

Branches will be deleted from the main repository, regardless of whether it is a direct branch or a forked branch, after each release. The goal for each release is to clean up the repository and start fresh for development of the next release.

## Branch naming

Branches should be named according to the following convention:

`{type}/{issue}-{description}`

- type → feature, bugfix, docs
- issue → GitHub issue no, eg. GH-238
- Description → “fix-gene-static”

  - The description should be kept under 30 characters and delimited with hyphens
