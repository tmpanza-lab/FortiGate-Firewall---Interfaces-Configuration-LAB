# FortiGate Firewall - Interfaces Configuration LAB

## Objective


The objective of this FortiGate Firewall - Interfaces Configuration LAB is to provide hands-on experience and understanding of key networking and security concepts related to interface configuration on a FortiGate firewall.

### Skills Learned

- Networking and Security Configuration Skills (VLAN Management, Inter-VLAN Routing, VLAN tagging, Redundant Interfaces and Link Aggregation (LACP)
- Navigating and configuring the FortiGate user interface and CLI
- Foundational skill for more advanced configurations, such as High Availability (HA), SD-WAN, and dynamic routing protocols.


### Tools Used

- FortiGate VM: A virtual appliance used in virtualized environments, such as VMware or Hyper-V
- FortiOS Web-based (GUI)
- FortiOS Command Line Interface (CLI)
- Network Simulators: GNS3 for simulated network devices (e.g., routers, PCs, or switches) to test managed switches supporting VLAN tagging (802.1Q) and LACP for link aggregation.
- Network Testing Tools: Ping, Traceroute, Packet Capturing Tools (Wireshark)

*Ref 1: Network Diagram*
![image](https://github.com/user-attachments/assets/d007e3f4-9ead-40a4-b046-cae6e71a0bb7)

 

## Steps


VLAN Configuration Part-1 #
![image](https://github.com/user-attachments/assets/f1478627-f5bc-4f5c-a8bb-1caba353c9ba)
![image](https://github.com/user-attachments/assets/4d14d462-53e4-43be-9f58-86fc2dfb845e)
![image](https://github.com/user-attachments/assets/7f7343b5-6bb7-4f38-b879-121486ad8f8e)
 

 


 


# Switch VLAN Configuration #
![image](https://github.com/user-attachments/assets/5b2749f4-30fa-414f-b163-9a757b4af4bc)
 
# Assign VLAN to Interfaces
![image](https://github.com/user-attachments/assets/f382bb2c-6191-469a-9396-9b2933ad56aa)
 

# Enable Routing
![image](https://github.com/user-attachments/assets/fce4f985-315c-40e0-adf0-5495648b11c0)
 

# FortiGate configuration #
![image](https://github.com/user-attachments/assets/1e2379d0-cbd5-4bd0-b9bd-90606f4b1964)
 

# Interfaces Configuration
![image](https://github.com/user-attachments/assets/6e75bcbf-4629-46d7-9b9d-81bba46b0c90)
![image](https://github.com/user-attachments/assets/09e32ae3-3511-4c12-af0e-4f3c8aebc9fb)
![image](https://github.com/user-attachments/assets/03ac34f3-b4d5-4eea-90fa-ca2248d1d8bb)
 
 
 
# Add Static Routes to other VLANs
![image](https://github.com/user-attachments/assets/3d70ccdb-88b9-4e8f-a705-1a7e031408bd)
 
Next
![image](https://github.com/user-attachments/assets/05d04881-5bc4-4d6a-8f96-8d9b127f0193)
![image](https://github.com/user-attachments/assets/e69672bf-7d56-4c8d-b1af-b63e97afbbcf)
![image](https://github.com/user-attachments/assets/c01077ba-0ec8-4dd1-90b8-bf161777e107)
![image](https://github.com/user-attachments/assets/31021abb-20e7-4c1d-aa3e-cbdc47841f31)
 
 
 
 Test Inter-VLAN routing
![image](https://github.com/user-attachments/assets/b32c7a34-9f43-448b-b655-5e52abde5dcb)
 


VLAN Configuration Part-2 #
![image](https://github.com/user-attachments/assets/56dcdcdf-d758-4fbf-bba0-bf4c41fde5c8)
 
# FortiGate VLAN Configuration
![image](https://github.com/user-attachments/assets/4bda109a-ac8e-4f07-89cf-86b956537b83)
 
# Switch Configuration
![image](https://github.com/user-attachments/assets/ac25de50-0158-48bc-be4e-3b2a59a24fd0)
 
# Assign interfaces to VLANs
![image](https://github.com/user-attachments/assets/71ef83d1-6fad-424e-815f-ec8f902c0027)
![image](https://github.com/user-attachments/assets/28a2049b-8dd3-458f-92fb-45b22d46e128)
![image](https://github.com/user-attachments/assets/29b16cfc-3ba9-48b2-8349-9e2f6c21f1d2)
 
 
 
This is static IP and our gateway is 10.1, which is our FortiGate IP.
So, let's try to access our FortiGate here from our web browser via the LAN 10.
Let's put the IP of our FortiGate this is the IP of our FortiGate.
Perfect, I can access to it.
![image](https://github.com/user-attachments/assets/743b3614-a182-45c2-8310-dec8aed5a52e)
 
Now to check our configuration, we need to go to network.
Interfaces > and we need to expand Port 1.
So go to this icon here. Click it and here we can find VLANs belonging to the to the Port 1.
This is what we are previously configured via the CLI.
![image](https://github.com/user-attachments/assets/519935c5-1a79-457c-a571-bb20798e79e5)
![image](https://github.com/user-attachments/assets/39dc16e4-81ce-4793-9199-c0f8ac57f703)

 
 

### Enable IVR (Inter VLAN Routing) On Fortigate ###

# We have Two Options To Enable IVR:

1)	Create A firewall Policy That Allow Traffic between VLANs
![image](https://github.com/user-attachments/assets/ddd2af94-f01e-46c5-b9cd-277259a5d5a4)


## Don't Forget To Activate Multiple interfaces Policy From Feature visibility ##
![image](https://github.com/user-attachments/assets/4cf18ab3-2623-48f5-aa20-28925590ccef)
 

Then I need to go to policy and object.
Firewall policy I will create new.
It would give it a name which is IVR-FGT and FortiGate in the oncoming interface.
I will choose the three VLANs and outgoing interface I need to choose also the three VLANS.
In source I will choose ALL and destination I will choose ALL.
In services I will choose ALL and this is our policy.
![image](https://github.com/user-attachments/assets/af19c39a-10cf-4afe-8413-d0c110f44bfb)
![image](https://github.com/user-attachments/assets/185972ce-dab6-44e3-b0e6-e8c2d46c9d77)
 
 

Set static IP for PC1 in VLAN 20
![image](https://github.com/user-attachments/assets/3fca3469-a2d1-4a1c-aae0-d67caf7fc588)
 
Set static IP for PC2 in VLAN 30
![image](https://github.com/user-attachments/assets/f5f029a1-f945-4d0f-88d8-6d9207724394)
 
From P1 – VLAN 20, I will try to ping my FortiGate IP address.
![image](https://github.com/user-attachments/assets/8085f4c2-a976-4d71-9d90-39467a0fef37)
 
From P2 – VLAN 30 I will try to ping my FortiGate IP address.
![image](https://github.com/user-attachments/assets/27ffde0e-b978-4880-9482-b79b71a82c40)
 

From FortiGate Firewall I will try to ping WEBADMIN – VLAN 10, PC1 – VLAN 20 and PC2 – VLAN 30 ‘s IP addresses.
![image](https://github.com/user-attachments/assets/78eaf597-44ac-4c64-91bd-ed7435f7fd88)
 




3)	Create VLANs Zone
So now I will show you the second method first, I will remove this policy.
![image](https://github.com/user-attachments/assets/4d54269c-b174-428f-93c1-cce9da272d38)
 

Test again to show you that ping will not pass then I will do the second method and we will test it also so I will delete this policy.

I will go back and I will try to ping again and it can't ping.
![image](https://github.com/user-attachments/assets/00b0e89a-7888-4ba3-a731-631dd7da62ae)
 

The second method is, is we need to go to network interfaces.

We need to create new zone.
![image](https://github.com/user-attachments/assets/904bb53b-d26e-46ed-bb4e-d81d1612e20d)
 

And this is the trick here we need to disable this, uh, policy here.
This policy means that the intrusion traffic, the traffic between those VLANS will be blocked if we disable it.

The traffic between those VLAN here will be allowed and they will try to ping again.
![image](https://github.com/user-attachments/assets/8abd2445-bb04-461a-b6a7-24d968997b90)
![image](https://github.com/user-attachments/assets/12be49e4-2272-4821-83e5-e67d6e20765c)

 
 


Now I can ping.
![image](https://github.com/user-attachments/assets/fd85c735-c0bc-42e4-b34b-446d776a9c47)
 

My recommendation to you is to do it via the policy so you can have a visibility on the traffic because when we do it via the zone, we can't see the traffic passing through our FortiGate.

But if we, do it from the policy, we have the visibility in FortiGate.

If we go to log and report and forward traffic.

Here we can see that this PC here is being in this PC.
![image](https://github.com/user-attachments/assets/75d0ed4c-150b-4eac-a723-ecbf4f1b4c08)
 

## Redundant Interface ##
![image](https://github.com/user-attachments/assets/c6a2de9e-d097-470c-8255-be69aa5dbc1a)

 
The Redundant interface is also like the Aggregate interface in the regrouping of ports, the different is:
- NO LACP protocol activated 
- In redundant interface we have the bandwidth of only one link
- the redundant interface send traffic in one interface only and the other interface stay on standby waiting for the active interface to fail.
# Configuration
![image](https://github.com/user-attachments/assets/afb9f4e4-5b45-4c3e-bc9e-c2dea3bc8c0b)
![image](https://github.com/user-attachments/assets/a1584ad3-d049-46da-837c-8844efad75c7)
 
 
# Interfaces Configuration
![image](https://github.com/user-attachments/assets/ee8cd4dd-d308-406e-a6f4-d81574d00af8)
![image](https://github.com/user-attachments/assets/be9c24d5-f949-44af-9357-636e5a1f6cfe)
 
 
So, to test it, I will go to my PC here and I will launch a PING toward my firewall.
![image](https://github.com/user-attachments/assets/bba461f0-b7e7-4a6a-b90b-e519fe0a7343)
![image](https://github.com/user-attachments/assets/5fba353b-4be0-4873-9ba4-e14af696c9f4)
 
 

Okay.

This is the IP address of my firewall.

Perfect.

Now I will try to delete one of these links here, so I will delete port 10.
![image](https://github.com/user-attachments/assets/68cff5b8-f7e5-40f4-af61-ad642af1d0a7)
 

And they will see if the pink's still working.

Perfect.

I can see it pinging.
![image](https://github.com/user-attachments/assets/15d9444a-7833-45ca-bb45-05c5505fe4f4)
 

Now I will put it back and I will delete the other interface.
![image](https://github.com/user-attachments/assets/d3e46528-58c0-49b1-91b3-a2d7434a88d9)
 

Port nine.

I will delete it.

We will check the ping now.

One packet dropped but ping still passing.
![image](https://github.com/user-attachments/assets/cbe58cd0-496c-4fa9-bd23-c8763f302a72)
 

So this is how to create redundant interface.



## LACP = LINK AGGREGATION CONTROL PROTOCOL (802.3ad)

- LACP it's a protocol that group from 2 to 4 fortigate physical interfaces to one logical interface 

# Please note that the interfaces should not be used in a policy or have an IP@

# Benefits of LACP 

- Redundant: in case if we lose one interface or link other interfaces take the trafic with metigatin of the down time 

- Bandwidth: if we have 50mb per link and we use two link in our LACP group we benifit from 100mb logical interface.

# LACP MODES

- Active: initiative the communication to the passive end.

- Passive: while the passive wait for the other end to start the communication.


# FortiGate Aggregate Interface (LACP) #
![image](https://github.com/user-attachments/assets/2535daef-7132-4818-9ac2-556927c05898)
![image](https://github.com/user-attachments/assets/4565e1c9-9e96-4c4e-8064-4b9dba4a6448)
![image](https://github.com/user-attachments/assets/c55e75c3-75b9-4ef0-a587-eaf60b47ae4d)
![image](https://github.com/user-attachments/assets/249bd7da-417e-4bf1-8326-bf5a355d7690)
 
 
 
 

# Switch LACP Configuration (Etherchannel)
![image](https://github.com/user-attachments/assets/fb981b98-4bd6-4caf-8946-f5756c95a3aa)
![image](https://github.com/user-attachments/assets/cbdc0983-090e-44b3-bdfa-53b3be65fa3b)
![image](https://github.com/user-attachments/assets/b20258dd-c828-4c91-9bcc-92002de538bb)

 
 
 

Create A firewall Policy That Allow Traffic between VLANS
![image](https://github.com/user-attachments/assets/703b84f8-2c93-427f-99b4-26ffa38ea0ef)
![image](https://github.com/user-attachments/assets/b21b4a36-b40f-4702-a6dd-89980e478d98)
 

 


I will try to ping the FortiGate.

Perfect.

I can PING it now.
![image](https://github.com/user-attachments/assets/48dabf2b-964a-4a3d-b9a0-b7a97770fc56)
 

I will try to remove one of the interfaces one pocket is dropped, but pink still working.
![image](https://github.com/user-attachments/assets/bc16bb8e-5314-4a16-9668-1d9bcd2d3d58)
 

One packet dropped and PING still passing traffic
 ![image](https://github.com/user-attachments/assets/f186231c-1b2c-4939-b752-84e79171824b)
![image](https://github.com/user-attachments/assets/5f88f304-c19c-44e8-8c1c-c2319ccdedc0)
![image](https://github.com/user-attachments/assets/4197fa41-57b9-46f0-9fd7-83334deff34a)
![image](https://github.com/user-attachments/assets/870c5b4e-0c69-4514-8831-0076400c4a99)
![image](https://github.com/user-attachments/assets/2e5f7bf7-d6a4-4827-8a0e-0d584fc1340d)

 

So, this is how to create and configure an LACP interface.

