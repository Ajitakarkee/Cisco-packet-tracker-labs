### Key Concepts
- **Topology:** One Class A (15.0.0.0/8), one Class B (182.98.0.0/16), one Class C (201.191.20.0/24) network.
- Router interfaces are **administratively down** by default (`shutdown` command).

### Step-by-Step Configuration

1. **Change Hostname**  
   `hostname R1`

2. **View Interfaces**  
   `show ip interface brief`  
   (Use `do show ip interface brief` from config mode)

3. **Configure Interface (Example: Gi0/0)**  
   `interface gigabitethernet 0/0`  
   `ip address 15.255.255.254 255.0.0.0`  
   `description ## to SW1 ##`  
   `no shutdown`

4. **Repeat for Other Interfaces**  
   Apply similar commands for remaining interfaces using appropriate Class A/B/C addresses and masks.

5. **Verify Configuration**  
   `show ip interface brief`  
   (Confirm IPs are manual and status is **UP/UP**)

6. **Save Configuration**  
   `write`  
   or  
   `copy running-config startup-config`

7. **Configure PCs in Packet Tracer**  
   - Manually assign IPs (subnet mask auto-fills based on class).  
   - Test connectivity with `ping` between PCs.

![Lab 7 Topology](Lab_7.png)
