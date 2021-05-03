### Report Of Immediate Action Title 
Pocket Website Wordpress stack update.
### Engineer (One Per Engineer)
Nelson Colón: Infra Engineer.
### Date(s)
04/28/2021
### Category
- [X] Infrastructure
- [ ] Protocol/Blockchain Dev
- [ ] App Solutions
- [ ] Quality Assurance
- [ ] N/A
### Contract
- [X] This process follows the Immediate Action Framework as discussed in the Pocket Network Corporation's `Organization Handbook`
- [ ] This process `DOES NOT` follow the Immediate Action Framework as discussed in the Pocket Network Corporation's `Organization Handbook`

If `DOES NOT` follow the Handbook's Immediate Action Framework, please describe in detail why below:
[Detailed Explanation]

## Report of Immediate Action
### Detailed Summary of executed Immediate Action
In order for files to be uploaded, had to modify the php ini configuration file from the wordpress site, and, enable the option to run scripts in wordpress in the WAF solution software that we use, Sucuri.

### Evidence and Justification of the need for the Immediate Action:**
As our users were not able to upload files to the server, this meant that posts couldn't be created in the intended way.

### Timeline of the Immediate Action
04/28/2021

### Survey
- [X] Steps `CAN/WILL` be taken to avoid this Immediate Action in the future. Explain in detail below:

This work was necessary as per security best practices.

- [ ] Steps `CANNOT/WILL NOT` be taken to avoid this Immediate Action in the future. Explain in detail below: