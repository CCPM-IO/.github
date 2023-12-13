# Security

The Colorado Center for Personalized Medicine - Informatics Operations (CCPM I/O) team and community take security bugs and vulnerabilities seriously.
We appreciate your efforts to responsibly disclose and, where necessary, remediate your findings when it comes to security issues.

General security incident procedures for projects found here are managed through the [University of Colorado's Office of Information Security incident report process](https://www.cu.edu/security/reporting-incident).
Please see that the linked materials for more detail on how to proceed.

We also follow a [University HIPAA Policy](https://research.cuanschutz.edu/regulatory-compliance/home/hipaa/university-hipaa-policy) regarding data used by some of our projects. Please use the following [special link for HIPAA related security incidents](https://research.cuanschutz.edu/regulatory-compliance/home/hipaa/hipaa-incident-reporting).

Besides the above, we require the following for projects:

- Private keys, passwords, and credentials must never be committed into source control.
- Data checked into source control must not include sensitive or personally identifiable information (PII).

### Github Copilot

CCPM I/O members are encouraged to use Github Copilot to help write code. However, this implies that code from a repository that deploys Github Copilot will be shared with the public internet. Thus, PII and any proprietary code cannot be included in any repository that uses Github Copilot. In addition, it is strongly discouraged to include file paths in your code. If you have doubts about what is considered proprietary, please consult with the I/O director. 
