# Contributing

The file is home to contributing information for Informatics Operations (IO) at the Colorado Center for Personalized Medicine (CCPM), University of Colorado Anschutz Medical Campus.

# Source Code, Data, and Reproducibility

**Pride:** We expect lab members to sign their code, which means that source code contributions are attributable to an individual's account on GitHub.
To quote from _The Pragmatic Programmer_:

> Craftsmen of an earlier age were proud to sign their work.
> You should be, too…
> People should see your name on a piece of code and expect it to be solid, well written, tested, and documented.

While some code will be proof-of-concept code, it should be of a form that inspires confidence.

**Language:** We write code for our analyses in Python or R, which allows everyone in the lab to know two languages and understand analytical code.

**Version Control Services:** Our primary version control service is GitHub, and we have a [`CCPM-TIS` account](https://github.com/CCPM-TIS) there.
We expect that lab members will maintain their code in repositories under these team accounts.
However, lab member should not commit to the branch that is shown as default on GitHub for any of these repositories.
Instead commits happen as described below to facilitate code review.

**Getting Code into CCPM-TIS Repositories:** Code moves from user repositories to `CCPM-TIS` repositories through a process of code review.
Code review is handled through pull requests.
The process is described briefly below.
Feel free to ask for guidance if you are uncomfortable with the process.
**We will revoke write access for failing to adhere to these rules.**

1. Make changes to your code and commit them in your own repository first.
1. Create a pull request into the repository owned by CCPM-TIS.
1. Name potential reviewers for your pull request.
1. Once at least one lab member has approved your pull request, you or a reviewer may merge your pull request.
   The only exception to this policy is this repository ("IO") where, in addition to the above rules, IO director must also approve the pull request.

**Composition of Pull Requests:** Each pull request may contain one or more changesets.
In keeping with good source control practice, each changeset or commit should contain _all_ changes necessary for a particular fix or update.
In addition, each pull request should relate to no more than one functional area in the code base you are updating.
Keeping the pull request focused to one area makes it easier for your reviewers to provide thoughtful feedback.

**Reviewing Pull Requests:** We expect that all lab members will participate in review of pull requests.
If you get named by the submitter, it's courteous to review the request.
We have created a [checklist](https://github.com/CCPM-TIS/IO/blob/master/extras/code_review_checklist.md) to facilitate review.
As a reviewer, you are responsible for making sure that all checklist guidelines are followed.
