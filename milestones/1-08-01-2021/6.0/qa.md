### QA Documentation For RC-0.6.0 Milestone
### Leader  
[Emanuel Medrano: Support Engineering Lead]  
### Date(s)  
03/30/2021  
### Participants
- [Emanuel Medrano:Support Engineering Lead]
## Survey
### Category
- [ ] Infrastructure  
- [ ] Protocol/Blockchain Dev  
- [ ] App Solutions  
- [X] QA/Support Engineering

### Implementation (Check All That Apply)
- [ ] Unit Tests
- [X] Integration Tests
- [X] Functional Tests
- [X] Behavior Tests
- [ ] Load Tests
- [ ] Stress Tests
- [ ] Simulations
- [ ] Certification
- [ ] Benchmarks
- [ ] Performance Tests
- [ ] Resource Monitoring
- [X] Negative Tests

## QA
### Summary

**How is this deliverable Quality Assured?**

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

**What was the original strategy?**

The Testing Strategy selected was:
- Refactoring of the existing Pocket Core func-tests.
- Re-running of refactored Pocket Core func-tests.
- Design of Pocket Core new func-tests for most recent and most impactfull features.
- Execution of Pocket Core new func-tests for most recent and most impactfull features on a single node network configuration.
- Execution of Pocket Core new func-tests for most recent and most impactfull features on a 5 nodes network configuration.
- Bugs Reporting and follow up.
- Bugs fixed re-testing.
- Legacy Codec related tests re-run for latest changes.

**Did the QA methodology follow the original strategy?**
- [X] `YES`
- [ ] `NO`

**QA Contract**

- [X] The QA for this deliverable ensures delivery of the project purpose

**Justification Statement**

It was considered the most complete strategy for the short time given and the urgency of the milestone, meaning the priorization was needed to make the milestone be submitted on time for the whole organization.

Most important, this milestone involved consensus breaking changes that needed throughout tests of the software, to make sure that existing functionality was not affected negatively and newly added functionality was covered as well.

Plus, negative and behavior tests included as integration tests, so that the tests got related to real scenarios.

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

### General Notes  
There were minor details found, that for the purpose of this release and it's aggressive timeline, would be fixed/solved on further releases.