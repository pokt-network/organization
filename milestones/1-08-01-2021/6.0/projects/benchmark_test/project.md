### Project Title:  Benchmark Testing 6.0
### Leader  
Otto Vargas  
### Date(s)  
3/30/2021  
### Category  
- [ ] Infrastructure  
- [X] Protocol/Blockchain Dev  
- [ ] App Solutions  
- [ ] Quality Assurance  
### Contract  
- [X] This process follows the Project Framework as discussed in the Pocket Network Corporation's `Organization Handbook`  
- [ ] This process `DOES NOT` follow the Project Framework as discussed in the Pocket Network Corporation's `Organization Handbook`  
  
If `DOES NOT` follow the Handbook's Project Framework, please describe in detail why below:  
### Project Purpose
Benchmark Test Performance of pocket 0.6.0 release with the protobuff changes. 
### Key Goals Of Project
- Test that the performance for the new release is equal or better than the previous release.
- Document the results for future reference
#### Milestone
6.0 Release  
#### Estimated Timeline  
4 days  
  
- [X] Timeline `DOES` correspond with the Milestone Estimated Timeline  
- [ ] Timeline is `DOES NOT` correspond with the Milestone Estimated Timeline  
  
If timeline is `DOES NOT` correspond with the Milestone Estimated Timeline, please describe in detail the reasons below:  
N/A
#### How to test functionality?  
Using gcvis as a tool, run a local full node for atleast 3 days without stop and document the behaviour.
#### Issues  
**List**  
  
- Run new build with gcvis   
  
##### Run new build with gcvis  
**Summary**  
  
The new build of pocket core was run for 5 days using gcvis to log data from heap and memory usage. The run showed small gains
in memory usage and consistent alloc / dealloc cycles. The initial thoughts about a small memory leak are still present, 
and is observed to be around 20-25 mb allocation in approximately 5 days which is smaller that the 35-40 on version 5.2.9 . 

  
**Leader**  
  
 Otto Vargas
  
**Issue Documentation**  
  
attached on the folder 
  
**Issue Notes**  


### Finalize
#### Detailed Changelog

#### Contributors List
- Otto Vargas

#### Auxillary Documentation


#### QA Documentation
**QA Strategy Document**

N/A for Project

**QA Execution Document**

[Outlines Issue Level Integration Assurance]

- [X] The QA execution `DOES` follow the original QA Strategy document
- [ ] The QA execution `DOES NOT` follow the original QA Strategy document

If QA execution `DOES NOT` follow the original QA Strategy document, please explain why in fine detail:

[Explain the QA change in fine detail]

**QA Contract**

- [X] The QA completed for this project `DOES` ensure delivery of the project purpose

**Justification Statement**

Project based on  documentation / information gathering with external tool.

#### Delivery Date
03/30/2021
### General Notes

### Editorial Notes

### External Links


### Lead Signoff

- [ ] I [NAME:TITLE] approve this project

- [ ] This project did not receive Milestone Lead signoff

If the project did not receive Milestone Lead signoff, please explain why in detail:

[Explain why there is no lead sign off]
