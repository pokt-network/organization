---
name: Validator hard disk usage Improvements
about: Improving validator hdd usage
title: "Milestone Rank Vote Proposal: Validator hard disk usage Improvements"
labels: Proposal
assignees: 'Otto Vargas'
---
### Proposal Title
Validator hard disk usage Improvements
### Date(s)
01/08/2021
### Category
- [ ] Infrastructure
- [X] Protocol/Blockchain Dev
- [ ] App Solutions
- [ ] Quality Assurance
### Contract
- [ ] This process follows the Milestone Rank Vote Framework as discussed in the Pocket Network Corporation's `Organization Handbook`
- [X] This process `DOES NOT` follow the Milestone Rank Vote Framework as discussed in the Pocket Network Corporation's `Organization Handbook`

If `DOES NOT` follow the Handbook's Milestone Rank Vote Framework, please describe in detail why below:

Framework not yet finished.

## Description of Proposal
### Background

Our Blockchain size at the time of writing is about 14.5Gb, this data is used by seed nodes, full nodes and validators.
In our latest update we updated to a newer version of tendermint that support a "Block Retention strategy", 
meaning that to run a node you could select to keep just a fraction of the blocks and greatly reduce the size of the downloaded chain in your machine.

### Goal
The goal of this proposal is to define a "Retention Strategy" that suit pocket network and clearly define the specifics of this strategy for each node type:
Full node, Validator, Seed.

For All Nodes this means that the amount of Hdd needed to run will depend on the strategy selected as default, that's why this proposal plans to add multiple "pre-configured" running profiles
to ease the running of each type of node.

Ex: 
- running with validator profile : block retention = last 3,000 blocks , inbound peers = 10 , outbound peers = 10
- running with full node profile : block retention = all blocks , inbound peers = 300 , outbound peers = 300
- running with seed profile : block retention = last 8,000 blocks , inbound peers = 100 , outbound peers = 100

Hdd usage estimated : 
- validator 2.8 Gb
- full node 14.5 Gb 
- seed 7.5 Gb


 _Definitive block retention not defined yet._

### Estimated completion time
3 weeks