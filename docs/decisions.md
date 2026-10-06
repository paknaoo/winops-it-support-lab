# Design Decisions

## D-001 - Lab management from the host via the MGMT segment only

**Context:** OPNsense GUI must be reachable before any lab workstation exists (WKS-001 is built in phase 9), while rules and DHCP relay are configured earlier.

**Decision:** The host has a virtual adapter only on VMnet40 (MGMT, 10.20.40.1). USERS, SERVERS and BACKUP have no host adapter. In OPNsense the LAN interface is assigned to MGMT, so the default anti-lockout rule protects GUI access there.

**Alternatives considered:** Temporary host adapter on USERS - rejected: exposes the firewall GUI on the user segment and lets the host bypass the firewall into a production-like network.

**Consequences:** Management plane is separated from users. Host traffic into other segments is subject to firewall rules. MGMT is shared later with PRTG01 (repo 2) and WAZUH01 (repo 3).
