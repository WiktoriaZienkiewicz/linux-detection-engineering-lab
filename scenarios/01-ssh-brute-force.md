SSH Brute-Force Detection

Objective

The objective of this scenario is to detect multiple failed SSH login attempts originating from the same source.

Environment

Ubuntu Linux
OpenSSH
Wazuh

Log source

/var/log/auth.log

Detection idea

Generate several failed SSH login attempts and analyse the authentication logs. A detection rule will identify repeated failed authentication attempts from the same IP address.

MITRE ATT&CK

T1110 - Brute Force

Possible false positives

A legitimate user entering an incorrect password multiple times.
An automated system using outdated credentials.

Recommended SOC response

Verify the source IP address and affected account.
Check whether a successful login occurred after the failed attempts.
Block the source address if malicious activity is confirmed.

Status

Not started.
