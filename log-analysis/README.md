# Linux Log Analysis – SSH Authentication Investigation

## Project Overview

This project demonstrates how Linux authentication logs can be analyzed to detect suspicious login activity and investigate potential brute-force attacks.

A Linux virtual machine was used to simulate failed SSH login attempts. System logs were then reviewed using command-line tools to identify authentication failures and analyze the activity recorded in the logs.

This investigation replicates a basic **Security Operations Center (SOC)** log analysis task commonly performed by cybersecurity analysts.

---

## Lab Environment

| Component | Details |
|-----------|--------|
| Operating System | Linux VM (RHEL based) |
| Virtualization | VirtualBox |
| Log File Analyzed | `/var/log/secure` |
| Service Investigated | SSH (Secure Shell) |

### Tools Used

- ssh
- grep
- wc
- ss
- systemctl

---

# Step 1 – Verify SSH Service Status

The SSH service was verified to confirm it was running.

```bash
systemctl status sshd
