### QA Strategy For Issue: Set PNI's Nodes as Persistent Peers to all Nodes in Cluster
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

## QA Strategy
### Summary

**What is the strategy?**

Find in the `/net_info` endpoint a list of `*.pokt.network` peers. This can be done by issuing the following command inside a container running in the `mainnet` namespace of the `pocket-system-mainnet` Kuberentes cluster in GCP and with curl previously installed: 
```
Validators
for i in $(seq 1 20); do  echo node$i; curl -s pocket-core-$i:26657/net_info | grep pokt.network:; done 
Seeds
for i in $(seq 1 10); do  echo seed$i; curl -s pocket-core-seed$i:26657/net_info | grep pokt.network:; done
Betas
for i in $(seq 1 5); do  echo beta$i; curl -s pocket-core-beta$i:26657/net_info | grep pokt.network:; done
```
**Why this strategy?**

The only way to get the peers that are conneted to the node is by calling the `/net_info` endpoint. The goal is to show that the other PNI's nodes are present in the address book.

**QA Contract**

- [X] The QA strategy `WILL` ensure delivery of the intended purpose

**Justification Statement**

After the `gateway-proxy` was uptaded, I ran check using the a pod in the `mainnet` namespace. The results were satisfactory after other PNI nodes were found in the list of peers of the tested nodes.

### Participant Quorum
- [X] `UNANIMOUS`
- [ ] `SPLIT`

If decision was `SPLIT`, please provide those who were for and against the strategy:
- Participant 1: FOR
- Participant 2: AGAINST

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

### General Notes  

