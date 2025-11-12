# 📈 Project Progress Tracking



---



## Phase 1: pfSense ✅



- [x] pfSense VM deployed and booted

- [x] Network interfaces configured (WAN, LAN, Management)

- [x] Access pfSense Web Interface

- [x] Change Default Admin Password

- [x] DHCP server enabled for lab network

- [x] SSH access working

- [x] Firewall Rules Setup

- [x] Enable Logging and Packet Capture

- [x] Kali Linux VM deployed and network connected

- [x] Internet connectivity verified through pfSense



**Completed**



---



## Phase 2: Security Onion 🔄



- [x] Download Security Onion ISO and verify checksum

- [x] Create Security Onion VM with proper specs (16GB RAM, 4 CPU and dual NIC)

- [x] Install Security Onion in standalone mode

- [x] Run so-setup and configure management interface

- [ ] Configure Suricata with default rules

- [ ] Test alert generation with EICAR file

- [ ] Install Splunk Universal Forwarder

- [ ] Verify logs flowing to Splunk

- [ ] Document any issues faced



**In Progress**



---



## Phase 3: Splunk SIEM ⏳



- [ ] Deploy Splunk server VM

- [ ] Apply for Splunk Developer license (50GB/day)

- [ ] Configure pfSense syslog forwarding

- [ ] Create Splunk indexes (firewall, securityonion, wazuh)

- [ ] Test log ingestion from pfSense

- [ ] Test log ingestion from Security Onion

- [ ] Create basic dashboard

- [ ] Create test alerts



**Planned**



---



## Phase 4: Endpoint Security ⏳



- [ ] Deploy Wazuh Manager VM

- [ ] Run Wazuh installation script

- [ ] Deploy Wazuh agent to Windows VM

- [ ] Verify agent connectivity

- [ ] Install Splunk UF on Wazuh Manager

- [ ] Test Wazuh alert ingestion in Splunk

- [ ] Configure basic active response rule



**Planned**



---



## Phase 5: Advanced Features ⏳



- [ ] Add SPAN port configuration (traffic mirroring)

- [ ] Tune Suricata with real traffic

- [ ] Create correlation rules in Splunk

- [ ] Build comprehensive dashboards

- [ ] Test incident response workflows

- [ ] Simulate attack scenarios

- [ ] Document lessons learned



**Planned**



---



\## Issues \& Solutions Discovered



\### Issue 1: pfSense DHCP not assigning IPs

\*\*Solution\*\*: Checked firewall rules, added pass rule for LAN traffic



\### Issue 2: No access to Security Onion web interface

\*\*Solution\*\*: Ongoing troubleshooting



---



\## Key Learnings



1\. VirtualBox promiscuous mode is critical for traffic mirroring

2\. DHCP pool must not overlap with static IPs

3\. Always document network settings (IPs, ports, credentials)

4\. Test connectivity after each major configuration change



---



\## Next Steps



1\. Complete Security Onion installation (current phase)

2\. Validate traffic generation with ping/curl

3\. Move to Splunk deployment

4\. Test all integrations before advanced features



---



\*\*Last Updated\*\*: 12.11.2025

\*\*Overall Completion\*\*: ~30%

