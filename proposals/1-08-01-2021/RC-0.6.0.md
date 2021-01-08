### Proposal Title 
RC-0.6.0
### Proposer
[Andrew: CTO]
### Date(s)
01/08/2021
### Category
- [ ] Infrastructure
- [X] Protocol/Blockchain Dev
- [ ] App Solutions
- [ ] Quality Assurance
### Contract
- [ ] This process follows the Milestone Rank Vote Framework as discussed in the Pocket Network Corporation's `Organization Handbook`
- [X] This process `DOES NOT` follow the Milestone Rank Vote Framework as discussed in the Pocket Network Corporation's `Organization Handbook`

If `DOES NOT` follow the Handbook's Milestone Rank Vote Framework, please describe in detail why below:

This is the first milestone proposal / rank vote and the handbook is not finished. This proposal will gloss over some details required in future proposals
as listed in the handbook.
[Detailed Explanation]
## Proposal
### Detailed Summary of Proposal
To frame RC-0.6.0 in a Rank Vote Proposal format, we first must understand the basics of RC-0.6.0 and its importance.

Here are the bullet points of how it improves both the software and the organization

- Uses Protobuf encoding instead of amino. This improves both speed, resource consumption and (most importantly) inoperability between languages
- Patches the Merkle Tree security hole (won't go into specifics, but a big flaw in the protocol that is exposed)
- Contains an upgrade mechanism that can be modeled after in the future

NOTE: this milestone is near completion already, and for reasons explained in the 'contract' section, the details are glossed over
### Estimated Timeline
1 Month

**Evidence and Justification for this timeline:**

Beta-0.6.0 is near code complete. 

The blockers will be QA and upstreaming protobuf to dependencies (like Pocket JS)

**Timeline Consultants**
 - Consultant 1:Luis De. Leon:CEO
 - Consultant 2:Otto Vargas: Blockchain Specialist
### How to test functionality?
Seamless transition between encoding formats (send transactions/queries before and after upgrade height and get the same result)
Seamless transition between merkle upgrade (claims and proofs don't stop between upgrades)
### Project Abstractions
- Codec changes
  - Near complete, finish the backwards compatible codecs.
- QA / Certification
  - Normally, this would not be its own project, however in this case we did not conduct 6.0 development in the new format.
  This justifies a QA and Certification project to ensure the quality of the legacy deliverables.
### QA Planification
- Unit tests that test both proto and amino encodings
- Unit tests that verify merkle functionality
- Integration tests with Pocket JS
- Simulation (upgrade) tests in a clean room environment 

(Normally would use QA plan template, but see contract section for gloss over explanation)
### Community Buy In Evidence
N/A
### Communication Plan
Drafting a message for discord, completing an upgrade guide, documenting changes in the changelog, and writing a detailed account in the release nots.

Coordinating major upgrade with governance through DAO proposal

### General Notes
N/A
### External Links
N/A
### Executive Signoff
- [ ] APPROVED
- [ ] DECLINED

If `DECLINED`, please describe in detail why below: