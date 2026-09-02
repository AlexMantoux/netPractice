*This project has been created as part of the 42 curriculum by amantoux.*

# NetPractice

## Description
 NetPractice is our first project of network designed to introduce us to the basics of computer networking configure IP addresses, connect devices through a router and understand the role of a gateway within a network.

## Instruction

- First you need to download `net_practice.1.9.tgz`

- Go to the place you downloaded it and write/enter the command line `tar -xvf net_practice.1.9.tgz`

- Enter in the directory net_practice and run `sh run.sh`

- Now you have access to the net_practice website. You can choose practice or exam mode. When you resolved any of the levels you can export your configaration level (a json file will be download). Exam mode is a 3 level test (level given are between 6 and 10).

## OSI model

<div style="text-align: center">
    <img src="./imgs/OSI_model.webp" alt="OSI model" width="300"/>   
</div>

## TCP/IP addressing
<div style="text-align: center">
    <img src="./imgs/tcp-ip.svg" alt="tcp/ip network model" width="300"/>   
</div>

## Subnet masks

<!-- TODO TRADUIRE EN ANGLAIS -->
| CIDR | MASQUE DE SOUS-RÉSEAU | MASQUE GÉNÉRIQUE (WILDCARD) | NBR D'ADRESSES IP | NBR D'IP UTILISABLES |
|------|-------------|---------------|-------------------|-------------------|
| /32 |	255.255.255.255 |	0.0.0.0 |	1	| 1
| /31 |	255.255.255.254 |	0.0.0.1 |	2	| 2
| /30 |	255.255.255.252 |	0.0.0.3 |	4	| 2
| /29 |	255.255.255.248 |	0.0.0.7 |	8	| 6
| /28 |	255.255.255.240 |	0.0.0.15 |	16	| 14
| /27 |	255.255.255.224 |	0.0.0.31 |	32	| 30
| /26 |	255.255.255.192 |	0.0.0.63 |	64 	| 62
| /25 |	255.255.255.128 |	0.0.0.127 |	128 | 126
| /24 |	255.255.255.0 |	0.0.0.255 |	256	| 254
| /23 |	255.255.254.0 |	0.0.1.255 |	512	| 510
| /22 |	255.255.252.0 |	0.0.3.255 |	1 024 |	1 022
| /21 |	255.255.248.0 |	0.0.7.255 |	2 048 |	2 046
| /20 |	255.255.240.0 |	0.0.15.255 |	4 096	| 4 094
| /19 |	255.255.224.0 |	0.0.31.255 |	8 192	| 8 190
| /18 |	255.255.192.0 |	0.0.63.255 |	16 384	| 16 382
| /17 |	255.255.128.0 |	0.0.127.255 |	32 768	| 32 766
| /16 |	255.255.0.0 |	0.0.255.255 |	65 536	| 65 534
| /15 |	255.254.0.0 |	0.1.255.255 |	131 072	| 131 070
| /14 |	255.252.0.0 |	0.3.255.255 |	262 144	| 262 142
| /13 |	255.248.0.0 |	0.7.255.255 |	524 288	| 524 286
| /12 |	255.240.0.0 |	0.15.255.255 |	1 048 576 |	1 048 574
| /11 |	255.224.0.0 |	0.31.255.255 |	2 097 152 |	2 097 150
| /10 |	255.192.0.0 |	0.63.255.255 |	4 194 304 |	4 194 302
| /9 |	255.128.0.0 |	0.127.255.255 |	8 388 608 |	8 388 606
| /8 |	255.0.0.0 |	0.255.255.255 |	16 777 216	|16 777 214
| /7 |	254.0.0.0 |	1.255.255.255 |	33 554 432	|33 554 430
| /6 |	252.0.0.0 |	3.255.255.255 |	67 108 864	|67 108 862
| /5 |	248.0.0.0 |	7.255.255.255 |	134 217 728	|134 217 726
| /4 |	240.0.0.0 |	15.255.255.255 |	268 435 456 |	268 435 454
| /3 |	224.0.0.0 |	31.255.255.255 |	536 870 912 |	536 870 910
| /2 |	192.0.0.0 |	63.255.255.255 |	1 073 741 824 |	1 073 741 822
| /1 |	128.0.0.0 |	127.255.255.255 |	2 147 483 648 |	2 147 483 646
| /0 |	0.0.0.0 |	255.255.255.255 |	4 294 967 296 |	4 294 967 294


## Default gateway

## Network devices

Routers and switches are both network devices but they are not aiming the same goal.
<div style="text-align: center">
    <img src="https://cf-assets.www.cloudflare.com/slt3lc6tev37/6ENfwtM3iUH99JpYoEC9FY/04abc1654ceff2645f50713394ebcb73/network-switch.svg" alt="OSI model" width="300" style="background-color: white"/>
</div>

### Routers

A router operates on layer 3 of the OSI model and use IP addressing. It goal is to link differents network together expecially by linking your local network (LAN) to the internet. It handles security (firewall), the NAT* (Network Address Translation), the DHCP (Dynamic Host Configaration Protocol) and permit wifi access.

*NAT is a network mechanism that allows to modify IP addresses on the headers of data packages that transits by a router or a firewall. It mainly serves to convert private IP addresses to public IP addresses.

*DHCP is a network protocol that attribute IP addresses to the connected devices and other network configurations like subnet masks, DNS (Domain name system) Server, etc... 

### Switches

The switch operates at layer 2 of the OSI model and uses MAC addresses. It connects multiple devices within the same local network (such as PCs, printers, or servers). It directs data only to the intended device, which optimizes performance and reduces collisions compared to older hubs.

The MAC (Media Access Control) address is a unique 48-bit physical identifier, coded in hexadecimal, etched into the chip of each network card (NIC) to identify a device on a local network.

### Internet Protocol

IP addresse is a 32-bit identifier...

- **IpV4**:

- **IpV6**:




## Resources
