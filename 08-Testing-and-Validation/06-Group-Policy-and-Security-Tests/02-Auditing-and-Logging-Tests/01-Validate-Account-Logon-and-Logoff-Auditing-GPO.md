# Validate Account Logon and Logoff Auditing GPO

## Overview

This document validates the account logon/logoff and Credential Validation audit GPO configured on **`OTCS-DC01`**. Four tests confirm the policy is actually generating Security log events.

## Test 1: Logoff Event Auditing 

**Note:** I logged out and logged back into the DC (`OTCS-DC01`) as Administrator.

In Server Manager, click **Tools** > **Event Viewer**.

<img width="601" height="256" alt="1" src="https://github.com/user-attachments/assets/b49028c6-ef6f-4a65-88b1-33628c8d7eb0" />

Click **Windows Logs** > **Security**.

<img width="835" height="458" alt="2" src="https://github.com/user-attachments/assets/0d795468-088f-4e4e-90f8-cef587e14998" />

You can see logs for logon and logoff. I right-clicked an **Audit Success** log for **Logoff** and clicked **Event Properties**.

<img width="825" height="422" alt="3" src="https://github.com/user-attachments/assets/f6e1c5fc-5e60-4efe-82e9-c9251649f393" />
