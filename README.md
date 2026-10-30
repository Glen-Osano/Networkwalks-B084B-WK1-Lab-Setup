# Networkwalks-B084B-WK1-Lab-Setup

<div align="center">

# 🐉 Kali Linux Virtual Lab Setup

**Setting up a lightweight, isolated virtual environment for cybersecurity practice using Oracle VirtualBox and Kali Linux.**

</div>

<p align="center">
  <img src="https://img.shields.io/badge/Skill-Cybersecurity-404040?style=flat-square&labelColor=C00000" />
  <img src="https://img.shields.io/badge/Hypervisor-VirtualBox-0070C0?style=flat-square&labelColor=000000" />
  <img src="https://img.shields.io/badge/OS-Kali%20Linux-E87500?style=flat-square&labelColor=000000&logo=kalilinux&logoColor=white" />
  <img src="https://img.shields.io/badge/Skill-Virtualization-404040?style=flat-square&labelColor=C00000" />
  <img src="https://img.shields.io/badge/GitHub-404040?style=flat-square&labelColor=0070C0&logo=github&logoColor=white" />
  <img src="https://img.shields.io/badge/Ethical%20Hacking-E87500?style=flat-square&labelColor=000000&logo=kalilinux&logoColor=white" />
</p>

---

## 📌 Project Overview

This project documents the step-by-step installation and initial configuration of a **Kali Linux virtual machine** using **Oracle VM VirtualBox**. 

The goal of this assignment is to establish a working virtual environment to safely practice ethical hacking, Linux administration, and security testing operations.

---

## 🎯 Objectives

- Download and install Oracle VM VirtualBox.
- Download the official Kali Linux virtual machine image.
- Import and configure the Kali Linux VM inside VirtualBox.
- Verify system boot, core utilities, and initial network access.
- Document the installation process for future lab expansions.

---

## 🛡️ Purpose of the Lab

This virtual machine serves as an isolated testbed for hands-on learning in cybersecurity. Having a dedicated virtual machine allows for safe experimentation without altering or risking the host operating system.

⚠️ **Disclaimer:** This lab environment is strictly intended for educational purposes and authorized security testing only.

---

## ⚙️ Lab Environment Specs

| 🧩 Component         | ⚙️ Details / Configuration           |
| :------------------- | :---------------------------------- |
| 🖥️ Host System       | Windows / macOS                     |
| 🧰 Hypervisor        | Oracle VM VirtualBox                |
| 🐉 Guest OS          | Kali Linux                          |
| 🧠 Allocated RAM     | 2048 MB (2 GB)                      |
| ⚡ Allocated Processors| 2 Cores                            |
| 💾 Storage           | Dynamic VDI (~20 GB)                |
| 🌐 Network Mode      | NAT / Bridged                       |

---

# 🪜 Step-by-Step Setup Guide

### Step 1: Download & Install Oracle VM VirtualBox

1. Downloaded the latest installer for Oracle VM VirtualBox from the official website.
2. Ran the setup wizard, accepting default feature selections and network driver installations.
3. Successfully launched VirtualBox Manager.

![](image-1-virtualbox-download.png)

---

### Step 2: Download Kali Linux

1. Navigated to the official Kali Linux website (`kali.org`).
2. Selected the pre-built Virtual Machine image (or ISO installer) tailored for VirtualBox.

![](image-2-kali-download.png)

---

### Step 3: Import & Configure Virtual Machine in VirtualBox

1. Opened VirtualBox Manager and imported/created the new virtual machine for Kali Linux.
2. Configured hardware resources:
   - **Base Memory:** Assigned 2048 MB RAM.
   - **Processors:** Allocated 2 CPU cores.
   - **Network:** Set to NAT for standard outbound internet access.

![](image-3-kali-vm-settings.png)

---

### Step 4: Launch Kali Linux & Initial System Check

1. Powered on the Kali Linux virtual machine.
2. Logged into the deskop environment using default credentials (`kali` / `kali`).
3. Opened the terminal to verify network connectivity and system uptime.

![](image-4-kali-desktop-boot.png)

---

# 🔎 Verification & Testing

To confirm that the virtual machine setup was completed successfully, the following basic checks were executed inside the Kali Linux terminal:

| ✅ Check                      | 🧾 Command Executed | 🎯 Target Result              |
| :-------------------------- | :------------------ | :---------------------------- |
| 🌐 Verify IP Configuration  | `ip a`              | Network adapter receives IP   |
| 📡 Test Outbound Connection | `ping -c 4 8.8.8.8` | 0% packet loss                |
| 🔎 Test DNS Resolution      | `ping -c 4 google.com` | Hostname resolves successfully |

```text
# Sample Output Verification
$ ip a
eth0: flags=4163<UP,BROADCAST,RUNNING,MULTICAST>  mtu 1500
        inet 10.0.2.15  netmask 255.255.255.0  broadcast 10.0.2.255
