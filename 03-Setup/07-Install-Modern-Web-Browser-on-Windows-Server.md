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



