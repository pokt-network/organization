---
name: Infrastructure budget optimization 
about: Since the release of 0.5.1 until the release of 0.5.2.9 and during the growth of the network. We faced the need of spin up resouces to meet the demand of the network and correct functioning of the network. Today with the great work done by blockchain-dev and further analysis of our current infrastructure. We concluded that we can reduce optimize the infrastructure budget/usage 
 
title: "Infrastructure budget optimization"
labels: Infrastructure 
assignees: 'Lowell Abbott'

---

### Proposal Title 
Infrastructure budget optimization
### Date(s)
01/07/2021
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
We just identified various opportunities after and with the release of 0.5.2.9 which result in better resource management and will improve our savings. 
Preliminary analysis of the benefits of this proposal show us that we will be saving ~$2000-4500 monthly which will allow us to resume the integration for more blockchains and lower our infrastructure costs


Tasks to be done:

- Investigate the resources and opportunities for lowering our budget and estimate the savings 
- Create proxy access to connect blockchains from production cluster to testnet validators and  Delete testnet blockchains
- Investigate and resize pocket seed nodepool 


Output:
- $2000-4500 in savings in our current infrastructure
- Allow us to resume the integrations with other blockchains


### Estimated Timeline
1-2 week

**Evidence and Justification for this timeline:**
We need to perform a full study of the resources that we can optimize, including the ones that we already know from the preliminary study and to develop.

Also, we need to provide an internal proxy in order for the testnet validator access the blockchains in the prod cluster.

**Timeline Consultants**


 - Consultant 1: Lowell Abbott

### How to test functionality?
[Detailed description on how to test the milestone]

### Project Abstractions
- Project 1
https://github.com/orgs/pokt-network/projects/128

### QA Planification
A detailed comparison report about the expenses of the current seed node pool and the new one and another budget report of the nodepool related to the testnet cluster

### Community Buy In Evidence
Michael, Luis agreed in slack conversations

### Communication Plan
We will make an annoucement in the #infra channel, upon completion of this proposal

### General Notes
Doesn't apply

### External Links
Doesn't apply

### Executive Signoff
- [ ] APPROVED
- [ ] DECLINED

If `DECLINED`, please describe in detail why below:
