# Official [Cyber Range](http://joshmadakor.tech/cyber-range) Project

# Vulnerability Management Program Implementation

In this project, we simulate the implementation of a comprehensive vulnerability management program, from inception to completion.

_**Inception State:**_ the organization has no existing policy or vulnerability management practices in place.

_**Completion State:**_ a formal policy is enacted, stakeholder buy-in is secured, and a full cycle of organization-wide vulnerability remediation is successfully completed.

---

<img width="1000" alt="image" src="https://github.com/user-attachments/assets/cfc5dbcf-3fcb-4a71-9c13-2a49f8bab3e6">

# Technology Utilized
- Tenable (enterprise vulnerability management platform)
- Azure Virtual Machines (Nessus scan engine + scan targets)
- PowerShell & BASH (remediation scripts)

---


# Table of Contents

- [Vulnerability Management Policy Draft Creation](#vulnerability-management-policy-draft-creation)
- [Mock Meeting: Policy Buy-In (Stakeholders)](#step-2-mock-meeting-policy-buy-in-stakeholders)
- [Policy Finalization and Senior Leadership Sign-Off](#step-3-policy-finalization-and-senior-leadership-sign-off)
- [Mock Meeting: Initial Scan Permission (Server Team)](#step-4-mock-meeting-initial-scan-permission-server-team)
- [Initial Scan of Server Team Assets](#step-5-initial-scan-of-server-team-assets)
- [Vulnerability Assessment and Prioritization](#step-6-vulnerability-assessment-and-prioritization)
- [Distributing Remediations to Remediation Teams](#step-7-distributing-remediations-to-remediation-teams)
- [Mock Meeting: Post-Initial Discovery Scan (Server Team)](#step-8-mock-meeting-post-initial-discovery-scan-server-team)
- [Mock CAB Meeting: Implementing Remediations](#step-9-mock-cab-meeting-implementing-remediations)
- [Remediation Round 1: Windows OS Updates](#remediation-round-1-windows-os-updates)
- [Remediation Round 2: Guest Account Group Membership](#remediation-round-2-guest-account-group-membership)
- [Remediation Round 3: Outdated Wireshark (Insecure Software)](#remediation-round-3-outdated-wireshark-insecure-software)
- [Remediation Round 4: Disable SMB Signing](#remediation-round-4-disable-smb-signing)
- [Remediation Round 5: RDP Without Network Level Authentication (NLA)](#remediation-round-5-rdp-without-network-level-authentication-nla)
- [Remediation Round 6: Weak LAN Manager Authentication Level](#remediation-round-6-weak-lan-manager-authentication-level)
- [First Cycle Remediation Effort Summary](#first-cycle-remediation-effort-summary)

---

### Vulnerability Management Policy Draft Creation

This phase focuses on drafting a Vulnerability Management Policy as a starting point for stakeholder engagement. The initial draft outlines scope, responsibilities, and remediation timelines, and may be adjusted based on feedback from relevant departments to ensure practical implementation before final approval by upper management.  
[Draft Policy](https://docs.google.com/document/d/1CLSWm1_9JL1oUqgyNNwtPXW6FzXJ7ddVnSAUQTyqC8I/edit?usp=drive_link)

---

### Step 2) Mock Meeting: Policy Buy-In (Stakeholders)

In this phase, a meeting with the server team introduces the draft Vulnerability Management Policy and assesses their capability to meet remediation timelines. Feedback leads to adjustments, like extending the critical remediation window from 48 hours to one week, ensuring collaborative implementation.

<a href='https://www.youtube.com/watch?v=cFDgyuvhBlY' target="_"><img width="600" alt="image" src="https://github.com/user-attachments/assets/549d21f4-26c2-412d-9117-d7b6835aedbf"></a>

[YouTube Video: Stakeholder Policy Buy-In Meeting](https://www.youtube.com/watch?v=cFDgyuvhBlY)

---

### Step 3) Policy Finalization and Senior Leadership Sign-Off

After gathering feedback from the server team, the policy is revised, addressing aggressive remediation timelines. With final approval from upper management, the policy now guides the program, ensuring compliance and reference for pushback resolution.  
[Finalized Policy](https://docs.google.com/document/d/1rvueLX_71pOR8ldN9zVW9r_zLzDQxVsnSUtNar8ftdg/edit?usp=drive_link)
<div style="text-align: center;">
    <img src="https://github.com/user-attachments/assets/9afcdbc1-0493-4af2-9287-1cb9b8f59b40" alt="image" width="400">
</div>

---

### Step 4) Mock Meeting: Initial Scan Permission (Server Team)

The team collaborates with the server team to initiate scheduled credential scans. A compromise is reached to scan a single server first, monitoring resource impact, and using just-in-time Active Directory credentials for secure, controlled access.  

<a href='https://www.youtube.com/watch?v=ZEw1ZCOlvHY' target="_"><img width="600" alt="image" src="https://github.com/user-attachments/assets/31fe8d0f-636b-475b-8d5a-a2795c183f86"></a>

[YouTube Video: Initial Discovery Scan](https://www.youtube.com/watch?v=ZEw1ZCOlvHY)

---

### Step 5) Initial Scan of Server Team Assets

In this phase, an insecure Windows Server is provisioned to simulate the server team's environment. After creating vulnerabilities, an authenticated scan is performed, and the results are exported for future remediation steps.  

<img width="635" height="820" alt="Scan 1" src="https://github.com/user-attachments/assets/0aa36d2a-61ff-43d3-a17e-c5fa3f8fd1c3" />


[Scan 1 - Initial Scan](https://drive.google.com/file/d/1dNyc8T26aokkWXR5LGcn-0iy5C6oPidX/view?usp=sharing)




---

### Step 6) Vulnerability Assessment and Prioritization

We assessed vulnerabilities and established a remediation prioritization strategy based on ease of remediation and impact. The following priorities were set:

1. Windows OS Updates (Re-enable and apply updates)
2. Guest Account Group Membership (Remove from Administrators)
3. Third-Party Software Removal (Outdated Wireshark)
4. Disable SMB Signing
5. RDP Without Network Level Authentication (NLA)
6. Weak LAN Manager Authentication Level

---

### Step 7) Distributing Remediations to Remediation Teams

The server team received remediation scripts and scan reports to address key vulnerabilities. This streamlined their efforts and prepared them for a follow-up review.  

[Remediation Email](https://github.com/joshmadakor1/lognpacific-public/blob/main/misc/remediation-email.md)

---

### Step 8) Mock Meeting: Post-Initial Discovery Scan (Server Team)

The server team reviewed vulnerability scan results, identifying outdated software, insecure accounts, and deprecated protocols. The remediation packages were prepared for submission to the Change Control Board (CAB). 

<a href="https://www.youtube.com/watch?v=JqIxiWwDDkA" target="_"><img width="600" src="https://github.com/user-attachments/assets/03027c66-5f7c-42d0-b6dd-09d053c040b1"/></a>

[Meeting Video](https://www.youtube.com/watch?v=JqIxiWwDDkA)

---

### Step 9) Mock CAB Meeting: Implementing Remediations

The Change Control Board (CAB) reviewed and approved the plan to remove insecure protocols and cipher suites. The plan included a rollback script and a tiered deployment approach.  

<a href="https://www.youtube.com/watch?v=enqOjUV0-7k" target="_"><img width="600" src="https://github.com/user-attachments/assets/07164e63-fbce-471a-b469-29a6d41b7bb8"/></a>

[Meeting Video](https://www.youtube.com/watch?v=enqOjUV0-7k)

---
### Step 10 ) Remediation Effort

#### Remediation Round 1: Windows OS Updates

Windows updates were re-enabled and applied until the system was fully up to date. A follow-up scan verified the changes.  

<img width="483" height="273" alt="Scan 2 - PASSED" src="https://github.com/user-attachments/assets/ce9682e4-f97f-4974-b067-048e111d98da" />

[Scan 2 - Windows OS Updates](https://drive.google.com/file/d/1oJX60-NJ-1xHnc7Es0s4cGOVm6vqxoiR/view?usp=drive_link)


#### Remediation Round 2: Guest Account Group Membership

The server team removed the guest account from the administrator group. A new scan confirmed remediation, and the results were exported for comparison.  

<img width="732" height="217" alt="Scan 3 - PASSED" src="https://github.com/user-attachments/assets/06cbcc85-3f5b-45ac-af32-72133d1546f5" />

[Scan 3 - Guest Account Group Removal](https://drive.google.com/file/d/1PFk99NHiRI8HjTdOML1FlXxAJgDYcM1z/view?usp=sharing)


#### Remediation Round 3: Outdated Wireshark (Insecure Software)

The server team used a PowerShell script to remove outdated Wireshark. A follow-up scan confirmed successful remediation.  

<img width="768" height="464" alt="Scan 4 " src="https://github.com/user-attachments/assets/ca0dc272-0107-4169-bec3-0722ada6cb2a" />

[Scan 4 - Third Party Software Removal](https://drive.google.com/file/d/1Kxuu94vrOjxUg877kuc7emvRpebxbwu2/view?usp=sharing)


#### Remediation Round 4: Disable SMB Signing

SMB Signing was enabled on the server to enforce message authentication and prevent man-in-the-middle attacks. A follow-up scan confirmed successful remediation.  

<img width="772" height="418" alt="Scan 5" src="https://github.com/user-attachments/assets/3ff7d567-76d3-4f48-9add-b95608dd5b74" />

[Scan 5 - SMB Signing Remediation](https://drive.google.com/file/d/141rh9HTfvl3whHV5f5PTTN78e4Lw7ULD/view?usp=drive_link)


#### Remediation Round 5: RDP Without Network Level Authentication (NLA)

Network Level Authentication (NLA) was enabled for Remote Desktop connections to require authentication before a session is established. A follow-up scan confirmed successful remediation.  

<img width="785" height="384" alt="Scan 6" src="https://github.com/user-attachments/assets/a2a0e86e-60ca-4342-82db-6696847da3a4" />

[Scan 6 - RDP NLA Remediation](https://drive.google.com/file/d/1SLP0PyHgNcaCjeTElQjGpTfCmkjuE509/view?usp=drive_link)


#### Remediation Round 6: Weak LAN Manager Authentication Level

The LAN Manager authentication level was configured to only allow NTLMv2 responses and refuse LM and NTLM. A follow-up scan confirmed successful remediation.  

<img width="782" height="357" alt="Scan 7" src="https://github.com/user-attachments/assets/e98566c1-ff3b-4349-82ed-d2c6f3aafdae" />

[Scan 7 - LAN Manager Authentication Remediation](https://drive.google.com/file/d/1Ra9dBBUSqF0CPm3pGZEO6hq7CEDtLuZc/view?usp=drive_link)

---

### First Cycle Remediation Effort Summary

The remediation process reduced total vulnerabilities by 81%, from 26 to 5. Critical vulnerabilities were fully resolved (100%), and high vulnerabilities dropped from 8 to 1 (88% reduction). Medium vulnerabilities were reduced from 15 to 3 (80% reduction). The remaining vulnerabilities (SQLite, Microsoft Edge, SSL certificates, and ICMP Timestamp) will be addressed in the next remediation cycle. In an actual production environment, asset criticality would further guide future remediation efforts.

<img width="623" height="388" alt="image" src="https://github.com/user-attachments/assets/da9d11ee-8447-43b3-870a-7e6f696b3b8e" />

[Remediation Data](https://docs.google.com/spreadsheets/d/1FTtFfZYmFsNLU6pm8nTzsKyKE-d2ftXzX_DPwcnFNfA/edit?gid=0#gid=0)

---

### On-going Vulnerability Management (Maintenance Mode)

After completing the initial remediation cycle, the vulnerability management program transitions into **Maintenance Mode**. This phase ensures that vulnerabilities continue to be managed proactively, keeping systems secure over time. Regular scans, continuous monitoring, and timely remediation are crucial components of this phase. (See [Finalized Policy](https://docs.google.com/document/d/1rvueLX_71pOR8ldN9zVW9r_zLzDQxVsnSUtNar8ftdg/edit?usp=drive_link) for scanning and remediation cadence requirements.)

Key activities in Maintenance Mode include:
- **Scheduled Vulnerability Scans**: Perform regular scans (e.g., weekly or monthly) to detect new vulnerabilities as systems evolve.
- **Patch Management**: Continuously apply security patches and updates, ensuring no critical vulnerabilities remain unpatched.
- **Remediation Follow-ups**: Address newly identified vulnerabilities promptly, prioritizing based on risk and impact.
- **Policy Review and Updates**: Periodically review the Vulnerability Management Policy to ensure it aligns with the latest security best practices and organizational needs.
- **Audit and Compliance**: Conduct internal audits to ensure compliance with the vulnerability management policy and external regulations.
- **Ongoing Communication with Stakeholders**: Maintain open communication with teams responsible for remediation, ensuring efficient coordination.

By maintaining an active vulnerability management process, organizations can stay ahead of emerging threats and ensure long-term security resilience.
