# 01 – Troubleshoot and Resolve Domain Controller Internet Connectivity Issue

## Overview

During the configuration of the Windows Server 2019 Domain Controller (**OTCS-SRV-DC01**), the server was unable to access the internet.

This issue prevented access to external resources such as websites.

This document outlines the troubleshooting process, root cause, and resolution.

Note: Windows-2019-SRV VM is the OTCS-SRV-DC01

---

# Problem

The Domain Controller(**OTCS-SRV-DC01**) could not access the internet.

### Symptoms:

<img width="713" height="502" alt="TS1" src="https://github.com/user-attachments/assets/a14bbf93-95b5-4dea-9b00-21ac2b8f2906" />

I searched for youtube on Google Chrome (on the Production server(**OTCS-SRV-DC01**)
- Site couldnt be reached
- DNS address could not be found

1. The Windows-2019-SRV VM is connected to OTCS-SW (a virtual switch [Hyper-V external]).
<img width="256" height="132" alt="TS2" src="https://github.com/user-attachments/assets/e307dcfb-0a4d-4f43-ab3d-559b28225a9d" />

2. Clicked on the Ethernet Logo at the bottom right (note the triangle exclamation sign [warning sign])
<img width="367" height="221" alt="TS3" src="https://github.com/user-attachments/assets/a3220c38-846d-4418-abc4-7e65c85bfbc1" />

<img width="573" height="359" alt="TS4" src="https://github.com/user-attachments/assets/92c52325-2e88-44fc-9667-b1355e1c0308" />























