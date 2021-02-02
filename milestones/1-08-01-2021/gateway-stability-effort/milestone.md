### Milestone Title: Gateway Stability Effort
### Leader  
Wilson Garcia: App Solutions
### Date(s)  
01/24/2021
### Category  
- [ ] Infrastructure  
- [ ] Protocol/Blockchain Dev  
- [x] App Solutions  
- [ ] Quality Assurance  
### Contract  
- [X] This process follows the Milestone Framework as discussed in the Pocket Network Corporation's `Organization Handbook`  
- [ ] This process `DOES NOT` follow the Milestone Framework as discussed in the Pocket Network Corporation's `Organization Handbook`  
  
If `DOES NOT` follow the Handbook's Milestone Framework, please describe in detail why below:  
## Original Proposal  
https://github.com/pokt-network/organization/blob/main/proposals/1-08-01-2021/gateway-stability-effort.md
## Detailed Summary
The team analized the Gateway actual code/implementation and noticed that the cherry picking module which manages the nodes used for every request can be improved to increase the success rate of the service. The result will increase the traffic going thru the Gateway.

The milestone targets the actual cherry picking system module which manages the nodes used for every request to improve its accuracy while selecting the proper nodes as per the algorithm to improve its success rate. The
result will increase the traffict and improve the quality of life.

1. Improve speed
2. Improve stability of the service
3. Reduces resource consumption
4. Improve the visibility of the chery picking flow

### Milestone Goals
- Finish the deep impact analysis.
- Start the code implementation.
- Create new tests.
- Work with the QA team with the testing.
- Transfer an updated Gateway doc to Github.

### Proposal Estimated Timeline
Three weeks
### How to test functionality?
New integration tests are going to be created to properly test the cherry picking flow and the success rate for multiple scenarios including
stable, unstable and intermittent nodes.

## Rank Vote  
https://github.com/pokt-network/organization/tree/main/rank-votes/1-08-01-2021
### Contract   
- [X] This Milestone `IS` signaled priority by the Rank Vote system  
- [ ] This Milestone `IS NOT` signaled priority by PNI's Rank Vote system  
  
If `IS NOT` signaled priority by PNI's Rank Vote system, describe in detail why this milestone is being executed:  
## Milestone  
### Plan  
#### Estimated Timeline  
Three weeks 
  
- [x] Timeline is `THE SAME` as the Original Proposal Estimated Timeline  
- [ ] Timeline is `NOT THE SAME` as the Original Proposal Estimated Timeline  
  
If is `NOT THE SAME` as the Original Proposal Estimated Timeline, please describe in detail the change in timeline below:  
[Detailed Description of Timeline Change]  
#### Projects  
**List**  
- Functional Testing      // functionality testing / regression test *WILSON/PABEL/EMANUEL*
- Unit Testing            // mocha tests *WILSON*
- Integration Testing     // mocha tests *WILSON/PABEL*

- Release Note    // Changelog  *WILSON*
- Documentation   // Update current documentation  *WILSON*
  
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