### Issue Title: Open Tendermint Ports gateway-proxy Kubernetes Service
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
Open tendermint port in the gateway-proxy service for pocket nodes.
### Key Goals Of Issue
- Allow inbound peers to peer with PNI's Pocket nodes
#### Project
[Project](../../network_fix.md)  
#### Estimated Timeline  
1 day
  
- [X] Timeline `DOES` correspond with the Project Estimated Timeline  
- [ ] Timeline is `DOES NOT` correspond with the Project Estimated Timeline  
  
If timeline is `DOES NOT` correspond with the Project Estimated Timeline, please describe in detail the reasons below:  
[Detailed Description of Timeline Change]  
#### How to test functionality?  
When querying the `http://[host]:[tendermint-port]/net_info` endpoint, at least one `"is_outbound: true"` should be found in the output.
  
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

After the `gateway-proxy` service was uptaded with the missing ports, checks were run using a pod in the `mainnet` namespace. The results were satisfactory after the amount of inbound peers went from 0 to 50, which is the maximun allowed.

#### Delivery Date  
02/8/2021
### General Notes  
