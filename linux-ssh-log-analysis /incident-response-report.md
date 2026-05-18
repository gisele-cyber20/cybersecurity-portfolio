# Incident Response Report: Suspicious SSH Login Activity

## Summary

This report reviews suspicious SSH login activity based on failed login attempts. The goal is to identify possible brute-force behavior, document evidence, and recommend security actions.

## Findings

- Multiple failed login attempts were observed.
- Repeated login failures may indicate password guessing or brute-force activity.
- SSH access should be monitored closely because it can provide remote access to a system.

## Risk

If an attacker successfully guesses valid credentials, they may gain unauthorized access to the system.

## Recommended Actions

- Enforce strong passwords.
- Disable root login over SSH.
- Use multi-factor authentication when possible.
- Limit SSH access to trusted IP addresses.
- Review logs regularly.
- Consider account lockout rules after repeated failed attempts.

## What I Learned

This project helped me practice reviewing security logs, identifying suspicious activity, documenting findings, and recommending next steps.

## How This Applies to a Cybersecurity Role

This connects to SOC and security analyst work because analysts review alerts, investigate activity, document evidence, and recommend actions to reduce risk.
