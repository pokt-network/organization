### QA Documentation For Project: Network Fix
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

- Checked all nodes (seeds, validators and betas) for inbound peers using their respective `/net_info` endpoint.
- Set up local node and used the `--persistent_peers` flag pointing to one of PNI's nodes.

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

The chosen approach is superior because a few lines of commands will save a lot of time when obtaining the amount of inbound peer each node has. The chosen approach allows to get all the nodes peers, inbound and outbound in two commands while the alternative approach would require to check each nodes log one by one.
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
- Search for PNI's peers in `/net_info`
 - Status: PASSED
### General Notes  
  
