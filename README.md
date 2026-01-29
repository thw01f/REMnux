# REMnux
REMnux® is a Linux toolkit for reverse-engineering and analyzing malicious software. REMnux provides a curated collection of free tools created by the community. Analysts can use it to investigate malware without having to find, install, and configure the tools.

# REMnux Installation 

This guide covers two installation methods:
1.  **VirtualBox** (Recommended for Windows/Mac/Linux hosts)
2.  **KVM / Virt-Manager** (Recommended for Linux hosts)


## Table of Contents
1. [Method 1: VirtualBox Installation](#method-1-virtualbox-installation)
2. [Method 2: KVM (Virt-Manager) Installation](#method-2-kvm-virt-manager-installation)
3. [Post-Installation: Updates](#post-installation-keeping-remnux-updated)


## Method 1: VirtualBox Installation

**1. Go to the Website:**
Visit [remnux.org](https://remnux.org).
![Home Page](https://raw.githubusercontent.com/thw01f/REMnux/main/REMnux_pic/1.png)

**2. Get the Distro:**
Navigate to the "Get the REMnux Distro" section.
![Get Distro](https://raw.githubusercontent.com/thw01f/REMnux/main/REMnux_pic/2.png)

**3. Download Options:**
You will see options for different platforms.
![Download Page](https://raw.githubusercontent.com/thw01f/REMnux/main/REMnux_pic/3.png)

**4. Download the OVA:**
Select the **VirtualBox OVA** file.
![Download OVA](https://raw.githubusercontent.com/thw01f/REMnux/main/REMnux_pic/4.png)

**5. Import Appliance:**
Open VirtualBox. Go to **File > Import Appliance**.
![Import Menu](https://raw.githubusercontent.com/thw01f/REMnux/main/REMnux_pic/6.png)

**6. Select File:**
Browse to your Downloads folder and select the `.ova` file.
![Select File](https://raw.githubusercontent.com/thw01f/REMnux/main/REMnux_pic/7.png)

**7. Review Settings:**
VirtualBox will show the default configuration (usually 4GB RAM). Click **Finish** (or Import).
![Review Settings](https://raw.githubusercontent.com/thw01f/REMnux/main/REMnux_pic/8.png)

**8. Launch:**
Select the new **REMnux v7** entry and click **Start**.
![Start VM](https://raw.githubusercontent.com/thw01f/REMnux/main/REMnux_pic/9.png)

**9. Boot Up:**
The machine will boot into the desktop environment.
![Desktop](https://raw.githubusercontent.com/thw01f/REMnux/main/REMnux_pic/10.png)
![Desktop Clean](https://raw.githubusercontent.com/thw01f/REMnux/main/REMnux_pic/11.png)

---

## Method 2: KVM (Virt-Manager) Installation
**Best for:** Users running Kali Linux, Ubuntu, or other Linux distros as their host.

**1. Download QCOW2:**
Ensure you have downloaded the **QCOW2** version of REMnux (often listed for Proxmox/KVM) instead of the OVA.
![QCOW2 Download](https://raw.githubusercontent.com/thw01f/REMnux/main/REMnux_pic/5.png)

**2. Create New VM:**
Open **Virtual Machine Manager** and click the **Plus (+)** icon.
![KVM Home](https://raw.githubusercontent.com/thw01f/REMnux/main/REMnux_pic/KVM1.png)

**3. Import Disk:**
Select **"Import existing disk image"** and click Forward.
![Import Disk](https://raw.githubusercontent.com/thw01f/REMnux/main/REMnux_pic/KVM2.png)

**4. Browse Storage:**
Click **Browse** to locate your file.
![Browse](https://raw.githubusercontent.com/thw01f/REMnux/main/REMnux_pic/KVM3.png)

**5. Select Volume:**
Select the location where your images are stored.
![Select Volume](https://raw.githubusercontent.com/thw01f/REMnux/main/REMnux_pic/KVM4.png)

**6. Select Image:**
Select the downloaded `.qcow2` file.
![Select QCOW2](https://raw.githubusercontent.com/thw01f/REMnux/main/REMnux_pic/KVM5.png)

**7. Configure Resources:**
* **OS Type:** Linux / Ubuntu 20.04
* **RAM:** 4096 MB (4GB)
* **CPUs:** 2
![Final Config](https://raw.githubusercontent.com/thw01f/REMnux/main/REMnux_pic/KVM6.png)

**8. Finish:**
Click **Finish**. The VM will boot immediately.
![KVM Boot](https://raw.githubusercontent.com/thw01f/REMnux/main/REMnux_pic/12.png)

---

## Post-Installation: Keeping REMnux Updated

**1. Open Terminal:**
Right-click the desktop and open a terminal.

**2. Run Upgrade Command:**
Type the following command:
```bash
sudo remnux upgrade
