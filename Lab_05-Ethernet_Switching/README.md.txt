## Lab Walkthrough

This lab demonstrates Ethernet LAN switching using Cisco Packet Tracer with two switches and four PCs.

When PC1 pings PC3, the process begins with an ARP broadcast to discover the MAC address of the destination. PC3 responds with an ARP reply, followed by ICMP echo request and reply communication between the devices.

Simulation mode is used to observe the packet flow step by step.

Pings are also performed between PC2 and PC4, allowing switches to learn all MAC addresses dynamically.

The `show mac address-table` command is used to verify MAC learning on each switch, showing which MAC address is mapped to which port.

Finally, the `clear mac address-table dynamic` command is used to reset the MAC address table and confirm that entries are removed.

---


![Ethernet Switching Lab](lab_5.png)
