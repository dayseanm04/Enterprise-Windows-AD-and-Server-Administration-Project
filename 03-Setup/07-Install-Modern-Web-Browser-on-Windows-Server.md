# 07 – Install Modern Web Browser on the Windows Server 2019

## Overview

By default, Windows Server 2019 includes Internet Explorer for legacy application compatibility.  
However, Internet Explorer is not suitable for modern web administration tools such as:

- Windows Admin Center  
- Cloud-based management portals  

To ensure compatibility with modern web technologies, I will install a modern browser such as **Google Chrome**.

---

#  Internet Explorer Enhanced Security Configuration (IE ESC)

**Internet Explorer Enhanced Security Configuration (IE ESC)** is enabled by default Windows 2019 Server.

IE ESC restricts access to most websites and blocks many downloads.  
To install a modern browser, IE ESC must be temporarily disabled.

---

# Step 1 – Disable IE Enhanced Security Configuration
1. Open **Server Manager**
2. Click **Local Server**
3. Look For **IE Enhanced Security Configuration**

<img width="1116" height="375" alt="5" src="https://github.com/user-attachments/assets/414cc9a8-c190-44f2-b852-3f4527d6de23" />

4. Click the hyperlink (typically shows "On")
5. Set the following:
   - **Administrators:** Off  
   - **Users:** Off 

<img width="412" height="448" alt="6" src="https://github.com/user-attachments/assets/38c7ea67-f991-4c09-b787-e1ed85dc3d44" />
6. Click **OK**

# Step 2 – Download a Modern Web Browser

1. Open **Internet Explorer**
2. Go to https://www.google.com/chrome/
3. Download the installer
4. Run the executable

<img width="844" height="222" alt="9" src="https://github.com/user-attachments/assets/a0bf8777-b8e0-44f5-aae8-a17a81d0328a" />

# Step 3 – Set Default Browser 

After installation:

1. Open **Settings**
2. Navigate to **Default Apps**
3. Set the newly installed browser as the default web browser

#  Step 4 – Re-Enable IE Enhanced Security Configuration

For security best practices, re-enable IE ESC after installing the browser.

1. Open **Server Manager**
2. Click **Local Server**
3. Click **IE Enhanced Security Configuration**
4. Set:
   - **Administrators:** On  
   - **Users:** On

5. Click **OK**
