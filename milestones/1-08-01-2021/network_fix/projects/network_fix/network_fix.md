### Project Title: Network FIx 
### Leader  
Julio Jimenez: Specialist 
### Date(s)  
02/8/2021
### Category  
- [X] Infrastructure  
- [ ] Protocol/Blockchain Dev  
- [ ] App Solutions  
- [ ] Quality Assurance  
### Contract  
- [X] This process follows the Project Framework as discussed in the Pocket Network Corporation's `Organization Handbook`  
- [ ] This process `DOES NOT` follow the Project Framework as discussed in the Pocket Network Corporation's `Organization Handbook`  
  
If `DOES NOT` follow the Handbook's Project Framework, please describe in detail why below:  
### Project Purpose
Fix networking issue affecting PNI's nodes where nodes are not peering with inbound peers, only outbound.
### Key Goals Of Project
- Allow inbound peers to connect to PNI's nodes
#### Milestone
[Link to `Parent` Milestone Documentation]  
#### Estimated Timeline  
1 week 
  
- [X] Timeline `DOES` correspond with the Milestone Estimated Timeline  
- [ ] Timeline is `DOES NOT` correspond with the Milestone Estimated Timeline  
  
If timeline is `DOES NOT` correspond with the Milestone Estimated Timeline, please describe in detail the reasons below:  
[Detailed Description of Timeline Change]  
#### How to test functionality?  
Verify that each node can peer with inbound/external peers. Use `/net_info` endpoint to find peers connected to the node being tested. 
#### Issues  
**List**  
  
- [Set PNI's Nodes as Persistent Peers to all Nodes in Cluster](https://github.com/pokt-network/organization/issues/71)
- [Open Tendermint Ports gateway-proxy Kubernetes Service](https://github.com/pokt-network/organization/issues/70) 
  
##### Set PNI's Nodes as Persistent Peers to all Nodes in Cluster  
**Summary**  

This project's goal is to allow inbound peers to connect to PNI's nodes. The issue is a networking one, especifically at the edge.
Also, in order to make sure PNI's nodes will peer with each other, we set every node in the cluster as persistent peer to each other. Since we are only allowing a limited amount of peers to connect to PNI's nodes, sometimes those spots feel up quickly and if another PNI's node fails and needs to peer and sync, it won't be able to sync. 
  
**Leader**  
  
Julio Jimenez: Specialist
  
**Issue Documentation**  
  
[Issue documentation](./tasks/persistent_peers/persistent_peers.md)
  
**Issue Notes**  
  
  
##### Open Tendermint Ports gateway-proxy Kubernetes Service   
**Summary**  
  
In order to make sure PNI's nodes will peer with each other, we set every node in the cluster as persistent peer to each other. Since we are only allowing a limited amount of peers to connect to PNI's nodes, sometimes those spots feel up quickly and if another PNI's node fails and needs to peer and sync, it won't be able to sync. 
  
**Leader**  
  
Julio Jimenez: Specialist
  
**Issue Documentation**  
  
[Issue documentation](./tasks/service-update/service_update.md)
  
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

- [X] The QA completed for this project `DOES` ensure delivery of the project purpose

**Justification Statement**

After the `gateway-proxy` was uptaded, I ran check using the a pod in the `mainnet` namespace. The results were satisfactory after the amount of inbound peers went from 0 to 50, which is the maximun allowed.
  
#### Delivery Date  
02/8/2021
### General Notes    

### Lead Signoff

- [X] I Julio Jimenez: Specialist approve this project

- [ ] This project did not receive Milestone Lead signoff

If the project did not receive Milestone Lead signoff, please explain why in detail:

[Explain why there is no lead sign off]