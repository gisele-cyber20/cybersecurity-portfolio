# Log Analysis Project – Linux Authentication Investigation

## Objective
The objective of this project was to analyze Linux authentication logs to identify failed login attempts and determine whether suspicious activity (such as brute-force attacks) was occurring.

---

## Environment
- OS: Ubuntu / RHEL (specify yours)
- Log file analyzed: /var/log/auth.log
- Tools used: grep, cat, wc
- Lab: Local VM inside VirtualBox

---

## Step 1 – Generate Failed Login Attempts
To simulate suspicious behavior, I attempted multiple failed SSH logins:


---

## Step 2 – Review Authentication Logs


---

## Step 3 – Filter Failed Password Attempts

---

## Step 4 – Count Failed Attempts


---

## Findings

- Multiple failed login attempts were recorded
- The logs show:
  - Timestamp
  - Username attempted
  - Source IP address
  - Authentication failure reason
- Repeated failed attempts could indicate brute-force activity

---

## Security Analysis

If this activity were observed in a production environment, I would:

- Identify the source IP address
- Check if attempts are automated (high frequency)
- Block malicious IP using firewall rules
- Implement fail2ban to prevent brute-force attacks
- Review SSH configuration for hardening

---

## Lessons Learned

- Linux authentication logs provide detailed evidence of login activity
- grep is powerful for log filtering
- Repeated failed logins are a key indicator of brute-force attempts
- Log analysis is critical for early detection of security incidents
