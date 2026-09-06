*This project has been created as part of the 42 curriculum by amantoux.*

# NetPractice

## Description
NetPractice is our first networking project, designed to introduce us to the fundamentals of computer networking. It focuses on configuring IP addresses, subnetting, connecting devices through a router, and understanding the role of a gateway within a network.

## Instructions

- First, download `net_practice.1.9.tgz`.

- Navigate to the directory where you downloaded the file and run the following command: 
    ```sh
    tar -xvf net_practice.1.9.tgz && cd net_practice
    ```

- Launch the training interface using the provided shell script:
    ```sh
    sh run.sh
    ```

- You now have access to the `net_practice` interface. You can choose between **Practice** and **Exam** mode.
- **Exporting Configurations:** Once you solve a level, you can export your configuration file (a `.json` file will be downloaded)
- **Exam Mode:** Consists of a 3-level test (levels are randomly assigned between 6 and 10).
- **Submission Requirements:** To submit your work, you must save your final exported `.json` configuration file into your repository as required by the evaluation guidelines.

## OSI Layers

<div style="text-align: center">
    <img src="./imgs/OSI_model.webp" alt="OSI model" width="300"/>   
</div>

## TCP/IP Addressing
<div style="text-align: center">
    <img src="./imgs/tcp-ip.svg" alt="TCP/IP network model" width="300"/>   
</div>

## Subnet Masks

| CIDR | SUBNET MASK | WILDCARD MASK | TOTAL IP ADDRESSES | USABLE IP ADDRESSES |
|------|-------------|---------------|-------------------|---------------------|
| /32 | 255.255.255.255 | 0.0.0.0 | 1 | 1 |
| /31 | 255.255.255.254 | 0.0.0.1 | 2 | 2 |
| /30 | 255.255.255.252 | 0.0.0.3 | 4 | 2 |
| /29 | 255.255.255.248 | 0.0.0.7 | 8 | 6 |
| /28 | 255.255.255.240 | 0.0.0.15 | 16 | 14 |
| /27 | 255.255.255.224 | 0.0.0.31 | 32 | 30 |
| /26 | 255.255.255.192 | 0.0.0.63 | 64 | 62 |
| /25 | 255.255.255.128 | 0.0.0.127 | 128 | 126 |
| /24 | 255.255.255.0 | 0.0.0.255 | 256 | 254 |
| /23 | 255.255.254.0 | 0.0.1.255 | 512 | 510 |
| /22 | 255.255.252.0 | 0.0.3.255 | 1,024 | 1,022 |
| /21 | 255.255.248.0 | 0.0.7.255 | 2,048 | 2,046 |
| /20 | 255.255.240.0 | 0.0.15.255 | 4,096 | 4,094 |
| /19 | 255.255.224.0 | 0.0.31.255 | 8,192 | 8,190 |
| /18 | 255.255.192.0 | 0.0.63.255 | 16,384 | 16,382 |
| /17 | 255.255.128.0 | 0.0.127.255 | 32,768 | 32,766 |
| /16 | 255.255.0.0 | 0.0.255.255 | 65,536 | 65,534 |
| /15 | 255.254.0.0 | 0.1.255.255 | 131,072 | 131,070 |
| /14 | 255.252.0.0 | 0.3.255.255 | 262,144 | 262,142 |
| /13 | 255.248.0.0 | 0.7.255.255 | 524,288 | 524,286 |
| /12 | 255.240.0.0 | 0.15.255.255 | 1,048,576 | 1,048,574 |
| /11 | 255.224.0.0 | 0.31.255.255 | 2,097,152 | 2,097,150 |
| /10 | 255.192.0.0 | 0.63.255.255 | 4,194,304 | 4,194,302 |
| /9 | 255.128.0.0 | 0.127.255.255 | 8,388,608 | 8,388,606 |
| /8 | 255.0.0.0 | 0.255.255.255 | 16,777,216 | 16,777,214 |
| /7 | 254.0.0.0 | 1.255.255.255 | 33,554,432 | 33,554,430 |
| /6 | 252.0.0.0 | 3.255.255.255 | 67,108,864 | 67,108,862 |
| /5 | 248.0.0.0 | 7.255.255.255 | 134,217,728 | 134,217,726 |
| /4 | 240.0.0.0 | 15.255.255.255 | 268,435,456 | 268,435,454 |
| /3 | 224.0.0.0 | 31.255.255.255 | 536,870,912 | 536,870,910 |
| /2 | 192.0.0.0 | 63.255.255.255 | 1,073,741,824 | 1,073,741,822 |
| /1 | 128.0.0.0 | 127.255.255.255 | 2,147,483,648 | 2,147,483,646 |
| /0 | 0.0.0.0 | 255.255.255.255 | 4,294,967,296 | 4,294,967,294 |

