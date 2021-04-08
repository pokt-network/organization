### Certification Documentation For RC-0.6.0 Milestone
### Leader  
[Emanuel Medrano: Support Engineering Lead/Specialist]  
### Date(s)  
03/30/2021  
### Participants
- [Emanuel Medrano:Support Engineering Lead/Specialist]
- [Eduardo Rodriguez:Blockchain Engineer/Specialist] - Colaborator
- [Otto Vargas:Blockchain Engineer/Spceialiste] - Colaborator 
## Survey
### Category
- [X] Protocol/Blockchain Dev  

### LEVEL
- [X] RC
- [ ] STABLE

## Certification
### Summary
**How is this deliverable certified?**

- Execution of the refactored functional tests: 1 single node setup
- Execution of the legacyCodec feature testing: 1 single node setup
- Execution of the behavioural tests added for specific changes: 1 single node setup
- Re-test of the legacyCodec feature testing when changing the upgradeHeight to be dynamic: 1 single node setup
- Execution of the refactored functional tests: 5 single node setup
- Execution of the legacyCodec feature testing: 5 single node setup
- Execution of the behavioural tests added for specific changes: 5 single node setup
- Re-test of the legacyCodec feature testing when changing the upgradeHeight to be dynamic: 5 single node setup
- Bugs found and reported, retesting.
- All product criteria are met and confirmed.

References:
- Functional Tests Results: https://docs.google.com/spreadsheets/d/1i8Oc5caTgoPPSG9IteCNYvzUlO-emYuEieYyg3QhLJI/edit#gid=966543550
- Functional Tests: https://github.com/pokt-network/pocket-core-func-tests

**Certification Contract**

- [X] The certification of this deliverable ensures Stability Level as described in the handbook

**Justification Statement**

After the whole suite of the original functional test was refactored to latest functionalities added and ran, the legacyCodec specific test were added and ran, the bugs were reported-solved-retested, the acceptance testing was set to passed; all these in both, a single node network and a 5 node network; then we can conclude that this RC-0.6.0 is certified as stable.

### Alternatives Considered
**Alternative Approach 1**

Functional and acceptance Testing on both: 1 single node and 5 nodes networks.

**Pros**
- Tests of all the expected behaviour by design.
- Validated all happy paths within the product.
- Focuses on details and requirements.

**Cons**
- Doesn't evaluate exceptions.
- Ignores non desired functionality.

**Alternative Approach 2**

Negative and Non-functional Testing on both: 1 single node and 5 nodes networks.

**Pros**
- Evaluate exceptions.
- Evaluate error messages.
- Evaluate proper error validations.
- Expose possible software vulnerabilities.

**Cons**
- Not likable by the user.

### Tools Required
**Tool 1**

PRLTS

**Link**

https://github.com/pokt-network/prlts

**Planned Usage**

Send network relays to the node(s)

**Tool 1**

Pocket Core RPCs

**Link**

https://github.com/pokt-network/pocket-core/blob/staging/doc/rpc-spec.yaml

**Planned Usage**

Functional and non-functional tests of the same.

**Alternative Approach 3**

Load Testing within the following characteristics:
5,000 Validator Nodes
4,166,666 Relays per session (1 hr sessions).
~15 minute blocks

**Pros**
- Tests of all the expected behaviour by design.
- Stress the software to specific network configurations to make healthy conclussions on the same, by exploring its boundaries. 

**Cons**
- The peering capabilities is done via Seed Nodes, as using persistent peering proved problematic for consensus in the earlier blocks.
- There are hardware limitations in the number and size of instances that GCP can provision in a single run.
- Disk space limited the generation of PRLTS evidence.

### General Notes  
There were minor details found, that for the purpose of this release and it's aggressive timeline, would be fixed/solved on further releases.

Several observations were made during the load test:

Memory climbs when processing claims and proof as observed in the Memory RSS Graph image.
The test processed ~4.133 M relays according to aggregated PRLTS data.
Claims were succesfully submitted and finalized into the state.
Proofs were submitted, however hardware limitations knocked more than 33% of the validator power offline, causing a chain halt.
Test Result: Inconclusive due to hardware limitations of the environment.