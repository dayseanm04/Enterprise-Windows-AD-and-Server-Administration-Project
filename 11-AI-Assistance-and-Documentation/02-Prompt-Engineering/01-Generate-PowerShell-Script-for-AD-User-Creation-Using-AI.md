# 01 – Generate PowerShell Script for AD User Creation Using AI

### Prompt
Show me a PowerShell script to create user accounts in Active directory. I'm using a windows 2019 server. The domain is corp.company.com and under the domain is users-ou and under users-ou there are departments OUs (HR, Administration, IT, Finance, Customer service), I want a powershell script to create 2 users accounts for each ou.

## AI Response (Summary)

ChatGPT generated a PowerShell script that creates 2 Actice Directory User Accounts for each Department OU in the Users-OU. The script created User accounts like:

- HR-User1 (Which is the users first name)
- Test (the users last name)

<img width="941" height="594" alt="10" src="https://github.com/user-attachments/assets/e3c3157f-e26a-4131-9965-32e2bb6bb4cf" />


## How I Used It

I first tested it in the **TST-AD-SRV** Virtual Machine, which represents a test environment. What ever change I make in the test dosent affect the production server which is **Win-2019-SRV**

<img width="666" height="215" alt="11" src="https://github.com/user-attachments/assets/3f03e232-2468-488e-a51e-23fe732e98bc" />


