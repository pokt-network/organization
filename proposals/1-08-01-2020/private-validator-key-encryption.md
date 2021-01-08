---
name: Validator Key encryption Rank Vote Proposal
about: encrypting priv val key as a security measure. 
title: "Milestone Rank Vote Proposal: private validator key encryption"
labels: Proposal
assignees: 'Eduardo Diaz'
---

### Proposal Title 
Private validator key encryption

### Date(s)
08/01/2021

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
Due to tendermint decisions we leave an unencrypted `priv_val_key.json` on the datadir. This is a security vulnerability for node-runners if a node is compromised looking up through dirs will expose their private key.

We have already differed from tendemrint in many philosophies of development we should likely make sure this private key is encrypted in the datadir provide a passphrase when running the node that should allow the node to unencrypt it in memory.

We should likely follow on Ethereum's [keystore](https://goethereumbook.org/en/keystore/) example as a standard on how to deal with vulnearable files.

### Estimation
3-5 weeks

This is due to a required break down of how tendermint accessess the file, having to provide a secure manner in which to access the encrypted file, we also need to apply this changes onto pocket core making it an effort on 2 deep layers of our stack.
