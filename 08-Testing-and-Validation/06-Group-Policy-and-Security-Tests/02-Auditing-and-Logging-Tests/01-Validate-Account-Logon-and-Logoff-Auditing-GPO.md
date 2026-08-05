# Validate Account Logon and Logoff Auditing GPO

## Overview

This document validates the account logon/logoff and Credential Validation audit GPO configured on **`OTCS-DC01`**. Four tests confirm the policy is actually generating Security log events.

## Test 1: Logoff Event Auditing 

**Note:** I logged out and logged back into the DC (`OTCS-DC01`) as Administrator.

In Server Manager, click **Tools** > **Event Viewer**.

<img width="601" height="256" alt="1" src="https://github.com/user-attachments/assets/b49028c6-ef6f-4a65-88b1-33628c8d7eb0" />

Click **Windows Logs** > **Security**.
