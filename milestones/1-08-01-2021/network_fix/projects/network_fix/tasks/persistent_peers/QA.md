### QA Documentation For Set PNI's Nodes as Persistent Peers to all Nodes in Cluster
### Leader  
Julio Jimenez: Specialist
### Date(s)  
02/8/2021
### Participants
- Julio Jimenez: Specialist
## Survey
### Category
- [X] Infrastructure  
- [ ] Protocol/Blockchain Dev  
- [ ] App Solutions  

### Implementation (Check All That Apply)
- [ ] Unit Tests
- [ ] Integration Tests
- [X] Functional Tests
- [ ] Behavior Tests
- [ ] Load Tests
- [ ] Stress Tests
- [ ] Simulations
- [ ] Certification
- [ ] Benchmarks
- [ ] Performance Tests
- [ ] Resource Monitoring
- [ ] [ADD OTHERS]

## QA
### Summary

**How is this deliverable Quality Assured?**

After updating the `gateway-proxy` service, I proceeded to exec into the "unjail" pod that lives in the `mainnet` namespace of the PNI's kubernetes cluster. Installed curl and ran the commands specified in the QA strategy docunment, to check if every node had PNI peers connected to them.

**What was the original strategy?**

[Link to the QA Strategy document]

**Did the QA methodology follow the original strategy?**
- [X] `YES`
- [ ] `NO`

If the QA methodology diverged from the original QA strategy, please explain in detail why:

[Provied Detailed explanation]

**QA Contract**

- [X] The QA for this deliverable ensures delivery of the project purpose

**Justification Statement**

By using this approach the tester will be able to confirm that other PNI's nodes are peering with the node being tested.

### Tools Required
**Tool 1**

curl

**Link**

https://curl.se

**Planned Usage**

This tool will be used to make requests to PNI's pocket nodes to get the node's network information.

**Tool 2**

Kubectl

**Link**

https://kubectl.docs.kubernetes.io

**Planned Usage**

This tool allows the user to interact with the kubernetes cluster.

## Results
### Test Execution Data
[If Applicable: Any evidence, generated data, supporting details]
### Cases Tested
- Search for PNI's peers in `/net_info`
 - Status: PASSED

### General Notes  

