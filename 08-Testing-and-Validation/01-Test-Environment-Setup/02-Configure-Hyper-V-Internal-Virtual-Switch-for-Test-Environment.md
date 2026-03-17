# 02 – Configure Hyper-V Internal Virtual Switch for Test Environment

## Overview

To prevent interference with the production network, the test server environment will be connected to an **isolated internal virtual network**.

I will create an **Internal Virtual Switch** in Hyper-V and connecet the TST-AD-SRV VM to it. This allows communication between the host and the TST-AD-SRV VM while keeping the testing environment separated from the production network.

