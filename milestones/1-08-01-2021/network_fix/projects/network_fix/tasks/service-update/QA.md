### QA Documentation For Open Tendermint Ports gateway-proxy Kubernetes Service
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

After updating the `gateway-proxy` service, I proceeded to exec into the "unjail" pod that lives in the `mainnet` namespace of the PNI's kubernetes cluster. Installed curl and ran the commands specified in the QA strategy docunment, to check if every node had inbound peers connected to them.

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

After the `gateway-proxy` was uptaded, I ran check using the a pod in the `mainnet` namespace. The results were satisfactory after the amount of inbound peers went from 0 to 50, which is the maximun allowed.

### Alternatives Considered
**Alternative Approach 1**

Look through each node's logs and find the line with the peers information.

**Pros**
- Do not have to access the cluster/container
- Do not need to know how kubernetes work and how to use `kubectl`

**Cons**
- Takes longer to go through all nodes to find this line


Explain in detail why the chosen option superior to this alternative:

The chosen approach is superior because a few lines of commands will save a lot of time when investigating the amount of inbound peer each node has.
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
- Search for inbound peers in `/net_info`
 - Status [PASSED]
- Set the `--persistent_peers` flag to a local (personal computer) node using node-19 address
 - Status [PASSED]

### General Notes  
  
