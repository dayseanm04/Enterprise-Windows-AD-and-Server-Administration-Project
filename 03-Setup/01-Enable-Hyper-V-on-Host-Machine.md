# 01 – Enable Hyper-V on Host Machine  

##  Overview  

This step prepares the Windows host machine for virtualization by enabling the **Hyper-V platform feature**.

I will use Hyper-V will to deploy and manage the virtual machines required for this **Enterprise Windows AD & Server Administration Project**, including Windows Server 2019 and client systems.

>  Note: Im building this project using a Windows computer as the host system.

---

##  Objective  

Enable the Hyper-V feature on the Windows host machine so it can support:
- Virtual machine creation
- Virtual networking (virtual Switch)
- Windows Server 2019 deployment

---

##  Prerequisites  

Before enabling Hyper-V, ensure:
- Windows 10/11 Pro, Enterprise, or Education edition  
- Virtualization enabled in BIOS/UEFI  
- Sufficient RAM (recommended 16GB+ for lab environments)  
- Hardware virtualization support (Intel VT-x / AMD-V)

---

## Step-by-Step   

### Step 1 - Open Control Panel  
1. Click **Start**
2. Search for **Control Panel**
3. Click **Open**

<img width="795" height="359" alt="1" src="https://github.com/user-attachments/assets/26504029-a30a-4e68-97bc-7caec83e594b" />

###  Step 2 - Navigate to Programs  
1. In Control Panel, click **Programs**

<img width="780" height="449" alt="2" src="https://github.com/user-attachments/assets/51eff0b2-48f4-4494-bed2-9288b5afc206" />

### Step 3 - Open Programs and Features  
1. Click **Programs and Features** or Click **Turn Windows features on or off**

<img width="780" height="372" alt="3" src="https://github.com/user-attachments/assets/cbe5fd9f-8ab9-49ff-974b-b1f55fad0207" />

###  Step 4 - Turn Windows Features On or Off  
1. Click **Turn Windows features on or off**

<img width="790" height="236" alt="4" src="https://github.com/user-attachments/assets/2d1a34f9-cb3f-42af-98ec-0fc6170f6ee8" />

### Step 5 - Enable Hyper-V  
1. Scroll through the list
2. Find **Hyper-V**
3. Check the box for **Hyper-V**
4. Click **OK**

<img width="717" height="436" alt="5" src="https://github.com/user-attachments/assets/c765a5ef-ad2b-402a-9bb1-a74897abff59" />

###  Step 6 - Restart the Computer
After enabling Hyper-V:
1. Restart the system when prompted
2. Allow Windows to complete feature installation


---

##  Verification

After reboot:

1. Open the **Start Menu**
2. Search for **Hyper-V Manager**

<img width="774" height="296" alt="6" src="https://github.com/user-attachments/assets/c7c3717c-072a-4fb5-a4bc-d860d81d4144" />

The host machine is now prepared to:
- Create and manage virtual machines
- Configure virtual networking  
- Deploy Windows Server 2019  
