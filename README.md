# Cisco_Practice_Lab

# 1. No. OF DEVICES

a. 2 Routers
b. 3 Switches
c. 6 Pc
d. RJ45 Cable

# 2. SETUP

a. Created VLAN 
    - VLAN 10 is for HR
    - VLAN 20 is for IT
    - VLAN 30 is for Finance
    Points :- VLAN 10, 20 can communicate with each other but cannot from VLAN 30 because I isolated it.

b. FLOW
   - HR <---> IT
   - IT <-/-> FINANCE
   - HR <-/-> FINANCE

c. Setup Details :-
   - Enabled the TRUNKING by DTP( Dynamic Trunking Protocol ) so that VLAN can transfer through link between switchs.
   - I configure IVR( Inter Vlan Routing [Router on-stick] ) in Router0 to seamless communication between different vlan.
   - I configure HSRP for Redundant link so that if one link goes down other can be used for backup.
   - I configure DHCP so that I don't have to assign IP in every PC Manually.
   - I configure ACL( Access Control List) to stop communication between HR,IT with FINANCE.

d. Verification
   - HR to IT ping succeed.
   - IT to HR ping succeed.
   - IT/HR to FINANCE ping failed.
   - DHCP assigned the expected IP to every PC.

# 3. Troubleshooting

   - Issue: DHCP failed assigning IP.
   - Checks: VLAN, Trunking, Interface Status, DHCP configuration and Default-Gateway.
   - Root Cause: Not Enable the Trunking to the port of switch which is connected to the DHCP configure Router.
   - Resolution: Record the actual fix.

# 4. Backup

 - Save the final .pkt lab file to my local storage of my pc and deploy one of the copy to GITHUB.

# 5. Learning

  - Record what I learn by mistake and did new thing in networking.
