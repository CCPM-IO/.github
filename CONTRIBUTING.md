# Contributing

The file is home to contributing information for Informatics Operations (IO) at the Colorado Center for Personalized Medicine (CCPM), University of Colorado Anschutz Medical Campus.

## Source Code, Data, and Reproducibility

### Pride

We expect lab members to sign their code, which means that source code contributions are attributable to an individual's account on GitHub.
To quote from [_The Pragmatic Programmer_](https://www.oreilly.com/library/view/the-pragmatic-programmer/9780135956977/):

> \[Craftspeople\] of an earlier age were proud to sign their work.
> You should be, too…
> People should see your name on a piece of code and expect it to be solid, well written, tested, and documented.

While some code will be proof-of-concept code, it should be of a form that inspires confidence.

### Programming Languages

We most often write code for our analyses in Python or R.
This allows everyone in the lab to know two languages and understand analytical code.

### Version Control Services

Our primary version control service is GitHub.
We expect repository management and code maintenance to occur through our [`CCPM-TIS` GitHub organization](https://github.com/CCPM-TIS).
We discourage direct commits to the default branch (for example, `main` or `master`) for all repositories.
Changes to default repository branches occur through ["feature branches"](https://www.atlassian.com/git/tutorials/comparing-workflows/feature-branch-workflow) and [GitHub pull requests](https://docs.github.com/en/pull-requests/collaborating-with-pull-requests/proposing-changes-to-your-work-with-pull-requests/creating-a-pull-request) with related code review and merges after  approval.

### Development

#### Linting

A [linter](<https://en.wikipedia.org/wiki/Lint_(software)>) is a code analysis tool designed to analyze code and flag for programming errors, bugs and stylistic errors.
These tools allow one to drastically improve their productivity when writing code for their research projects as stylistic errors and programming errors will automatically be covered through this setup.

##### Pre-commit

We recommend the use of pre-commit with our repositories.
Using pre-commit allows you to setup a "git hook" which can check for errors prior to committing changes with git.
See [pre-commit installation documentation](https://pre-commit.com/#install) and individual repositories for their unique configurations and potential linting expectations.

### Updates to Code

We practice code review on all changes to repositories.
Code review is handled through [GitHub pull requests](https://docs.github.com/en/pull-requests/collaborating-with-pull-requests/proposing-changes-to-your-work-with-pull-requests/creating-a-pull-request).
The process is described briefly below.
Feel free to ask for guidance if you are uncomfortable with the process.

**⚠️ We will revoke write access for failing to adhere to these rules.**

1. Make changes to your code and commit them in a non-default branch.
1. Create a pull request into the repository owned by CCPM-TIS.
1. Select potential reviewers for your pull request.
1. Once at least one lab member has approved your pull request, you or a reviewer may merge your pull request.
   - There are sometimes exceptions to this policy where, in addition to the above rules, an IO director must also approve the pull request (for example, with the `.github` repository).

#### Composition of Pull Requests

Each pull request may contain one or more changes.
In keeping with good source control practice, each pull request should include all commits necessary to complete a particular fix or update.
In addition, each pull request should relate to no more than one functional area in the code base you are updating.
Keeping the pull request focused to one area makes it easier for your reviewers to provide thoughtful feedback.
We recommend keeping pull requests as small as feasible to address fixes or new capabilities.
Larger pull requests involving many lines changed and/or very complex changes may be a sign that further granularity (and smaller changes) would be beneficial.

#### Reviewing Pull Requests

We expect that lab members will participate in requested review of pull requests.
See the checklist below on how to facilitate code review.
As a reviewer, you are responsible for making sure that all checklist guidelines are followed.

### Code Review Checklist

- [ ] **Pride:** We expect lab members to sign their code via commits attributable to a user.
  Each commit must be attributed to a recognized user.

- [ ] **Licensing:** A LICENSE file is in the root of the repository.

- [ ] **Using Other Code:** Code taken from elsewhere is properly acknowledged and compatible with the license.

- [ ] **Style Guide:** Python code follows [PEP 8](https://www.python.org/dev/peps/pep-0008).
  R code follows [Google's R Style Guide](https://google.github.io/styleguide/Rguide.xml).
  We provide instructions on how to automate the linting process [here](linter_install_tutorial.md)

- [ ] **Variable and Function Names:** Variable names are descriptive and interpretable to someone looking at this code for the first time (e.g. not `a`, `b`, `x`, etc.).

- [ ] **File Commenting:** Each file has a comment at the top to broadly describe its function and how it is expected to be used (e.g. imported, run from command line, both).

- [ ] **Function Comments:** Each function has a docstring which reports the computation that it intends to implement, its arguments, and its return value(s).

- [ ] **In-line Commenting:** At least 2 spaces are placed between in-line comments (`#`) and source code.

- [ ] **Imports:** All trivial imports are at the top of the file.

- [ ] **Column Length:** The code should be readable in a text editor with a reasonable format as well as the GitHub interface.
  This means that there are no excessively long lines.
  We strongly recommend that repository maintainers select a maximum line length for code of 80 or 100 characters and that this be specified in a contributors document for the repository.
  Plain text, markdown, and other text-based formats can alternatively be broken at sentences.
  This rule is already covered well in [PEP 8](https://www.python.org/dev/peps/pep-0008/#maximum-line-length) but called out here to clarify that we apply it to more than Python code.
  One reason for this is to aid in readability of `diff` output when performing code reviews.

- [ ] **Whitespace:** There is no unnecessary whitespace.

- [ ] **Code with constants** Any constants are specified at the beginning of the file.

- [ ] **Code that uses a random seed \[special case of constants\]** Code that uses a random seed is reproducible.
  This means that the seed can be set _and_ a default value is specified.

- [ ] **API error handling** APIs should catch and handle anticipated errors (e.g. key doesn't exist, type mismatch in lookup) by identifying the source of the error (e.g. lookup failed with PK=XYZ) to the caller with as much precision as possible.
