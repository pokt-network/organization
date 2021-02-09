### Issue Title: Set PNI's Nodes as Persistent Peers 
### Leader  
Julio Jimenez: Specialist  
### Date(s)  
02/8/2021  
### Category  
- [X] Infrastructure  
- [ ] Protocol/Blockchain Dev  
- [ ] App Solutions  
- [ ] Quality Assurance
### Survey
- [X] Issue originally created by PNI Member
- [ ] Issue originally created by outside contributor
### Contract  
- [X] This process follows the Issue Framework as discussed in the Pocket Network Corporation's `Organization Handbook`  
- [ ] This process `DOES NOT` follow the Issue Framework as discussed in the Pocket Network Corporation's `Organization Handbook`  
  
If `DOES NOT` follow the Handbook's Issue Framework, please describe in detail why below:  
### Issue Purpose
In order to make sure PNI's nodes will peer with each other, we set every node in the cluster as persistent peer to each other. Since we are only allowing a limited amount of peers to connect to PNI's nodes, sometimes those spots feel up quickly and if another PNI's node fails and needs to peer and sync, it won't be able to sync. 
### Key Goals Of Issue
- Make sure PNI's nodes will always be able to peer to other nodes
#### Project
[Project](../../network_fix.md) 
#### Estimated Timeline  
1 day
  
- [X] Timeline `DOES` correspond with the Project Estimated Timeline  
- [ ] Timeline is `DOES NOT` correspond with the Project Estimated Timeline  
  
If timeline is `DOES NOT` correspond with the Project Estimated Timeline, please describe in detail the reasons below:  
[Detailed Description of Timeline Change]  
#### How to test functionality?  
When querying the `http://[host]:[tendermint-port]/net_info` endpoint, other PNI's nodes should be present. Tester should access the bastion-vm in GCP. From there create a pod in the `mainnet` namespace, install curl if it's not already installed. Then, proceed to curl any of the nodes in the namespace. Eg: `curl pocket-core-1:26657/net_info`.
  
  
#### QA Documentation  
**QA Strategy Document**

[QA strategy](QA_strategy.md)

**QA Execution Document**

[QA document](QA.md)

- [X] The QA execution `DOES` follow the original QA Strategy document
- [ ] The QA execution `DOES NOT` follow the original QA Strategy document

If QA execution `DOES NOT` follow the original QA Strategy document, please explain why in fine detail:

[Explain the QA change in fine detail]

**QA Contract**

- [X] The QA completed for this issue `DOES` ensure delivery of the issue purpose

**Justification Statement**

After the `gateway-proxy` was uptaded, I ran check using the a pod in the `mainnet` namespace. The results were satisfactory after other PNI's nodes were found in the list of peers of the nodes tested.
  
#### Delivery Date  
02/8/2021
### General Notes  
