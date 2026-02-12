# Linux Hardening & Security Audit with Lynis (Ubuntu)

## Objective
Perform a baseline security audit on Ubuntu using Lynis, apply hardening actions, and validate improvements through a post-hardening audit.

## Environment
- OS: Ubuntu (dual boot)
- Tool: Lynis
- Focus: Security hardening, baseline vs post-hardening comparison

## Baseline Scan Results
- Hardening Index: 67
- Key issues detected:
  - Time sync (NTP) not updated recently
  - Vulnerable/outdated packages
  - MongoDB warning (related to old Rocket.Chat snap service)

## Hardening Actions Applied
1. Enabled firewall (UFW)
2. Enabled and configured Fail2ban
3. Installed malware scanner (ClamAV) and enabled signature updates
4. Enabled time synchronization (systemd-timesyncd)
5. Updated system packages and removed vulnerable/outdated packages
6. Removed outdated third-party repositories (MongoDB 4.4 repo)

## Post-Hardening Scan Results
- Hardening Index: 71
- Firewall: Enabled ✅
- Malware scanner: Enabled ✅

## Evidence
- `baseline/` includes initial audit logs and report
- `post-hardening/` includes final audit logs and report


## Key Takeaways
- Lynis provides a structured methodology for Linux hardening.
- Even small changes (time sync, updates, firewall, malware scanning) significantly improve system security posture.
- Evidence-based remediation is essential for real-world security work.

