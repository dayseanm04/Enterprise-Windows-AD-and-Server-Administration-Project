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

Logged in as **Administrator** and went to `C:\shared-folders`.

<img width="530" height="242" alt="6" src="https://github.com/user-attachments/assets/5b6706c2-4466-4a02-a2ce-d448bac39ebf" />
