---
name: Gateway Stability Effort.
about: In the last couple of weeks it has taken to our attention that the Gateway is failing to deliver an stable service, the management of the nodes is not filtering properly success and fail scenarios.

title: "Gateway Stability Effort"
labels: App Solutions, Gateway
assignees: "Pabel de Jesus"
---

### Proposal Title
Gateway Stability Effort
### Estimated time of execution
Three weeks
### Resources
- [1] Team member(s)
- [50%] Bandwidth
### Category
- [ ] Infrastructure
- [ ] Protocol/Blockchain Dev
- [x] App Solutions
- [ ] Quality Assurance
### Contract
- [x] This process follows the Milestone Rank Vote Framework as discussed in the Pocket Network Corporation's `Organization Handbook`
- [ ] This process `DOES NOT` follow the Milestone Rank Vote Framework as discussed in the Pocket Network Corporation's `Organization Handbook`

If `DOES NOT` follow the Handbook's Milestone Rank Vote Framework, please describe in detail why below:
## Proposal
### Detailed Summary of Proposal
The team analized the Gateway actual code/implementation and noticed that the cherry picking module which manages the nodes used for every request can be improved to increase the success rate of the service. The result will increase the traffic going thru the Gateway.
### Estimated Timeline
Three weeks

**Evidence and Justification for this timeline:**

- Two weeks of Analysis and Development
- One week of testing.
Since the Gateway cherry picking module is tether to the whole system in a full process effort, the whole justification goes down to assure the proper implementation of the change.

**Timeline Consultants**

[Name:Support]
 - Consultant 1: Blockchain Dev Consultant
 - Consultant 2: Infra Dev Consultant
### How to test functionality?
To properly test the changes we are going to do multiple scenarios for the success rate to accurately fail-safe to other working nodes in the network if the one(s) being used are failing for x reason.

### Project Abstractions
- [Project 1](https://github.com/orgs/pokt-network/projects/129)

### QA Planification
The last week of the milestone the QA team will be testing a code-freeze version of the new deployment, doing regression testing to assure stability.
### Community Buy In Evidence
Private
### Communication Plan
Discord

### General Notes

### External Links

### Executive Signoff
- [ ] APPROVED
- [ ] DECLINED

If `DECLINED`, please describe in detail why below:
