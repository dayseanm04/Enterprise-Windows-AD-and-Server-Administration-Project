# Validate Account Logon and Logoff Auditing GPO

## Overview

This document validates the account logon/logoff and Credential Validation audit GPO configured on **`OTCS-DC01`**. Four tests confirm the policy is actually generating Security log events.

## Test 1: Logoff Event Auditing 

**Note:** I logged out and logged back into the DC (`OTCS-DC01`) as Administrator.
