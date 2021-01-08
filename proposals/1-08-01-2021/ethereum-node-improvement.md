---
name: Ethereum node improvement 
about: We currently have issues with the perfomance of the ethereum node. Sometimes the blockchain height is behind the network and it stucks with long running requests 
 
title: "Ethereum node improvement"
labels: Infrastructure 
assignees: 'Lowell Abbott'
---

### Proposal Title 
Ethereum node improvement

### Date(s)
01/08/2021
### Category
- [x] Infrastructure
- [ ] Protocol/Blockchain Dev
- [ ] App Solutions
- [ ] Quality Assurance
### Contract
- [x] This process follows the Milestone Rank Vote Framework as discussed in the Pocket Network Corporation's `Organization Handbook`
- [ ] This process `DOES NOT` follow the Milestone Rank Vote Framework as discussed in the Pocket Network Corporation's `Organization Handbook`

If `DOES NOT` follow the Handbook's Milestone Rank Vote Framework, please describe in detail why below:

### Description of Proposal
We are currently facing perfomance issues with our ethereum full node. We think is better to change the client but this requires time to investigate and sync in order to switch with the current ethereum full node. 

Tasks to be done:

- Investigate which is the best ethereum client to replace our current ethereum node 
- Spin up the node and wait for sync
- Replace the node

Output:
- A little of budget savings 
- High perfomant ethereum request and up-to-date block height 


Link to the project:

### Estimated Timeline
1-2 weeks

**Evidence and Justification for this timeline:**
The estimation is based in the investigation and correct deployment of the ethereum node.

This time doesn't include the sync time needed in order to have the ethereum node ready to receive connections

**Timeline Consultants**

- Consultant 1: Lowell Abbott

### How to test functionality?
Ethereum node should be up and running and should not delay in block height while in peak traffic

### Project Abstractions
- Project 1
https://github.com/orgs/pokt-network/projects/125

### QA Planification

[1] The ethereum node should be up and running
[2] The ethereum node should not be behind in blockheight  while in peak traffic time of the day
[3] The ethereum node should return long requests in time

### Community Buy In Evidence
[Links, quotes, evidence to support this proposal]
### Communication Plan
[How will this milestone be communicated? Describe in detail]

### General Notes
This proposal will incur in more infrastructure costs, because we will be running this additional ethereun node with the better proposed cli that will replace our existing one 

### External Links
[If applicable]
### Executive Signoff
- [ ] APPROVED
- [ ] DECLINED

If `DECLINED`, please describe in detail why below:
