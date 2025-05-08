# Homelab
My personal homelab running Proxmox, WireGuard, Vaultwarden and Caddy, with custom tmperature monitoring and fan control. All repurposed, older hardware I have refurbished and refinished.

I have built this homelab for fun, security, and educational purposes. You'll find that all of my gear is cheap, older things I've either purchased or gotten for free. Security is a prime concern, and I do my best to keep everything as locked down as I can. I strongly prefer open source, well documented materials with large communities, as I am entirely self taught and learning as I go. 

## Core Functionality 
- Virtualization and containerization with Proxmox
- Self hosted VPN via WireGuard for secure remote access to network
- Self hosted password manager with Vaultwarden
- Reverse proxy and SSL with Caddy
- Envionrmental monitoring and automated active cooling with TDisplay S3

## Hardware
Optiplex 7040 - 8core CPU, 16GB ram, 500GB HDD. Also has a CD drive, which I didnt have on my network before (bonus!) This hosts Proxmox and all my VMs and LXCs.
Intel SS4200-E NAS - 8tb storage in a RAID 5 for 6 total TB usable. This bad boy is one of the first commercial NAS systems to come out way back in 2007, and I found a guy selling 3 of them that he bought, upgraded to the max ram and cpu the motherboard would support (a whopping 2 core CPU and 2 gigs DDR2 ram), and stuck them all back in the boxes to sit in his basement until 2024. I was able to refurb one (check my other repo) and sell the remaining two for cost. Free NAS for me!
LilyGo TDisplay S3 - I used a DS18B20 sensor attached to a breadboard and wrote a simple Arduino sketch to monitor and display temp as well as serve a webpage with the data. Using WireGuard, I can VPN to my home network and check the status of the cabinet. I also attached a Noctuna NF12 5v fan to a usb port on the optiplex, and a MOSFET wired to the TDisplay. This way, the display can control the exhaust fan I installed in the rear of the cabinet. I can also control the fan manually via a slider on the Tdisplay's webpage. 
