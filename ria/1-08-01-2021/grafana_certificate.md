### Report Of Immediate Action Title 
Grafana/Monitoring certificate
### Engineer (One Per Engineer)
Julio Jimenez: Specialist
### Date(s)
02/9/2021
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
Created a new certificate named `mainnet-certificate` for `grafana-mon.mainnet.pokt.network` in the `monitoring` namespace. 

### Evidence and Justification of the need for the Immediate Action:**
Infrastructure team and business team could not get access to dashboards for monitoring and business metrics. 
### Timeline of the Immediate Action
1 week

### Survey
- [X] Steps `CAN/WILL` be taken to avoid this Immediate Action in the future. Explain in detail below:

- Do not edit the certificate in or the `prometheus-operator-grafana` ingress
- Do not remove/edit the `mainnet-certificate` certificate in the `monitoring' namespace

- [ ] Steps `CANNOT/WILL NOT` be taken to avoid this Immediate Action in the future. Explain in detail below:

[Detailed Explanation]

### General Notes
Troubleshooting and monitoring time are being taken into consideration in the timeline of the Immediate Action.

This configuration is managed by a helm chart, so the changes had to be done manually. We will bring all this configurations to the `pocket-core-internal-deployments` repository once when we switch to Flux v2.