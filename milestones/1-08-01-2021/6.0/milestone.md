### Milestone Title: RC-0.6.0
### Leader  
Andrew: CTO
### Date(s)  
01/13/2021
### Category  
- [ ] Infrastructure  
- [X] Protocol/Blockchain Dev  
- [ ] App Solutions  
- [ ] Quality Assurance  
### Contract  
- [X] This process follows the Milestone Framework as discussed in the Pocket Network Corporation's `Organization Handbook`  
- [ ] This process `DOES NOT` follow the Milestone Framework as discussed in the Pocket Network Corporation's `Organization Handbook`  
  
If `DOES NOT` follow the Handbook's Milestone Framework, please describe in detail why below:  
## Original Proposal  
https://github.com/pokt-network/organization/blob/main/proposals/1-08-01-2021/RC-0.6.0.md
## Detailed Summary
To frame RC-0.6.0 in a Rank Vote Proposal format, we first must understand the basics of RC-0.6.0 and its importance.

Here are the bullet points of how it improves both the software and the organization

Uses Protobuf encoding instead of amino. This improves both speed, resource consumption and (most importantly) inoperability between languages
Patches the Merkle Tree security hole (won't go into specifics, but a big flaw in the protocol that is exposed)
Contains an upgrade mechanism that can be modeled after in the future
NOTE: this milestone is near completion already, and for reasons explained in the 'contract' section, the details are glossed over 

NOTE: Due to the transition period into this process, the Milestone is already code complete. This milestone will focus it's goals accordingly.
### Milestone Goals
- Completely QA and Certify the completed 6.0 codebase
- Transfer the Pocket Core docs to Github and update it for 6.0
### Proposal Estimated Timeline  
1 Month
### How to test functionality?  
The software performs seamless network upgrades with the encoding change from amino to proto. 
It must maintain the legacy standard until the upgrade height.
The service must maintain every functionality prior to this upgrade.
It must at a minimum maintain the baseline resource consumption, if not improve on it.
## Rank Vote  
https://github.com/pokt-network/organization/tree/main/rank-votes/1-08-01-2021
### Contract   
- [X] This Milestone `IS` signaled priority by the Rank Vote system  
- [ ] This Milestone `IS NOT` signaled priority by PNI's Rank Vote system  
  
If `IS NOT` signaled priority by PNI's Rank Vote system, describe in detail why this milestone is being executed:  
## Milestone  
### Plan  
#### Estimated Timeline  
1 Month 
  
- [ ] Timeline is `THE SAME` as the Original Proposal Estimated Timeline  
- [ ] Timeline is `NOT THE SAME` as the Original Proposal Estimated Timeline  
  
If is `NOT THE SAME` as the Original Proposal Estimated Timeline, please describe in detail the change in timeline below:  
[Detailed Description of Timeline Change]  
#### Projects  
**List**  
- Functional Testing      // functionality testing / regression test *LUIS/EMAN*
- Unit Testing            // go tests *ANDREW*
- Upgrade Simulations     // sim *OTTO*
- Backwards Compatibility // prior protocol version compatibility *ED*
- Benchmark Testing       // resources *OTTO*
- Load Testing            // stress testing *LUIS*

- User guide  *ANDREW*
- Release Note / Changelog  *ANDREW*
- Architectural Documentation // Software specific implementation details *ANDREW*
- Reference Documentation     // CLI doc / RPC doc / Metrics *ED*
- Development Documentation   // Mocking software, code generation *ED*
  
##### [PROJECT 1 TITLE] // TODO!!
**Summary**  
  
[DETAILED SUMMARY OF PROJECT]  
  
**Leader**  
  
[NAME:TITLE]  
  
**Project Plan Documentation**  
  
[LINK TO PROJECT DOCS]  
  
**Project Notes**  
  
[Any notes on project 1]  
  
##### [PROJECT 2 TITLE]  
**Summary**  
  
[DETAILED SUMMARY OF PROJECT]  
  
**Leader**  
  
[NAME:TITLE]  
  
**Project Plan Documentation**  
  
[LINK TO PROJECT DOCS]  
  
**Project Notes**  
  
[Any notes on project 1]  
  
### Finalize  
#### Detailed Changelog  
[LINK TO CHANGELOG TEMPLATE]  
  
#### Contributors List  
- Contributor 1  
    - Contribution Details
    - Link to Documentation
- Contributor 2  
      - Contribution Details
      - Link to Documentation
  
#### Auxillary Documentation   
[Links if applicable]  
  
#### QA Documentation  

**QA Strategy Document**

[Outlines The Original Strategy Project Level Integration Assurance]

**QA Execution Document**

[Outlines Project Level Integration Assurance]

- [ ] The QA execution `DOES` follow the original QA Strategy document
- [ ] The QA execution `DOES NOT` follow the original QA Strategy document

If QA execution `DOES NOT` follow the original QA Strategy document, please explain why in fine detail:

[Explain the QA change in fine detail]

**QA Contract**

- [ ] The QA completed for this Milestone `DOES` ensure delivery of the Milestone purpose

**Justification Statement**

[Provide a detailed statement of satisfaction of the QA Organization Level QA requirements]

#### Certification Documentation  
[Link to Certification Documentation]  
  
#### Communication Announcement  
[Link to Required Comms]  
  
#### Delivery Date  
01/01/1970
### General Notes  
[Any notes]  
### Editorial Notes  
[Opinion piece]  
### External Links
[If Applicable]