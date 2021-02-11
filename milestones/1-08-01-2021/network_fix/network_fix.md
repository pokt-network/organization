### Milestone Title: Network Fix
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
- [X] This process follows the Milestone Framework as discussed in the Pocket Network Corporation's `Organization Handbook`  
- [ ] This process `DOES NOT` follow the Milestone Framework as discussed in the Pocket Network Corporation's `Organization Handbook`  
  
If `DOES NOT` follow the Handbook's Milestone Framework, please describe in detail why below:  
## Original Proposal  
[Original milestone proposal](https://github.com/pokt-network/organization/blob/main/proposals/1-08-01-2021/network-fix.md)
### Detailed Summary of Proposal  
Fix networking issue affecting PNI's nodes where nodes are not peering with inbound peers, only outbound.
### Milestone Goals
- Allow inbound peers to connect to PNI's nodes
### Proposal Estimated Timeline  
2 weeks  
### How to test functionality?  
Verify if in the output of the `http://[host]:[tendermint-port]/net_info` endpoint, at least one `"is_outbound: true"` is found.
## Rank Vote  
[Rank vote](https://docs.google.com/spreadsheets/d/1_MnAyzj-tg1hmcBuqM-SUvMzN_eMUl9EcoG0i7Dj9og/edit?usp=sharing)
### Contract   
- [X] This Milestone `IS` signaled priority by the Rank Vote system  
- [ ] This Milestone `IS NOT` signaled priority by PNI's Rank Vote system  
  
If `IS NOT` signaled priority by PNI's Rank Vote system, describe in detail why this milestone is being executed:  
[Details of why the milestone is being executed against the signaling of the Rank Vote]  
## Milestone  
### Plan  
#### Estimated Timeline  
2 week  
  
- [ ] Timeline is `THE SAME` as the Original Proposal Estimated Timeline  
- [X] Timeline is `NOT THE SAME` as the Original Proposal Estimated Timeline  
  
If is `NOT THE SAME` as the Original Proposal Estimated Timeline, please describe in detail the change in timeline below:  
[Detailed Description of Timeline Change]  

#### Projects  
**List**  
  
- [Network Fix](./projects/network_fix/network_fix.md)  
  
##### Network Fix
**Summary**  
  
This project's goal is to allow inbound peers to connect to PNI's nodes. The issue is a networking one, especifically at the edge.
Also, in order to make sure PNI's nodes will peer with each other, we set every node in the cluster as persistent peer to each other. Since we are only allowing a limited amount of peers to connect to PNI's nodes, sometimes those spots feel up quickly and if another PNI's node fails and needs to peer and sync, it won't be able to sync. 
  
**Leader**  
  
Julio Jimenez: Specialist
  
**Project Plan Documentation**  
  
[Network Fix](./projects/network_fix/network_fix.md)  
  
**Project Notes**  
  
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

- [X] The QA completed for this Milestone `DOES` ensure delivery of the Milestone purpose

**Justification Statement**

After the `gateway-proxy` service was uptaded with the missing ports, checks were run using a pod in the `mainnet` namespace. The results were satisfactory after the amount of inbound peers went from 0 to 50, which is the maximun allowed and PNI nodes were present in the peers list.

#### Certification Documentation  
[Link to Certification Documentation]  
  

#### Delivery Date  
02/8/2021
