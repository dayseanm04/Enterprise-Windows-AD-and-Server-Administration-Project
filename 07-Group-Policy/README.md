# 07 – Group Policy

The Group Policy work for this project is split between two sections: where the GPOs were configured, and where they were tested.

## Where the GPOs Were Configured

All Group Policy settings were set up in **[06-Security-and-Hardening](../06-Security-and-Hardening/)** using Group Policy Management.

**Account and Password Policies**
- [**Configure Password Policies**](../06-Security-and-Hardening/01-Account-and-Password-Policies/01-Configure-Password-Policies.md)
- [**Configure Account Lockout Policies**](../06-Security-and-Hardening/01-Account-and-Password-Policies/02-Configure-Account-Lockout-Policies.md)

**Audit and Logging**
- [**Configure Account Logon Auditing**](../06-Security-and-Hardening/02-Audit-and-Logging/01-Configure-Account-Logon-Auditing.md)
- [**Configure Logon/Logoff Auditing**](../06-Security-and-Hardening/02-Audit-and-Logging/02-Configure-Logon-Logoff-Auditing.md)
- [**Configure File System and Share Auditing**](../06-Security-and-Hardening/02-Audit-and-Logging/03-Configure-File-System-and-Share-Auditing.md)

## Where the GPOs Were Tested

Every policy above was tested to confirm it actually applied. The tests are in **[08-Testing-and-Validation/06-Group-Policy-and-Security-Tests](../08-Testing-and-Validation/06-Group-Policy-and-Security-Tests/)**.

- [**Test Password Policy GPO**](../08-Testing-and-Validation/06-Group-Policy-and-Security-Tests/01-Account-and-Password-Policy-Tests/01-Test-Password-Policy-GPO.md)
- [**Test Account Lockout GPO**](../08-Testing-and-Validation/06-Group-Policy-and-Security-Tests/01-Account-and-Password-Policy-Tests/02-Test-Account-Lockout-GPO.md)
- [**Validate Account Logon and Logoff Auditing GPO**](../08-Testing-and-Validation/06-Group-Policy-and-Security-Tests/02-Auditing-and-Logging-Tests/01-Validate-Account-Logon-and-Logoff-Auditing-GPO.md)





