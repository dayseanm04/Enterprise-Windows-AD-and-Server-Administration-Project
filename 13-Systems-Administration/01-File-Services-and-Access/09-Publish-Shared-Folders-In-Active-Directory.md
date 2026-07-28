# Publish Shared Folders in Active Directory

## Overview
Users can already get to the shared folders through the network path directly, but publishing them in Active Directory makes them easier to find — users can search for a shared folder by name right from Active Directory instead of needing to know the exact server and path. This also sets up the mapped network drives so each department gets quick access to their folder.

## Create a Shared Folder Object in Active Directory

1. Open **Active Directory Users and Computers**.
2. Expand Domain
3. Click the **Users-OU**.
4. Click the **IT** OU.
5. Right-click an empty space → **New** → **Shared Folder**.
6. Entered the folder's name and its network path.

<img width="441" height="374" alt="1" src="https://github.com/user-attachments/assets/362cd0b0-9c48-4fad-b23f-d24bc89c244d" />

<img width="611" height="413" alt="2" src="https://github.com/user-attachments/assets/e25e1229-1c37-4036-b672-b8fbeb1ce167" />

## Verify with Active Directory Search

Logged in as **`d.moore`** to confirm the shared folder shows up for a regular user, not just from the admin account.

