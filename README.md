# Active Directory and SIEM Project

## Project Overview

To study Active Directory and SIEM, I created a project in my virtual box. I set up a domain in Active Directory, added users to it, and installed SIEM agents to gather logs from the endpoints and try to create an attack scenario and analyze the logs.

## Topics Learned

- How to set up a domain controller in Windows Server 2022
- How to create users in a domain controller
- How to add users to a domain
- How to add ELK agents to endpoints and get logs from endpoints
- How to enable default detection rules in ELK
- How to attempt brute force on the user in the AD and generate alerts in ELK

## Prerequisites

- VirtualBox
- Windows 10
- Kali Linux
- Windows Server 2022
- Elastic Stack Trial

## Setup Instructions

1. **Install Prerequisites**:
   - Install VirtualBox on your machine.
   - Set up virtual machines with Windows 10, Kali Linux, and Windows Server 2022.

2. **Configure the AD Domain Controller**:
   - Open Server Manager and navigate to `Manage > Add Roles and Features`.
   - Follow the prompts to set up the domain controller.

3. **Create Domain and Users**:
   - Create a domain controller `soc.team`.
   - Create a new user group named `SOC`.
   - Create users `Cyril` and `Athul`, as well as organizational units named `HR` and `NOC`, and add the users to these units.

4. **Log in to User Accounts**:
   - Attempt to log in to the user accounts using the target machine.

5. **Set up ELK**:
   - Log in to the ELK trial in the cloud.
   - Install ELK agents on the endpoints.

6. **Verify Logs**:
   - Ensure logs are being received from the endpoints.

7. **Create Attack Scenarios**:
   - Attempt to brute force the users in Active Directory to generate alerts in the SIEM.
   - Investigate the alerts generated.

## Diagram

![Project Setup Diagram](diagram.png)

## Screenshots

Here are some screenshots illustrating the project setup and results:

### Domain Controller Setup

![Domain Controller Setup](screenshots/domain_controller_setup.png)

### User Creation

![User Creation](screenshots/user_creation.png)

### ELK Setup

![ELK Setup](screenshots/elk_setup.png)

### Logs from Endpoints

![Logs from Endpoints](screenshots/logs_from_endpoints.png)

## Issues and Troubleshooting

- I attempted to brute force the users in Active Directory to receive alerts on the SIEM, but I encountered issues. I am currently troubleshooting this.

## Conclusion

This project helped me understand the setup and management of Active Directory and the integration of SIEM for monitoring and alerting on potential security incidents.
