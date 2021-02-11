### Milestone Title: Tx Indexer 
### Leader  
Eduardo Diaz Blockchain Engineer
### Date(s)  
01/14/2021
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
[Tx indexer Proposal](https://github.com/pokt-network/organization/blob/main/proposals/1-08-01-2021/tx-indexer-milestone-proposal.md)

## Milestone Detailed Summary
The current tx indexer implemented by Tendermint team offers subpar performance by forcing us to load all index keys sort them and then build a page.

this default tx indexer has turned out to be inneficcient due to: 
- Missindexing of txs: block events get appended to all txs
- Inneficient retrieval of data: originally tendermint loaded all tx's in memory which was causing memory overflows, we proceeded to change that however due to limitations on the implementation we still must iterate through all tx's within range sort them and then build the page.

The tx indexer should be able to understand the indexes it's going through and be able to build a page without having to load all keys and sorting them.

I propose we keep this format in order to keep compatibility with indexing (following format will be broken into a regular expression)

```regex
([a-z .]+)\/([a-z 0-9]+)\/([0-9]+)\/([0-9]+)[\/]?
```
this makes sure we get any format like this
```
send.action/<address>/<height>/<index>
claim.action/<address>/<height>/<index>
tx.block/<height>/<height>/<index>
```

This index key would allow us to:
- easily grasp the context of the key in a humanly readable fashion
- break down height & index to allow our store to iterate through them in order.

### Milestone Goals
- Establish a proper indexing format which should be future proof.
- Reduce the bottleneck caused by the tendermint's implementatin. 

### Proposal Estimated Timeline  
1 Month

### How to test functionality?  
Protocol should work seamlesss, it must mantain a node should be able to query through transactions.

if events are changed for this a node must resync in order to reindex all transactions.
otherwise nodes would not be able query txs irregardless of the store.

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
- Functional Testing                  // functionality testing / regression test *ED*
- Benchmark Testing                   //  of improvement *ANDREW*
- Custom goleveldb comparator         // Documentation & code completeness *ED*
  
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
