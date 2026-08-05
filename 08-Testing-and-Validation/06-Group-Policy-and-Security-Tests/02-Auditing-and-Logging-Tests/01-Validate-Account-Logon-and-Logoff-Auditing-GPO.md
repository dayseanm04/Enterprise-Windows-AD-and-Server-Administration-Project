# Validate Account Logon and Logoff Auditing GPO

## Overview

This document validates the account logon/logoff and Credential Validation audit GPO configured on **`OTCS-DC01`**. Four tests confirm the policy is actually generating Security log events.

## Test 1: Logoff Event Auditing 

**Note:** I logged out and logged back into the DC (**`OTCS-DC01`**) as Administrator.

In Server Manager, click **Tools** > **Event Viewer**.

<img width="601" height="256" alt="1" src="https://github.com/user-attachments/assets/b49028c6-ef6f-4a65-88b1-33628c8d7eb0" />

Click **Windows Logs** > **Security**.

<img width="835" height="458" alt="2" src="https://github.com/user-attachments/assets/0d795468-088f-4e4e-90f8-cef587e14998" />

You can see logs for logon and logoff. I right-clicked an **Audit Success** log for **Logoff** and clicked **Event Properties**.

<img width="825" height="422" alt="3" src="https://github.com/user-attachments/assets/f6e1c5fc-5e60-4efe-82e9-c9251649f393" />

It shows the log for when I shut down the VM, confirming the logoff event was recorded.

<img width="732" height="338" alt="3" src="https://github.com/user-attachments/assets/a70fb82e-6546-4127-841c-46f15e1299f8" />

I cleared the log so the next test starts from a clean baseline.

<img width="1012" height="402" alt="4" src="https://github.com/user-attachments/assets/e22c6f8e-5dd1-4dc9-a21b-91a8293a3f22" />

Click Cleared

<img width="790" height="280" alt="5" src="https://github.com/user-attachments/assets/8501b4e0-b363-4ccd-bdfb-bd30e622fce6" />

I signed out.

<img width="586" height="246" alt="6" src="https://github.com/user-attachments/assets/9cf8ed90-387d-404d-ac5d-944b4e533f67" />

---

## Test 2: Logon Failure and Success Auditing

**Why this test:** account lockout and brute-force detection both depend on failed logons being logged. 

I logged in as **`e.davis`** using an incorrect password 3 times, then logged in again with the correct password.

<img width="898" height="507" alt="7" src="https://github.com/user-attachments/assets/4e764f48-0828-4bf0-a7dd-5747252ab80a" />

<img width="842" height="450" alt="8" src="https://github.com/user-attachments/assets/164e1fe6-c410-423a-8721-0b9488e97745" />

I logged in as **`e.davis`** using the correct password.

<img width="644" height="342" alt="9" src="https://github.com/user-attachments/assets/2841cb1c-232c-4139-a475-00c3684a547d" />

**Verify:**

I signed out and logged back in as Administrator, then went to **Server Manager > Tools > Event Viewer > Windows Logs > Security** and scrolled until I found the **Audit Failure** logs.

<img width="828" height="447" alt="10" src="https://github.com/user-attachments/assets/592e5e22-a647-4e26-af86-ba97ec14c5fe" />

I right-clicked the first one and clicked **Event Properties**.

<img width="837" height="389" alt="11" src="https://github.com/user-attachments/assets/9149388b-c6e1-4702-92ea-2beb1d186032" />

It showed the failed logon entry for `e.davis`, confirming the failure was captured.

<img width="688" height="357" alt="12" src="https://github.com/user-attachments/assets/c8911e7b-e803-4958-a6e0-13d07d3a304b" />

I closed that, then scrolled through the logs and found an **Audit Success** log under category **Logon**, right-clicked it, and clicked **Event Properties**.

<img width="853" height="363" alt="13" src="https://github.com/user-attachments/assets/6493c24a-9550-4264-a30a-47ccce623695" />

<img width="790" height="460" alt="14" src="https://github.com/user-attachments/assets/94245ad0-0fb1-4ed8-b414-024ef10ddbff" />

