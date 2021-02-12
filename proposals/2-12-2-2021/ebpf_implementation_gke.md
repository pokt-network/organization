---
name: BPF implementation in GKE.
about: Implementing Cilium and Falco BPF solutions in our GKE cluster.
title: "Milestone Rank Vote Proposal: eBPF Implementation"
labels: Proposal
assignees: 'Nelson Colon'
---

### Proposal Title
BPF implementation in GKE.
### Category
- [x] Infrastructure
- [ ] Protocol/Blockchain Dev
- [ ] App Solutions
- [ ] Quality Assurance
### Contract
- [x] This process follows the Milestone Rank Vote Framework as discussed in the Pocket Network Corporation's `Organization Handbook`
- [ ] This process `DOES NOT` follow the Milestone Rank Vote Framework as discussed in the Pocket Network Corporation's `Organization Handbook`

## Description of Proposal
### Background
Monitoring and security need to improve in the cluster facing towards the future of Pocket. Cilium and Falco can build into what we already have to create alarms and notifications more flexible, adaptables and useful for us and the whole team.

### Goal
Implement Falco and Cilium into the GKE cluster of nodes to improve monitoring and security inside the pods.

### Estimated completion time
4 weeks

### Tasks
- Install Cilium and Falco pods in the testnet GKE.
- Do QA and develop rules and alarms for cluster.
- Migrate configuration to mainnet GKE.