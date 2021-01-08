---
name: PocketJS Amino to ProtoBuf.
about: Actually the pocket-js library is using AminoJS to encode sending transactions and decode responses from the network, this library is a headache for both the blockchain and app solutions team to work on, for the same reason the blockchain development team is aiming to improve the overall flow by replacing Amino for ProtoBuf.

title: "PocketJS Amino to ProtoBuf"
labels: App Solutions, Gateway
assignees: "Pabel de Jesus"
---

### Proposal Title
PocketJS Amino to ProtoBuf
### Estimated time of execution
Three weeks
### Resources
- [2] Team member(s)
- [100%] Bandwidth
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
The team will release a new pocket-js version (0.7.0-rc) that will include the new dependency change from AminoJS to ProtoBuf, this change will improve the overall communication with the network ina a low level, allowing us to also maintain the impacted sections accordingly. Issues introduced during the implementation and explicitly high priority requests will be fixed.

### Estimated Timeline
Three weeks

**Evidence and Justification for this timeline:**

- Two weeks of Analysis and Development
- One week of testing.
The change will break main functionalities of the PocketJS library, due to the high importance of the changes needed, the team will provide a robust new version and new tests.

**Timeline Consultants**

[Name:Support]
 - Consultant 1: Blockchain Dev Consultant
### How to test functionality?
To properly test the changes we are going to perform a full regression testing of every feature related to sending/receiving a transaction while communicating with the network.
### Project Abstractions
- [Project 1](https://github.com/orgs/pokt-network/projects/130)

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
