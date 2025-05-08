# My Homelab

My personal homelab running Proxmox, WireGuard, Vaultwarden, and Caddy, with custom temperature monitoring and fan control. All built on repurposed, older hardware I have refurbished and refinished.

## About

I've built this homelab for fun, security, and educational purposes. You'll find that all of my gear consists of affordable, older components I've either purchased or acquired for free. Security is a prime concern, and I've focused on keeping everything as locked down as possible. I strongly prefer open-source, well-documented materials with large communities, as I am entirely self-taught and learning as I go.

## Core Functionality

* **Virtualization and Containerization:** Utilizing Proxmox VE to run virtual machines and LXC containers.
* **Secure Remote Access:** Self hosted VPN for secure access to my home network from anywhere.
* **Self-Hosted Password Management:** Running Vaultwarden for a private and secure password manager.
* **Reverse Proxy and SSL:** Using Caddy to manage secure connections and route traffic to internal services.
* **Environmental Monitoring and Automated Cooling:** Custom solution with a LilyGo T-Display S3 for temperature monitoring and automated fan control.

## Hardware

* **Optiplex 7040:**
    * 8-core CPU, 16GB RAM, 500GB HDD.
    * Includes a CD Drive, which I was lacking. Bonus!
    * This machine serves as the host for Proxmox and all my VMs and LXCs.

* **Intel SS4200-E NAS:**
    * 8TB raw storage configured in RAID 5, providing 6TB usable storage.
    * This bad boy is one of the first commercial NAS systems to come out way back in 2007, and I found a guy selling 3 of them that he bought, upgraded to the max ram and cpu the motherboard would support (a whopping 2 core CPU and 2 gigs DDR2 ram), and stuck them all 
      back in the boxes to sit in his basement until 2024. I was able to refurb one and sell the remaining two for cost. Free NAS for me!
    * (https://github.com/iThinkiKhan/intel-ss4200e-homelab-NAS)

* **LilyGo T-Display S3 (with Custom Temp Sensor & Fan Control):**
    * I used a DS18B20 sensor attached to a breadboard and wrote a simple Arduino sketch to monitor and display temp as well as serve a webpage with the data. Using WireGuard, I can VPN to my home network and check the status of the cabinet. I also attached a Noctuna NF12 5v fan to a usb port on the optiplex, and a MOSFET wired to the TDisplay. This way, the display can control the exhaust fan I installed in the rear of the cabinet. I can also control the fan manually via a slider on the Tdisplay's webpage. 
