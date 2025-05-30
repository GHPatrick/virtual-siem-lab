# Wazuh SIEM Lab Environment

This project sets up a virtual Security Information and Event Management lab using VirtualBox. The lab includes a Wazuh Manager running on Ubuntu, an Ubuntu endpoint agent, and a Windows 10 endpoint agent. All three virtual machines are networked together to simulate a small-scale Security Operations Center (SOC) environment, allowing for hands-on learning in log monitoring, endpoint visibility, and basic threat detection.

---

## Purpose

Designed as a practical learning environment for IT Helpdesk and Cybersecurity fundamentals, this lab demonstrates:

- SIEM deployment and configuration with Wazuh
- Endpoint monitoring on Windows and Linux
- Virtual networking with VirtualBox
- Log forwarding and event visibility

---

## Architecture Diagram

> **Note:** The Wazuh Web UI is accessed directly inside the Wazuh Manager VM.

![wazuh diagram](https://github.com/user-attachments/assets/3a140ed2-3556-40ed-a63d-80b2e028143a)


---

## Lab Components

| Component                      | Description                                        |
|-------------------------------|----------------------------------------------------|
| **VirtualBox Host**           | The physical machine running VirtualBox           |
| **Wazuh Manager (Ubuntu)**    | Central SIEM server and web dashboard (accessed inside VM) |
| **Ubuntu Agent VM**           | Sends system logs to Wazuh Manager                 |
| **Windows 10 Agent VM**       | Sends Windows event logs to Wazuh Manager          |
| **Host-Only Network**         | VirtualBox network for internal VM communication   |

---

## Getting Started

### 1. Prerequisites

- VirtualBox installed
- Ubuntu ISO (for manager and agent)
- Windows 10 ISO (for agent)
- [Wazuh installation guide](https://documentation.wazuh.com/current/installation-guide/index.html)

### 2. VM Setup Steps 

#### Wazuh Manager

- Install Ubuntu Server on a VM
- Install Wazuh Manager and the Web UI
- Launch a browser inside the VM to access Wazuh using your machine's IP address

#### Ubuntu Agent

- Install Ubuntu Desktop or Server on second VM
- Install Wazuh agent
- Configure agent to connect to the manager 

#### Windows Agent

- Install Windows 10 in VirtualBox
- Install Wazuh Windows agent
- Register agent with the manager 

---

## What You Can Do With This Lab

- Monitor real-time logs from Linux and Windows endpoints
- Simulate logon events, system changes, or file modifications and observe alerts
- Explore Wazuh rule sets and decoders
- Practice basic triage and incident detection techniques

---

## Screenshots
> The Wazuh dashboard showing that the Ubuntu and Windows 10 agents are active.

![ubuntu manager dashboard](https://github.com/user-attachments/assets/16860c93-3456-4f25-8b08-632eb54454f5)

> The Ubuntu and Windows 10 agent list in Wazuh.

![wazuh agents](https://github.com/user-attachments/assets/a7a8f045-e83e-480e-9c4c-bcd94f957d1c)

> Here we have an attempted login failure demonstrated in the Ubuntu agent terminal.

![SSH failed login alert ubuntu agent](https://github.com/user-attachments/assets/54944e92-e0c4-4cf9-a561-d9eff9199094)

> Here is the alert caught in Wazuh.

![user login failed](https://github.com/user-attachments/assets/592e48a4-2287-44d1-80c9-197b6fe88c07)






---

## Skills Demonstrated

- Virtualization and system setup (VirtualBox, Ubuntu, Windows)
- SIEM configuration and use (Wazuh)
- Basic Linux/Windows administration
- Log collection and security monitoring

---

## Future Enhancements?

- Add intrusion detection scenario simulations
- Forward logs to an ELK stack or Splunk instance

---

## Why This Project?

I decided on this lab because I wanted to get a hands-on experience of what a SOC Analyst does at a very base level. I approached it to gain a practical understanding of how security data is collected, analyzed, and visualized in real-world environments, starting with tools that are freely available to anyone.
