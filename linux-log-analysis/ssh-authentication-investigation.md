# Linux Log Analysis – SSH Authentication Investigation

## Project Overview

This project demonstrates how Linux authentication logs can be analyzed to detect suspicious login activity.

A Linux virtual machine was used to simulate failed SSH login attempts. The authentication logs were then reviewed using command-line tools to identify potential brute-force activity.

This investigation replicates a basic Security Operations Center (SOC) task where analysts review system logs to detect unauthorized access attempts.

---

## Lab Environment

Operating System: Red Hat Enterprise Linux (RHEL) VM  
Virtualization Platform: VirtualBox  
Log File Analyzed: `/var/log/secure`  
Service Investigated: SSH (Secure Shell)

---

## Tools Used

- ssh
- systemctl
- ss
- grep
- wc
- Linux terminal

---

# Step 1 – Verify SSH Service Status

The SSH service was verified to ensure it was running on the system.

### Command Used

```bash
systemctl status sshd
Explanation
This command checks whether the OpenSSH server daemon is active and able to accept incoming SSH connections.
Expected Result
The output confirms that the SSH service is active (running).
Step 2 – Verify SSH Listening Port
Next, the system was checked to confirm that SSH is listening for connections.
Command Used
ss -tulpn
Explanation
This command lists all listening ports and the services associated with them.
Result
The output confirmed that SSH was listening on:
TCP port 22
Step 3 – Simulate Failed SSH Login Attempts
To simulate suspicious activity, several login attempts were made using an invalid username.
Command Used
ssh fakeuser@localhost
Result
The system rejected the login attempts and generated authentication failures.
Example output:
Permission denied (publickey,password).
This behavior simulates a brute-force login attempt targeting the SSH service.
Step 4 – Review Authentication Logs
Linux authentication logs were examined to identify failed login attempts.
Command Used
sudo cat /var/log/secure
Explanation
This command displays the authentication log where SSH login events are recorded.
Example log entry:
Failed password for invalid user fakeuser from ::1 port 53918 ssh2
These log entries confirm that authentication attempts were unsuccessful.
Step 5 – Filter Failed Login Attempts
To isolate failed login attempts, the log file was filtered using grep.
Command Used
sudo grep "Failed password" /var/log/secure
Explanation
The grep command searches for lines containing the phrase Failed password, allowing analysts to quickly locate authentication failures.
Step 6 – Count Failed Login Attempts
To quantify suspicious activity, the number of failed login attempts was counted.
Command Used
sudo grep "Failed password" /var/log/secure | wc -l
Result
25 failed login attempts detected
Counting failed authentication attempts helps identify potential brute-force attacks.
Findings
The investigation identified multiple failed login attempts targeting the SSH service.
All attempts used an invalid username and originated from the localhost system, confirming that the activity was simulated within the lab environment.
Repeated authentication failures like these could indicate:
brute-force password attacks
automated login attempts
unauthorized access attempts
Security Recommendations
To reduce the risk of SSH attacks, the following security measures are recommended:
• Disable password authentication and use SSH key-based authentication
• Install fail2ban to block repeated failed login attempts
• Restrict SSH access using firewall rules
• Change the default SSH port
• Enable multi-factor authentication (MFA)
Skills Demonstrated
Linux administration
Security log analysis
Threat detection
Command-line investigation
Incident response methodology
Conclusion
This project demonstrates how Linux authentication logs can be analyzed to detect suspicious login activity.
Understanding how to investigate system logs is an essential skill for cybersecurity professionals working in Security Operations Centers (SOC).
Through this investigation, failed SSH login attempts were simulated, identified in system logs, and analyzed using Linux command-line tools.
