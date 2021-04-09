### Report Of Immediate Action Title 
Disable GKE Auto Upgrade
### Engineer (One Per Engineer)
Julio Jimenez: Specialist
### Date(s)
04/9/2021
### Category
- [X] Infrastructure
- [ ] Protocol/Blockchain Dev
- [ ] App Solutions
- [ ] Quality Assurance
### Contract
- [X] This process follows the Immediate Action Framework as discussed in the Pocket Network Corporation's `Organization Handbook`
- [ ] This process `DOES NOT` follow the Immediate Action Framework as discussed in the Pocket Network Corporation's `Organization Handbook`

If `DOES NOT` follow the Handbook's Immediate Action Framework, please describe in detail why below:

[Detailed Explanation]
## Report of Immediate Action
### Detailed Summary of executed Immediate Action
- Set cluster release channel to Static
- Disable node auto-upgrade on each of the node pools

### Evidence and Justification of the need for the Immediate Action:**
Whenever nodes get an update they need to be restarted, taking down all our infrastructure. Now we will have more control of the downtime while upgrading.
### Timeline of the Immediate Action
1 day

### Survey
- [X] Steps `CAN/WILL` be taken to avoid this Immediate Action in the future. Explain in detail below:

- Do not set the cluster release channel to Static
- Do not enable the node-autoupgrade option when creating or editing a node pool

- [ ] Steps `CANNOT/WILL NOT` be taken to avoid this Immediate Action in the future. Explain in detail below:

[Detailed Explanation]

### General Notes
Even though the cluster release channel was set to Static, GKE updates the API server version whenever an update is ready and this cannot be changed.