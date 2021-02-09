### Certification Documentation For Milestone: Network Fix  
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

### LEVEL
- [ ] RC
- [X] STABLE

## Certification
### Summary
**How is this deliverable certified?**

- Checked all nodes (seeds, validators and betas) for inbound peers using their respective `/net_info` endpoint.
- Set up local node and used the `--persistent_peers` flag pointing to one of PNI's nodes.

**Certification Contract**

- [X] The certification of this deliverable ensures Stability Level as described in the handbook

**Justification Statement**

After the `gateway-proxy` was uptaded, a check was run using a pod in the `mainnet` namespace. The results were satisfactory after the amount of inbound peers went from 0 to 50, which is the maximun allowed and PNI's nodes were in the list of peers of the tested nodes.

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
 - Status: [PASSED]
### General Notes  
