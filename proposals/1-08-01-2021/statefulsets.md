---
name: StatefulSet
about: Change PNI's nodes kubernetes controller from deployments to statefulsets
title: "Milestone Rank Vote Proposal: StatefulSets"
labels: Proposal
assignees: 'Julio Jimenez'
---
### Proposal Title 
StatefulSets
### Date(s)
07/01/2021
### Category
- [x] Infrastructure
- [ ] Protocol/Blockchain Dev
- [ ] App Solutions
- [ ] Quality Assurance
### Contract
- [x] This process follows the Milestone Rank Vote Framework as discussed in the Pocket Network Corporation's `Organization Handbook`
- [ ] This process `DOES NOT` follow the Milestone Rank Vote Framework as discussed in the Pocket Network Corporation's `Organization Handbook`

If `DOES NOT` follow the Handbook's Milestone Rank Vote Framework, please describe in detail why below:

## Description of Proposal
### Background
In kubernetes a deployment is a resource to deploy a stateless application, if using a PVC, all replicas will be using the same Volume and none of it will have its own state and statefulsets are used for Stateful applications, each replica of the pod will have its own state, and will be using its own Volume.

Currently PNI's nodes are deployments which is not the right way to manage our nodes since pocket is a stateless application. 

PNI's nodes being managed as deployments has brought many issues in the past, thankfully we have been able to solve them but they could have been avoided by using StatefulSets.

### Goal
Add stability to PNI's nodes by switching from deployments to statefulsets.


### Estimated completion time
3 weeks

### Tasks
- Resctructure pocket-core-internal-deployment mainnet directory
- Set affinitty to pods
- Add health checks (liveness and readiness)
- Create new storage classes in different zones
- Update deployments to statefulsets
