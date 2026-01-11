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



## Phase 2: Security Onion ✅



- [x] Download Security Onion ISO and verify checksum

- [x] Create Security Onion VM with proper specs (16GB RAM, 4 CPU and dual NIC)

- [x] Install Security Onion in standalone mode

- [x] Run so-setup and configure management interface

- [x] Established controlled SSH access to the SO VM through VirtualBox port forwarding

- [x] Configure Suricata with default rules

- [x] Validating traffic mirroring with tcpdump

- [x] Test alert generation with EICAR file



**Completed**



---



## Phase 3: Splunk SIEM ✅



- [x] Deploy Splunk server VM

- [x] Apply for Splunk Developer license

- [x] Configure pfSense syslog forwarding

- [x] Create Splunk indexes (firewall, securityonion, wazuh)

- [x] Test log ingestion from pfSense

- [x] Configure Security Onion Forwarder

- [x] Test log ingestion from Security Onion

- [x] Create basic dashboard



**Completed**



---



## Phase 4: Endpoint Security ✅



- [x] Deploy Wazuh Manager VM

- [x] Run Wazuh installation script

- [x] Deploy Wazuh agent to Windows VM

- [x] Verify agent connectivity

- [x] Install Splunk UF on Wazuh Manager

- [x] Test Wazuh alert ingestion in Splunk

- [x] Configure basic active response rule



**Completed**



---



## Phase 5: Microsoft Defender 🔄



- [x] Access Microsoft Defender XDR portal

- [x] Onboard Windows VM using local script

- [x] Generate test detections

- [ ] Investigated the generated alert

- [ ] Tested response actions on the device

- [ ] 



**In Progress**



---



## Phase 5: Advanced Features ⏳




- [ ] Tune Suricata with real traffic

- [ ] Create correlation rules in Splunk

- [ ] Build comprehensive dashboards

- [ ] Test incident response workflows

- [ ] Simulate attack scenarios

- [ ] Document lessons learned



**Planned**



---



## Issues & Solutions Discovered



### Issue 1: pfSense DHCP not assigning IPs

**Solution**: Checked firewall rules, added pass rule for LAN traffic



### Issue 2: No access to Security Onion web interface

**Solution**: Changed Security Onion VM network adapter from NAT to NATNetwork, and used a Kali Linux VM (with the same network adapter and in the same subnet) to enable direct HTTPS access via the NatNetwork subnet without port forwarding complexity.


### Issue 3: pfSense logs not appearing in Splunk

**Solution**: Created UDP data input in Splunk on port 514 with sourcetype syslog and index firewall. Verified pfSense remote logging configuration and restarted services.


### Issue 4: Wazuh agent alerts not appearing in Splunk

**Solution**: Reconfigured Splunk Universal Forwarder on Wazuh Manager to monitor /var/ossec/logs/alerts/alerts.json with correct inputs.conf and outputs.conf. Restarted forwarder and Wazuh alerts now flowing to Splunk.

---



## Key Learnings



1. VirtualBox promiscuous mode is critical for traffic mirroring

2. DHCP pool must not overlap with static IPs

3. Always document network settings (IPs, ports, credentials)

4. Test connectivity after each major configuration change



---



## Next Steps



1. Microsoft Defender for Endpoint

2. Tune Suricata with real traffic

3. Create correlation rules in Splunk



---



**Last Updated**: 11.01.2026

**Overall Completion**: ~90%

