---
name: Autohealer for node runners 
about: Autohealer tool for solving issues like autounjailing and specific alarms that runs along pocket nodes
 
title: "Autohealer for node runners"
labels: Infrastructure 
assignees: 'Lowell Abbott'
---

### Proposal Title 
Autohealer for node runners

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
Many node runnners get jailed by sevice unavailability, node unsync and other issues and when the node user realizes his server is jailed. A significant amount of opportunity time has passed. Which  translates it to not generating POKT.

We thought about a tool that can auto-unjail node when the node is fully synced and reachable over the internet 

Tasks to be done:

- Investigate the best security wise and non invasive way of doing autounjailing running along pocket core 

Output:
- Stable node growth and happy node runners 


Link to the project:

### Estimated Timeline
2-3 weeks

**Evidence and Justification for this timeline:**
We will require time to investigate, code/the best less invasive way for coding and deploying this artifact along with pocket-core

**Timeline Consultants**

- Consultant 1: Lowell Abbott

### How to test functionality?
A node should be able to be unjailed if its jailed and synced on the latest block height

### Project Abstractions

### QA Planification

[1] The autohealer tool should unjail if the pocket node its on the latest node sync 
[2] The autohealer before unjail shoud check if node is on latest block height and its service is reachable and healthy 

### Community Buy In Evidence
In isolated conversations and in node hours talks a similar solution was discussed 

### Communication Plan
Via discord channel 

### General Notes

### External Links

### Executive Signoff
- [ ] APPROVED
- [ ] DECLINED

If `DECLINED`, please describe in detail why below:
