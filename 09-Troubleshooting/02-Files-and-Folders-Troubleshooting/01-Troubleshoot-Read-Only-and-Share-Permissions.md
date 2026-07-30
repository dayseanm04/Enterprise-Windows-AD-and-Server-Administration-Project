# Troubleshooting Read-Only and Share Permissions

Found while testing file and folder permissions in [02-Test-HR-Folder-Access.md](../../08-Testing-and-Validation/05-File-Folder-Permission-Tests/02-Test-HR-Folder-Access.md).

## Verify the Issue
Opened the HR-Folder and tried to edit one of the files:

logged in as emma davis

<img width="481" height="134" alt="1" src="https://github.com/user-attachments/assets/29c31fc8-f436-40dc-9c84-74f1a7062019" />

Opened **`hiring-doc.txt`**:

<img width="562" height="384" alt="2" src="https://github.com/user-attachments/assets/b22aae38-1532-4b0e-a884-18059b436253" />

Wrote **"More Data via emma davis"** and hit Ctrl+S to save:

<img width="721" height="551" alt="3" src="https://github.com/user-attachments/assets/62625c06-8509-435a-89c2-7752f43293f5" />

Clicked **Save**

It said **`hiring-doc.txt`** already exists do I want to replace it? Clicked **Yes**.

Clicked **Yes**

<img width="724" height="623" alt="4" src="https://github.com/user-attachments/assets/2dcc6b19-99c6-425f-a4df-d1d37f9a76b7" />

It then said: ***"hiring-doc, this file is set to read-only. Try again with a different file name."***

<img width="717" height="511" alt="5" src="https://github.com/user-attachments/assets/fcbcb6f8-0bf6-45d8-b3d8-6e27988abbfb" />

## Fix 1: Remove the Read-Only Attribute

Logged in as **Administrator**

<img width="530" height="242" alt="6" src="https://github.com/user-attachments/assets/5b6706c2-4466-4a02-a2ce-d448bac39ebf" />

Opened File explorer and went to `C:\shared-folders`.

Right-clicked the **HR-Folder**, unchecked **Read-only**, clicked **OK**, then confirmed **Apply changes to this folder, subfolders and files**, and clicked **OK** again.

<img width="725" height="646" alt="7" src="https://github.com/user-attachments/assets/603fab7b-aeff-4b24-a255-f88e3cd4e57f" />

Opened the HR-Folder, and did the same for **`hiring-doc.tx**t` and **`onboarding-doc.txt`**, and unchecked **Read-only** on both.

### Verify Fix 1
Logged back in as `e.davis`:

<img width="481" height="134" alt="8" src="https://github.com/user-attachments/assets/29c31fc8-f436-40dc-9c84-74f1a7062019" />

Opened File Explorer → Network → `OTCS-DC01` → HR-Folder → `hiring-doc.txt`, added "new data by emma davis", and pressed Ctrl+S.

Hit Ctrl+S to save:

<img width="520" height="329" alt="9" src="https://github.com/user-attachments/assets/6debd66c-d41c-4609-92f3-e9c302fd31d9" />

<img width="707" height="594" alt="10" src="https://github.com/user-attachments/assets/4e3a1772-e211-4ac1-9bdd-2e8599b42738" />

Clicked **Save**:

<img width="723" height="679" alt="11" src="https://github.com/user-attachments/assets/14724d45-2296-44c9-a418-8266a9a8a461" />

Clicked **Yes** to replace the existing file but this time got a different error:

<img width="832" height="580" alt="12" src="https://github.com/user-attachments/assets/b4577fd0-f0da-4a7b-a1ce-45ac4a038165" />

Clicked **OK**, but still couldn't save the changes. So the read-only fix wasn't the whole problem.

## Fix 2: Configure Share Permissions
Logged back in as **Administrator**:

<img width="530" height="242" alt="13" src="https://github.com/user-attachments/assets/5b6706c2-4466-4a02-a2ce-d448bac39ebf" />

Opened File Explorer → Network → `OTCS-DC01`, right-clicked the **HR-Folder**, and clicked **Properties**.

<img width="554" height="426" alt="14" src="https://github.com/user-attachments/assets/892ebdab-0903-4a00-8d71-0835970d5a84" />

Clicked the **Sharing** tab:

<img width="554" height="426" alt="Screenshot 2026-07-29 172445" src="https://github.com/user-attachments/assets/b4c231e0-32c4-4f6e-9f13-96327dc0e39b" />

Clicked the **Advanced Sharing...** tab:

<img width="565" height="440" alt="Screenshot 2026-07-29 172537" src="https://github.com/user-attachments/assets/ffdec628-b726-486c-9359-2def64c50efd" />

