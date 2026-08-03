# Configure File and Folder Auditing

Builds on [**03-Configure-File-System-and-Share-Auditing.md**](../../06-Security-and-Hardening/02-Audit-and-Logging/03-Configure-File-System-and-Share-Auditing.md) where I configured the **Object Access auditing** *category* . This is the other half: pointing that category at an actual folder by setting up its SACL (System Access Control List).

## Overview
Turning on Object Access auditing at the GPO level doesn't log anything by itself, it just tells Windows to *pay attention* to file activity. To actually get events in the log, I still have to tell Windows which folder to watch and what actions on it count as worth logging. I'm setting this up on the Finance-Folder, since that's the folder I want to track changes on.

## Set Up Auditing on the Finance-Folder
1. Open File Explorer → **This PC** → **Local Disk (C:)** → `shared-folders`.
2. Right-click **Finance-Folder**, click **Properties**, click the **Security** tab.

<img width="673" height="474" alt="1" src="https://github.com/user-attachments/assets/8344414f-9197-4912-a961-c884d3c9ea24" />

3. Click **Advanced**, then click the **Auditing** tab.

<img width="901" height="499" alt="2" src="https://github.com/user-attachments/assets/28886534-994a-4376-957c-b30ff0e85016" />

4. Click **Add**. For **Principal**, selected **`Finance-Sec-G`**.
5. Set **Applies to** to **This folder, subfolders and files**.
6. Clicked **Show advanced permissions**, and checked:
   - Create files / write data
   - Create folders / append data
   - Change permissions
   - Delete
   - Take ownership

<img width="997" height="600" alt="3" src="https://github.com/user-attachments/assets/560ee523-6e79-43ec-afa3-558c61899383" />

7. Clicked **OK**, **OK**.

## Result
**`Finance-Sec-G`**'s activity on the Finance-Folder — file/folder creation, permission changes, deletions, and ownership changes will now generate audit events, since both this SACL and the domain-wide Object Access audit policy are in place.
