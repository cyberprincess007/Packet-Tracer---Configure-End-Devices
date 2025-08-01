# Packet-Tracer---Configure-End-Devices

## Objective
Build a simple Packet Tracer network and perform basic configuration of end devices, including setting static IP addresses, verifying connectivity, and completing basic switch configuration.
In this lab, I built a small network in Cisco Packet Tracer with two PCs, a server, and a switch. I gave each device a static IP address, connected them with the correct cables, and made sure they could communicate by using ping and a web browser. I also practiced basic switch setup, including renaming it and shutting down an interface to see how it affects connectivity.

## Tools Used
- Cisco Packet Tracer (latest version)

## Summary of Tasks
1. **Build the Topology**
   - Deployed a **2960 switch**, two **PC-PT** computers, and one **Server-PT**.
   - Connected devices using **Copper Straight-Through** cables:
     - `PC0` FastEthernet0 → `Switch0` FastEthernet0/1
     - `PC1` FastEthernet0 → `Switch0` FastEthernet0/2
     - `Server0` FastEthernet0 → `Switch0` GigabitEthernet0/1

2. **Configure Static IP Addresses**
   - **Server0**
     - IP Address: `192.168.1.1`
     - Subnet Mask: `255.255.255.0`
   - **PC0**
     - IP Address: `192.168.1.2`
     - Subnet Mask: `255.255.255.0`
   - **PC1**
     - IP Address: `192.168.1.3`
     - Subnet Mask: `255.255.255.0`

3. **Verify Connectivity**
   - **Ping Tests**
     - From `PC0` to `Server0` (`192.168.1.1`) — successful replies.
     - From `PC1` to `PC0` (`192.168.1.2`) — successful replies.
   - **Web Browser Test**
     - Accessed `192.168.1.1` in a browser from both PCs — successfully displayed the Cisco Packet Tracer webpage.

4. **Basic Switch Configuration**
   - Renamed the switch from `Switch0` to `Central` using the **Config** tab.
   - Viewed equivalent IOS commands in the **Equivalent IOS Commands** box:
     ```
     Switch> enable
     Switch# configure terminal
     Switch(config)# hostname Central
     ```
   - Configured and navigated interfaces in the Config and CLI tabs.
   - Shut down the `FastEthernet0/1` interface via CLI:
     ```
     Central(config-if)# shutdown
     ```
   - Observed the link lights for `PC0` turning red due to administrative shutdown.

## Outcome
- Successfully built a small network in Packet Tracer.
- Assigned static IPs to a server and PCs for direct communication.
- Verified end-to-end connectivity using ping and a web browser.
- Performed basic switch configuration, including hostname changes and interface shutdown.

  

## Skills Demonstrated
- Network topology creation in Packet Tracer
- Static IP address assignment
- Basic connectivity troubleshooting using ping and web browser tests
- Introductory Cisco IOS configuration via Config and CLI tabs
- Interface shutdown and administrative control
- Understanding of link light status indicators