## Default Gateway

A **default gateway** is a network node (usually a router) that serves as an access point or forwarding node to other networks when no other route matches the destination IP address. 

When a host wants to send data to an IP address outside its local subnet, it sends the packets to the default gateway's IP address. The default gateway must reside within the same local subnet as the device relying on it.

## Network Devices

Routers and switches are both network devices, but they fulfill different roles.

<div style="text-align: center">
    <img src="https://cf-assets.www.cloudflare.com/slt3lc6tev37/6ENfwtM3iUH99JpYoEC9FY/04abc1654ceff2645f50713394ebcb73/network-switch.svg" alt="Network Switch" width="300" style="background-color: white"/>
</div>

- ### Routers

    A router operates at **Layer 3** of the OSI model and uses IP addressing. Its goal is to link different networks together, specifically connecting your Local Area Network (LAN) to an external network like the internet. Routers handle security (firewalls), **NAT** (Network Address Translation), **DHCP** (Dynamic Host Configuration Protocol), and Wi-Fi access.

    *\*NAT is a networking mechanism that modifies IP addresses in the headers of data packets in transit through a router or firewall. It is primarily used to map private IP addresses to public IP addresses.*

    *\*DHCP is a network protocol used to automatically assign IP addresses and other configuration parameters (such as subnet masks, default gateways, and DNS servers) to connected devices.*

- ### Switches

    A switch operates at **Layer 2** of the OSI model and uses MAC addresses. It connects multiple devices within the same local network (such as PCs, printers, or servers). A switch forwards data only to the specific intended device, optimizing performance and reducing packet collisions compared to legacy hubs.

    *\*The MAC (Media Access Control) address is a unique 48-bit physical identifier coded in hexadecimal and burned into the Network Interface Card (NIC) to identify a specific device on a local network.*

### Internet Protocol

- **IPv4**: An IPv4 address is a 32-bit numerical label represented as 4 decimal numbers separated by dots. The total number of unique addresses available under IPv4 is roughly 4.3 billion.

- **IPv6**: IPv6 uses 128-bit addresses represented as 8 groups of hexadecimal digits separated by colons. The number of unique IPv6 addresses is roughly $3.4 \times 10^{38}$, which is virtually inexhaustible.

IPv6 was introduced because IPv4 addresses were reaching exhaustion due to the explosion of connected devices. IPv6 also simplifies network configuration and reduces reliance on NAT.

However, IPv4 remains the dominant protocol today for several reasons:
- Legacy infrastructure built around IPv4.
- High migration and upgrade costs.
- Compatibility issues: IPv4 and IPv6 devices cannot communicate directly without transition mechanisms.
- NAT prolongs IPv4's lifespan by allowing multiple devices on a local private network to share a single public IPv4 address.
- Transition to IPv6 is taking place gradually.

Since IPv4 and IPv6 packets are not natively compatible, several coexistence techniques are used:
- **Dual Stack:** Devices run IPv4 and IPv6 protocol stacks simultaneously.
- **Tunneling:** Encapsulating IPv6 packets inside IPv4 packets to traverse IPv4-only networks.
- **Translation:** Devices convert packets between IPv4 and IPv6 using protocols such as NAT64.

## Resources

### Core Networking Concepts
- **OSI Model & TCP/IP Stack:**
  - [Cloudflare: What is the OSI Model?](https://www.cloudflare.com/learning/ddos/glossary/open-systems-interconnection-model-osi/)
  - [GeeksforGeeks: TCP/IP Model](https://www.geeksforgeeks.org/tcp-ip-model/)
- **Subnetting & Addressing:**
  - [IPAddressGuide Subnet Cheat Sheet](https://www.ipaddressguide.com/subnet)
  - [Subnet IPv4 Practice Exercises](https://www.subnetting.net/)

### AI Usage
- Formatting and translating documentation into English markdown.