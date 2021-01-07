---
name: Tx Indexer Rank Vote Proposal
about: Indexing txs in an efficient manner. 
title: "Milestone Rank Vote Proposal: Tx Indexer"
labels: Proposal
assignees: 'Eduardo Diaz'
---

### Proposal Title 
Solid Tx Indexing

### Date(s)
01/01/1970

### Category
- [ ] Infrastructure
- [x] Protocol/Blockchain Dev
- [ ] App Solutions
- [ ] Quality Assurance
### Contract
- [ ] This process follows the Milestone Rank Vote Framework as discussed in the Pocket Network Corporation's `Organization Handbook`
- [x] This process `DOES NOT` follow the Milestone Rank Vote Framework as discussed in the Pocket Network Corporation's `Organization Handbook`

If `DOES NOT` follow the Handbook's Milestone Rank Vote Framework, please describe in detail why below:
Still needs to be written.

### Description of Proposal
Currently we are reliant on tx indexing method of tendemint, this has turned out to be inneficient, due to:
- Missindexing of txs: block events get appended to all txs
- Inneficient retrieval of data: originally tendermint loaded all tx's in memory which was causing memory overflows, we proceeded to change that however due to limitations on the implementation we still must iterate through all tx's within range sort them and then build the page.

I propose we keep this format in order to keep compatibility with indexing (following format will be broken into a regular expression)
```regex
([a-z .]+)\/([a-z 0-9]+)\/([0-9]+)\/([0-9]+)[\/]?
```
this makes sure we get any format like this
```
send.action/<address>/<height>/<index>
claim.action/<address>/<height>/<index>
```
This index key would allow us to:
- easily grasp the context of the key in a humanly readable fashion
- break down height & index to allow our store to iterate through them in order.

#### Caveats
- The pending overhauling of events for RC-0.6.0 must be taken into account for the indexing. (As a note, the event itself is not neccesary for the first element of the index key, the tx memo or message would work as well)
- The efficiency of the comparator underneath, given that this custom index keys are non standard iterating through them and ranging through them might have a slight decline. As long as this is still faster than loading all tx's on to memory & soritng them and building the page, then this implemantation should hold for production.
