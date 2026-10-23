# Insider-data-theft-investigation

A simulated insider data theft investigation using Windows 10 VM and investigated with Autopsy. This is all documented in the [lab-notebook](lab-notebook/) and [findings table](evidence-notes/findings.md).


## Why I chose this project
I chose insider data theft as it is a common security challenge within corporate forensics, where an employee leaves and takes data with them. Building the scenario myself allows me to practise evidence handling such as cloning, hashing and verifying a working copy. It also let me analyse a Windows disk in Autopsy and keep contemporaneous notes throughout the project.

## Scenario
Caleb Bridger, a sales analyst at the fictional company Jewellery Dream leaves to join a rival company and takes Jewellery Dreams' customer list and pricings. HR asks the forensic examiner to investigate Caleb's returned laptop. Full details in [Scenario](documents/scenario.md).


## Tools Used
- VirtualBox 7.4.2: Built the "laptop" VM and the "analysis" VM. Both systems used Windows 10 Pro.
- Autopsy 4.23.1: Analysis of the laptop disk.
- 7-Zip: Created the password protected archive in the scenario


## Repository Structure
- [lab-notebook/](lab-notebook/): Notes and write ups of each section. Contemporaneous notes stored inside [raw-notes/](lab-notebook/raw-notes/)
- [documents/](documents/): evidence items, scenario and screenshots.
- [evidence-notes/](evidence-notes/): Findings table.


## Key Findings
- HolidayPictures.7z was deleted at 15:38 on the 11th of October. The name was misleading for an archive of company files, this shows concealment but no proof of intent.
- The user searched "How to delete files permanently from windows." in Edge.
- In Autopsy, recent documents show file paths to "customers.csv" and "pricings.csv" which no longer exist on the disk.
- Web history reveals search of OneDrive and blocked account creation which shows an attempt but not a transfer or intent of the account.


## Limitations
- No completed transfer and no record of USB device.
- The suspect and examiner are the same person so analysis wasn't blind.
- Only used one tool (Autopsy) so no crosschecking with another tool.

