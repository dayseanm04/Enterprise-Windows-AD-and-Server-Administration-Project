# Configure File and Folder Auditing

## Overview
Turning on Object Access auditing at the GPO level doesn't log anything by itself, it just tells Windows to *pay attention* to file activity. To actually get events in the log, I still have to tell Windows which folder to watch and what actions on it count as worth logging. I'm setting this up on the Finance-Folder, since that's the folder I want to track changes on.

## Set Up Auditing on the Finance-Folder
1. Open File Explorer → **This PC** → **Local Disk (C:)** → `shared-folders`.
2. Right-click **Finance-Folder**, click **Properties**, click the **Security** tab.

<img width="673" height="474" alt="1" src="https://github.com/user-attachments/assets/8344414f-9197-4912-a961-c884d3c9ea24" />

3. Click **Advanced**, then click the **Auditing** tab.

<img width="901" height="499" alt="41" src="https://github.com/user-attachments/assets/28886534-994a-4376-957c-b30ff0e85016" />

4. Click **Add**. For **Principal**, selected **`Finance-Sec-G`**.
5. Set **Applies to** to **This folder, subfolders and files**.
