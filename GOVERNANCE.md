# Flyte Governance 

This document defines the governance structure for the Flyte project.

## Overview
Flyte, a graduated LF AI&Data Foundation project, is committed to building an open, inclusive, productive and self-governing open source community focused on building a scalable and resillient platform for Machine Learning and Data Processing workloads. This document aims to define how community should work together to achieve this goal.


## Community roles and path to maintainership:

The following table lists the roles we use within the Flyte community. The table describes:

- General responsibilities expected by individuals in each role
- Requirements necessary to join or stay in a given role
- How the role manifests in terms of permissions and privileges.


<table>
  <thead>
    <tr>
    <th>Role</th>
    <th>Responsibilities</th>
    <th>Requirements</th>
    <th>Privileges</th>
    <th>Scope</th>
    </tr>
  </thead>

  <tr>
    <td>Community participant</td>
    <td>Follow the LF AI & Data Foundation <a href="https://lfprojects.org/policies/code-of-conduct/">Code of Conduct</a></td>
    <td>None</td>
    <td>
        <p>Can submit PRs and issues</p>
        <p>Can join <a href="https://slack.flyte.org/">Flyte Slack workspace</a></p>
        <p>Can take part in community discussions</p>
    </td>
    <td>Github organization </td>
  </tr>  
  <tr>
    <td rowspan="2">Contributor</td>
    <td colspan="4"><i>Inherits from Community participant role</i></td>
  </tr>
  <tr>
    <td>
        
<p>Follow the project's contributing guide</p>   
    </td>
    <td>
    <p><b>One or several of the below:</p></b>
<p>Report and sometimes resolve issues</p>
<p>Occasionally submit PRs</p>
<p>Contribute to the documentation</p>
<p>Show up at meetings, takes notes</p>
<p>Answer questions from other community members</p>
<p>Submit feedback on issues and PRs</p>
<p>Test releases and patches and submit reviews</p>
<p>Run or helps run events</p>
<p>Promote the project in public</p>
    </td>
    <td>
        <p>Eligible to become flyteorg Organization Member</p>
        <p>May review, approve PRs (non-binding), and merge approved PRs.</p>
    </td>
   <td>Specific repository/repositories</td> 
  </tr>
<tr>
    <td rowspan="2">Maintainer</td>
    <td colspan="4"><i>Inherits from Contributor Role</i></td>
  </tr>
 
  <tr>
    <td>
        <p>Review and approve (binding) PRs</p>
        <p>Ensure contributions align with project goals and meet the project's quality standards</p>
        <p>Mentor new contributors</p>
    </td>
    <td>
        <p>Must be an existing contributor</p>
        <p>Highly experienced and active reviewer</p>
        <p>Demonstrates a broad knowledge of the project across multiple areas</p>
    </td>
    <td>
        <p>Can merge PRs</p>
        <p>May create branches</p>
        <p>May vote on RFCs (non-binding)</p>
        <p>Represent the project in public as a Maintainer</p>
    </td>
    <td>Specific repository/repositories</td> 
  </tr>

  <tr>
    <td rowspan="2">Steering Committee</td>
    <td colspan="4"><i>Inherits from Maintainer Role</i></td>
  </tr>
  <tr>
    <td>
        <p>Set priorities and roadmap for the project</p>
        <p>Mentor new contributors and maintainers</p>
        <p>Vote on governace, role, RFCs, and other project-wide changes</p>
    </td>
    <td>
        <p>Must be an existing maintainer</p>
        <p>Highly active maintainer and participant in multiple functional areas</p>
    </td>
    <td>
    <p>Org-wide permissions</p>
    <p>Binding vote on RFCs</p>
    <p>Represent the project in other communities and upstream organizations</p>
    <p>
    
  </td>

  <td>Github organization </td>
  
  </tr>
</table>

## Expanded description and processes

### **Community participant**
You do not need to be a member of the Flyte team to contribute. Anyone can help by using and talking about Flyte, participating in discussions, answering questions on Slack/Stack Overflow, opening issues, submitting PRs, etc. All of these are fantastic and welcome contributions to the project.

### **Contributor**
Contributors are those who make regular contributions to the project (documentation, code reviews, responding to issues, participation in proposal discussions, contributing code, etc.). 

#### **New contributor nomination and election process**

New contributors may be self-nominated or nominated by existing contributors by completing the following steps:

1. Submit [a new issue](https://github.com/flyteorg/community/issues/new?assignees=&labels=contributor-nomination&template=contributor-nomination.md&title=) to the `community` repo using the `contributor nomination` label
2. Assign current maintainers to the issue. If unsure, check [MAINTAINERS.md](https://github.com/flyteorg/community/blob/main/MAINTAINERS.md)
3. Once submitted, new contributors must be elected by a [supermajority](#supermajority) of that project’s (repository) maintainers in no more than 14 days.
4. If a new contributor is accepted, they will receive an invitation to join the `flyteorg` Github organization, inheriting the permissions defined for the Contributor role in that repository or repositories.

### **Maintainers**
Maintainers are in charge of the day to day maintenance of the team's projects.

They review and approve (binding) PRs, merge PRs, and may cast non-binding votes on RFCs, ensuring contributions align with project goals and meet the project's quality standards.

#### **New maintainer nomination and election process**
New maintainers must already be contributors and can only be nominated by an existing maintainer by completing the following steps:

1. Submit a [new issue](https://github.com/flyteorg/community/issues/new?assignees=&labels=maintainer-nomination&template=new-maintainer-nomination.md&title=) to the `community` repo using the `maintainer-nomination` label
2. Assign current maintainers to the issue. If unsure, check [MAINTAINERS.md](https://github.com/flyteorg/community/blob/main/MAINTAINERS.md)
3. Once submitted, new maintainers must be elected by a [supermajority](#supermajority) of that project’s (repository) maintainers in no more than 14 days.
4. If a new maintainers is accepted, they will receive an invitation to join the `flyteorg` Github organization, inheriting the permissions defined for the maintainer role in that repository or repositories.

#### Additional notes
- Maintainers can be removed by a supermajority of the current team's maintainers or can resign by notifying one of the current team's maintainers.

- In extenuating circumstances, i.e. long term absence of a maintainer, technical steering committee members may act as maintainers.

### **Technical Steering Committee**

The Steering Committee Members are responsible for the direction of the project (roadmap), and cross-cutting concerns such as:
- Reviewing and deciding on new sub-projects to add to Flyte
- Create Special Interest Groups or Working Groups to focus on cross-project technical issues and requirements
- Voting on role changes (eg adding new Steering Committee member)
- Voting on updating this document
- Voting on RFCs that impact any of the above responsibilities.

## Stepping Down/Emeritus Process
If and when contributors' commitment levels change, contributors can consider stepping down (moving down the contributor ladder) vs moving to emeritus status (completely stepping away from the project).

Contact the Maintainers about changing to Emeritus status, or reducing your contributor level.
_______
**NOTE:** The current list of maintainers and TSC members lives in [MAINTAINERS](MAINTAINERS.md)
____
## Definitions

### Supermajority
A supermajority is defined as two-thirds of members in the group (66%). A supermajority of Maintainers is required for certain decisions as outlined above. Voting on decisions can happen on the mailing list, GitHub, Slack, email, or via a voting service, when appropriate. Maintainers can either vote "agree, yes, +1", "disagree, no, -1", or "abstain". A vote passes when supermajority is met. An abstain vote equals not voting at all.









