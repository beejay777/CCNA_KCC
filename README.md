# Day 1
#### Main points.
-  Basic (Revision of previously learned topics and basic theory about internet, cabling, ip and other stuffs and _contains little Laboratory exercise_)
-  Routing
-  Switching 
-  Security

**Topics to revise**
- Routing:
- IP, subnet, subnet mask:
- Switch:
- Firewall:
- DNS:
- Encryption:


# Day 2
What is required to be a network? Or components of a network.
1. Device
  - End Devices (source or destinations of messages for communication _eg. Computers, Mobiles_)
  - Intermediate Devices (Relayers of information _eg. Repeaters, Routers, Switch, firewall_) **Network administration is concerned on managing, and configuring network devices which is _ROUTER_**
2. Media
  - Guided
    - Twisted
    - Fiber
    - Co-axial
    - Ethernet
  - Unguided
    - Radiowave
    - Microwave
    - wifi
3. Services (softwares)

Characterstics:
- Bandwidth (how much data can be transferred in a given second)
- Cost
- Security
- Speed (delay)
- Quality of Service (prioritization of data) (_important concept_)
- Reliability (how often the network goes down)
- Availability (how long the network goes down for)
- Backup / Fault Tolerance / Redundancy


#### Network Topologies
                                       
Pysical Topologies (how it looks) |  Logical Topoligies (how data flows)
--- | ---
Bus |  Bus 
Star | Bus
E-Star | Bus
Ring | Ring


# Day 3
#### Basic Router Commands
```processing
router> 
router> enable                  // Privilage Execute Mode
router# configure terminal
router(config)#                 // Global conf
router(config)# interface fa0
router(config-if)#              // Global sub-conf mode
router(config-if)# ip address 192.168.1.1 255.255.255.0
router(config-if)# no shutdown  // Switches on the port fa0

// Add hostname
router(config-if)# hostname myName
myName(config-if)#              // Changes the hostname (the name of router)

// Add password
myName(config-if)# enable password anypassword
or
myName(config-if)# enable secret anypassword

// To remove any configurations put 'no' infront of the command without putting the variables
myName(config-if)# no enable password    // Removes the password 
```

After setting up the router the router config must be saved before turning off the router or else we should configure everytime we use the router. To save the config the **NVRAM** (Non Volatile Ram) is used. The configs can also be saved in **Flash Storage** (present in router itself) and in the **TFTP server**.

![CISCO configuration Copy command](https://www.certificationkits.com/assets/images/stories/cisco-ccna/ch-3-2-ios/cisco-ccna-ios-02.jpg "CISCO configuration Copy command")


The syntax of copy command is. 
`copy <source> <destination>`
