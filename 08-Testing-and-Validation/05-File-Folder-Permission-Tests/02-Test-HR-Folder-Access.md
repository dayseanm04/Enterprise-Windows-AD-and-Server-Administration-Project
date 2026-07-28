# Test HR-Sec-G Folder Access

## Overview
For this test, I'm logged in as Emma Davis [`e.davis`] another test user for the project. She's in the HR Department, and belongs to both `HR-Sec-G` and `EveryUser-Sec-G`. `HR-Sec-G` has Full Access to the Company-Folder and HR-Folder and their files, so this test checks two things: that she actually has full access where she's supposed to, and that she's still blocked from folders outside her permissions, like IT.

## Verify the Logged-In User
Confirmed I'm logged in as `e.davis`:

<img width="505" height="198" alt="1" src="https://github.com/user-attachments/assets/046c7be5-3e2d-4038-9e2e-0eaf5c5e8bc8" />

## Test Company-Folder Access (Full Access)

### 1. Open File Explorer, Click Network, Click OTCS-DC01

<img width="689" height="424" alt="2" src="https://github.com/user-attachments/assets/5c9083fa-9df2-4525-8f48-63428d5e2a07" />

<img width="712" height="410" alt="2" src="https://github.com/user-attachments/assets/c94a3b72-985e-4a69-bf45-87cc5a4f124a" />

### 2. Click Company-Folder

<img width="795" height="414" alt="3" src="https://github.com/user-attachments/assets/b614e966-5da0-46b4-8292-febc29c56f4f" />

### 3. Edit and Save a File
Opened **`policies.txt`**, wrote some data into it, and saved it — no issues, which confirms Full Access on the file:

<img width="559" height="326" alt="4" src="https://github.com/user-attachments/assets/86a0f561-935a-4aef-9fbf-7ffc2101eb62" />

**Opened policies.txt to verify**

<img width="774" height="430" alt="5" src="https://github.com/user-attachments/assets/473f75ea-582d-4f42-a4ec-9f44e9e7bc48" />

## Test HR-Folder Access (Full Access)
Went back to `\\OTCS-DC01` and opened the HR-Folder. As expected, Emma has full access to the HR-Folder and its files, so I opened `hiring-doc.txt` with no issues:

<img width="748" height="420" alt="6" src="https://github.com/user-attachments/assets/9c0914b0-6a6c-46ae-a971-669618724695" />

<img width="777" height="446" alt="7" src="https://github.com/user-attachments/assets/855ddba9-0802-488e-8842-250736afaf27" />

## Test IT-Folder Access (Should Be Denied)
Tried to open the IT-Folder next:

<img width="799" height="524" alt="8" src="https://github.com/user-attachments/assets/ad15b04c-4774-45a4-a41a-38b639d732be" />

Couldn't get in — access denied, exactly as expected since Emma isn't part of **`IT-Sec-G`**:

## Test Finance-Folder Access (Should Be Denied)
Tried to open the Finance-Folder next:

<img width="799" height="440" alt="9" src="https://github.com/user-attachments/assets/3af0f61a-b0a7-4af0-928a-d29f04d37ea4" />
