# Complete Guide to Setting Up Servers with zimaOS and casaOS

## Table of Contents
- [Introduction](#introduction)
- [Hardware Requirements](#hardware-requirements)
- [Setting Up zimaOS](#setting-up-zimaos)
  - [zimaOS on Mac Mini](#zimaos-on-mac-mini)
  - [zimaOS on Raspberry Pi](#zimaos-on-raspberry-pi)
  - [zimaOS on Other Mini Computers](#zimaos-on-other-mini-computers)
- [Setting Up casaOS](#setting-up-casaos)
  - [casaOS on Mac Mini](#casaos-on-mac-mini)
  - [casaOS on Raspberry Pi](#casaos-on-raspberry-pi)
  - [casaOS on Other Mini Computers](#casaos-on-other-mini-computers)
- [Common Use Cases](#common-use-cases)
- [Troubleshooting](#troubleshooting)
- [Conclusion](#conclusion)

## Introduction

This guide walks you through setting up home servers using two popular operating systems: zimaOS and casaOS. These lightweight server operating systems are perfect for creating home media servers, personal cloud storage, home automation hubs, and more.

Each system has its own advantages:
- **zimaOS**: Focused on simplicity and ease of use, great for beginners
- **casaOS**: More feature-rich with a modular app store approach

This guide is designed for beginners with minimal technical knowledge. We'll cover installation and basic configuration on different hardware platforms.

![Comparison of zimaOS and casaOS interfaces side by side](images/os-comparison.png)
*Above: Side-by-side comparison of zimaOS (left) and casaOS (right) dashboards*

[Back to Top](#table-of-contents)

## Hardware Requirements

Before we begin, make sure you have the following:

### For Mac Mini Setup:
- A Mac Mini (2010 or newer)
- USB flash drive (8GB or larger)
- Ethernet cable or WiFi connectivity
- External keyboard, mouse, and monitor (for initial setup)

### For Raspberry Pi Setup:
- Raspberry Pi 4 (2GB RAM or more recommended)
- microSD card (16GB or larger, Class 10)
- Raspberry Pi power supply
- Ethernet cable or WiFi connectivity
- Optional: case for the Raspberry Pi

### For Other Mini Computers:
- Any x86-64 mini PC (Intel or AMD)
- 2GB RAM minimum (4GB recommended)
- 16GB storage minimum (SSD preferred)
- Ethernet port or WiFi adapter

### Additional Items:
- External storage drive (recommended for media storage)
- A computer with internet access to download the OS images
- Basic knowledge of how to access your router settings

![Hardware setup for server installation](images/hardware-setup.png)
*Above: Typical hardware setup for a home server installation*

[Back to Top](#table-of-contents)

## Setting Up zimaOS

### zimaOS on Mac Mini

#### Step 1: Download and Prepare Installation Media
1. Visit the zimaOS website (https://zimaos.com) and download the latest version
2. Insert your USB flash drive into your computer
3. Download and install Etcher (https://etcher.io) to create a bootable USB
4. Open Etcher, select the zimaOS image file, select your USB drive, and click "Flash"

![Etcher flashing zimaOS image to USB](images/zimaos-etcher.png)
*Above: Etcher being used to flash the zimaOS image to a USB drive*

#### Step 2: Boot Mac Mini from USB
1. Connect keyboard, mouse, and monitor to your Mac Mini
2. Insert the prepared USB drive
3. Power on the Mac Mini while holding the Option (⌥) key
4. When the boot menu appears, select the USB drive

#### Step 3: Install zimaOS
1. Follow the on-screen installation wizard
2. Select your language and region
3. When prompted for installation location, select the Mac Mini's internal drive
4. **WARNING**: This will erase all data on the Mac Mini
5. Create an administrator account when prompted
6. Complete the installation and allow the system to reboot

![zimaOS installation wizard](images/zimaos-install.png)
*Above: zimaOS installation wizard showing disk selection*

#### Step 4: Initial Configuration
1. When zimaOS boots for the first time, open a web browser on another device
2. Navigate to http://zimaos.local or find the IP address from your router
3. Log in with the administrator credentials you created during installation
4. Complete the initial setup wizard:
   - Set up network configuration
   - Configure time zone settings
   - Enable automatic updates
   - Configure storage settings

![zimaOS first login screen](images/zimaos-login.png)
*Above: zimaOS first login screen after installation*

#### Step 5: Enable Services
1. From the zimaOS dashboard, navigate to "Services"
2. Enable the services you need (file sharing, media server, etc.)
3. Configure each service according to your needs
4. Set up user accounts for family members if needed

![zimaOS services dashboard](images/zimaos-services.png)
*Above: zimaOS services configuration panel*

[Back to Top](#table-of-contents)

### zimaOS on Raspberry Pi

#### Step 1: Download and Flash zimaOS
1. Visit the zimaOS website and download the Raspberry Pi image
2. Insert your microSD card into your computer using an adapter if necessary
3. Download and install Raspberry Pi Imager (https://www.raspberrypi.org/software/)
4. Open Raspberry Pi Imager
5. Click "Choose OS" and select "Use custom" to locate your downloaded zimaOS image
6. Click "Choose Storage" and select your microSD card
7. Click the gear icon to open advanced options
8. Set hostname, enable SSH, configure WiFi (if not using Ethernet), and set locale settings
9. Click "Write" to flash the image to the microSD card

![Raspberry Pi Imager with zimaOS](images/zimaos-pi-imager.png)
*Above: Raspberry Pi Imager showing custom OS selection for zimaOS*

#### Step 2: Set Up Raspberry Pi
1. Insert the microSD card into your Raspberry Pi
2. Connect the Ethernet cable (or rely on the WiFi settings you configured)
3. Connect the power supply to boot the Raspberry Pi

![Raspberry Pi hardware setup](images/pi-setup.png)
*Above: Raspberry Pi hardware setup with microSD and connections*

#### Step 3: Access zimaOS Dashboard
1. Wait about 2 minutes for the Raspberry Pi to boot completely
2. From another device on the same network, open a web browser
3. Navigate to http://zimaos.local or find the IP address from your router
4. If prompted, log in with the default credentials:
   - Username: admin
   - Password: zimaos

#### Step 4: Complete Initial Setup
1. Follow the on-screen setup wizard
2. Change the default password when prompted
3. Configure your timezone and regional settings
4. Set up automatic updates

![zimaOS Pi dashboard](images/zimaos-pi-dashboard.png)
*Above: zimaOS dashboard running on Raspberry Pi*

#### Step 5: Configure Storage
1. Navigate to "Storage" in the dashboard
2. If you have external drives, connect them to the Raspberry Pi's USB ports
3. Format and mount the external drives as needed
4. Configure sharing permissions

![zimaOS storage configuration](images/zimaos-storage.png)
*Above: zimaOS storage configuration panel*

[Back to Top](#table-of-contents)

### zimaOS on Other Mini Computers

#### Step 1: Check Compatibility
1. Ensure your mini computer meets the minimum requirements:
   - x86-64 processor
   - 2GB RAM minimum
   - 16GB storage
   - UEFI boot support

#### Step 2: Download and Create Installation Media
1. Download the zimaOS x86-64 image from the official website
2. Create a bootable USB drive using Etcher or Rufus (https://rufus.ie)

![Rufus creating zimaOS bootable USB](images/zimaos-rufus.png)
*Above: Rufus creating a bootable USB drive with zimaOS*

#### Step 3: Boot and Install
1. Connect keyboard, mouse, and monitor to your mini computer
2. Enter BIOS/UEFI settings (usually by pressing F2, F10, or Delete during boot)
3. Set the USB drive as the first boot device
4. Save changes and reboot
5. Follow the zimaOS installation wizard
6. Select your language and region
7. Choose the internal storage as the installation target
8. Create an administrator account

#### Step 4: First Boot Configuration
1. After installation completes, the system will reboot
2. Access the zimaOS interface via http://zimaos.local or via IP address
3. Complete the initial setup wizard:
   - Configure network settings
   - Set up storage
   - Configure time zone
   - Enable automatic updates

![zimaOS setup wizard](images/zimaos-setup-wizard.png)
*Above: zimaOS initial setup wizard*

#### Step 5: Optimize for Your Hardware
1. Navigate to "System" → "Settings" → "Hardware"
2. Enable hardware acceleration if available for your device
3. Configure power management settings
4. Set up fan control if applicable

![zimaOS hardware settings](images/zimaos-hardware-settings.png)
*Above: zimaOS hardware optimization settings*

[Back to Top](#table-of-contents)

## Setting Up casaOS

### casaOS on Mac Mini

#### Step 1: Prepare Your Mac Mini
1. Back up any important data on your Mac Mini
2. Make sure your Mac Mini is connected to the internet
3. If possible, use a wired Ethernet connection for stability

#### Step 2: Install Required Software
1. On your Mac Mini, open Terminal (Applications → Utilities → Terminal)
2. Update and install required packages by typing:
   ```bash
   /bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"
   brew update
   brew install curl wget git
   ```

![Terminal with Homebrew installation](images/casaos-terminal.png)
*Above: Terminal showing Homebrew installation on Mac Mini*

#### Step 3: Install casaOS
1. In Terminal, run the casaOS installation script:
   ```bash
   curl -fsSL https://get.casaos.io | sudo bash
   ```
2. When prompted, enter your Mac administrator password
3. The installation will take several minutes to complete
4. When finished, you'll see a success message with the URL to access casaOS

![casaOS installation in Terminal](images/casaos-installation.png)
*Above: casaOS installation progress in Terminal*

#### Step 4: Access casaOS Dashboard
1. Open a web browser on any device connected to the same network
2. Navigate to http://mac-mini.local:80 or use the IP address provided during installation
3. If you see a browser security warning, proceed anyway (this is due to the self-signed certificate)

![casaOS login screen](images/casaos-login.png)
*Above: casaOS login screen in web browser*

#### Step 5: Initial Setup
1. Create your casaOS administrator account
2. Set a secure password
3. Complete the setup wizard:
   - Set up system preferences
   - Configure storage locations
   - Set up user access controls

#### Step 6: Install Apps
1. Navigate to the "App Store" in the casaOS dashboard
2. Browse available applications
3. Click "Install" on any apps you want to use
4. Popular starter apps include:
   - Plex Media Server
   - NextCloud (personal cloud storage)
   - Home Assistant (home automation)
   - Transmission (torrent client)

![casaOS App Store](images/casaos-appstore.png)
*Above: casaOS App Store showing available applications*

[Back to Top](#table-of-contents)

### casaOS on Raspberry Pi

#### Step 1: Prepare Raspberry Pi OS
1. Download and install Raspberry Pi OS Lite (64-bit recommended) using Raspberry Pi Imager
2. During setup, enable SSH and configure WiFi if needed
3. Boot your Raspberry Pi with the prepared microSD card
4. Connect to your Raspberry Pi via SSH or connect a monitor and keyboard

![Raspberry Pi OS Imager](images/raspi-imager.png)
*Above: Raspberry Pi Imager with OS selection*

#### Step 2: Update System
1. Update package lists and upgrade existing packages:
   ```bash
   sudo apt update && sudo apt upgrade -y
   ```
2. Install dependencies:
   ```bash
   sudo apt install -y curl wget git
   ```

#### Step 3: Install casaOS
1. Run the casaOS installation script:
   ```bash
   curl -fsSL https://get.casaos.io | sudo bash
   ```
2. The installation will take 5-10 minutes depending on your Raspberry Pi model and internet speed
3. When completed, the terminal will display the access URL and default credentials

![casaOS installation on Pi](images/casaos-pi-install.png)
*Above: casaOS installation process on Raspberry Pi*

#### Step 4: Access casaOS
1. From another device on your network, open a web browser
2. Navigate to http://raspberrypi.local:80 or use the IP address shown in the installation output
3. If the page doesn't load, wait a few more minutes as the services may still be starting

#### Step 5: Configure casaOS
1. Create your administrator account
2. Set your timezone and language preferences
3. Configure storage:
   - Navigate to "Storage" in the dashboard
   - Mount any external drives
   - Set up storage pools if needed

![casaOS dashboard on Pi](images/casaos-pi-dashboard.png)
*Above: casaOS dashboard running on Raspberry Pi*

#### Step 6: Optimize for Raspberry Pi
1. Install lightweight versions of apps when available
2. Monitor system resources in the dashboard
3. Consider setting up overclocking if you're comfortable with it (for advanced users):
   ```bash
   sudo nano /boot/config.txt
   ```
   Add these lines for a modest overclock on Pi 4:
   ```
   over_voltage=2
   arm_freq=1750
   ```

![casaOS system monitor](images/casaos-pi-monitor.png)
*Above: casaOS system monitor showing resource usage*

[Back to Top](#table-of-contents)

### casaOS on Other Mini Computers

#### Step 1: Install Linux
1. Install a compatible Linux distribution (Ubuntu Server 20.04 or newer recommended)
2. Make sure the system is up to date:
   ```bash
   sudo apt update && sudo apt upgrade -y
   ```

![Ubuntu Server installation](images/ubuntu-server.png)
*Above: Ubuntu Server installation process*

#### Step 2: Install casaOS
1. Open a terminal and run:
   ```bash
   curl -fsSL https://get.casaos.io | sudo bash
   ```
2. Follow the on-screen instructions
3. Wait for installation to complete (approximately 5-15 minutes)

#### Step 3: Access and Configure
1. Find your device's IP address:
   ```bash
   ip addr show | grep inet
   ```
2. From another device, open a web browser and navigate to http://[YOUR-IP-ADDRESS]:80
3. Complete the initial setup wizard
4. Create an administrator account

![casaOS initial setup](images/casaos-setup.png)
*Above: casaOS initial setup wizard*

#### Step 4: Hardware-Specific Optimizations
1. For Intel NUC or similar mini PCs:
   - Enable hardware acceleration in casaOS settings
   - Configure wake-on-LAN if desired
2. For ARM-based mini computers:
   - Choose ARM-compatible apps from the app store
   - Monitor CPU temperature and set up cooling as needed

#### Step 5: Set Up Storage
1. Navigate to "Storage" in the casaOS dashboard
2. Format and mount any additional drives
3. Configure sharing permissions
4. Set up backup schedules if needed

![casaOS storage management](images/casaos-storage.png)
*Above: casaOS storage management interface*

[Back to Top](#table-of-contents)

## Common Use Cases

### Media Server Setup
1. Install media server software like Plex, Jellyfin, or Emby from the app store
2. Configure your media folders in the app settings
3. Set up libraries for Movies, TV Shows, Music, etc.
4. Configure remote access if you want to stream outside your home

![Plex Media Server in casaOS](images/plex-setup.png)
*Above: Plex Media Server running through casaOS*

### Personal Cloud Storage
1. Install NextCloud or Seafile from the app store
2. Set up user accounts for family members
3. Configure automatic backup from phones and computers
4. Set storage quotas if needed

![NextCloud in zimaOS](images/nextcloud.png)
*Above: NextCloud personal cloud storage running on zimaOS*

### Home Automation Hub
1. Install Home Assistant or openHAB
2. Connect compatible smart home devices
3. Set up automation routines
4. Configure remote access securely

![Home Assistant dashboard](images/home-assistant.png)
*Above: Home Assistant dashboard for smart home control*

### Network-wide Ad Blocker
1. Install Pi-hole or AdGuard Home
2. Configure your router to use your server as DNS
3. Customize blocklists
4. Monitor statistics to see blocked ads

![Pi-hole dashboard](images/pihole.png)
*Above: Pi-hole dashboard showing blocked ads statistics*

### Game Server
1. Install game server applications like Minecraft Server
2. Configure server settings
3. Set up port forwarding on your router
4. Create backup schedules

![Minecraft server running on casaOS](images/minecraft-server.png)
*Above: Minecraft server configuration in casaOS*

[Back to Top](#table-of-contents)

## Troubleshooting

### Common zimaOS Issues

#### Dashboard Not Loading
1. Check if your server is powered on
2. Verify network connectivity
3. Try accessing via IP address instead of hostname
4. Wait 5 minutes and try again (initial boot can take time)

![zimaOS network diagnostics](images/zimaos-network.png)
*Above: zimaOS network diagnostics tool*

#### Storage Not Mounting
1. Check physical connections
2. Verify drive format (should be ext4, NTFS, or exFAT)
3. Try mounting manually via command line:
   ```bash
   sudo mount /dev/sdX /mnt/yourdrive
   ```
4. Check drive health with SMART tools

#### Performance Issues
1. Check CPU and RAM usage in dashboard
2. Reduce number of running services
3. Consider hardware upgrade if needed
4. Check for overheating

![zimaOS system monitor](images/zimaos-system-monitor.png)
*Above: zimaOS system monitor showing resource usage*

### Common casaOS Issues

#### Installation Fails
1. Verify internet connection
2. Check system requirements
3. Try installation with the alternative method:
   ```bash
   git clone https://github.com/IceWhaleTech/CasaOS.git
   cd CasaOS
   ./build/scripts/setup/setup.sh
   ```

![casaOS manual installation](images/casaos-manual-install.png)
*Above: Manual installation of casaOS from GitHub*

#### Apps Won't Install
1. Check disk space with:
   ```bash
   df -h
   ```
2. Restart Docker service:
   ```bash
   sudo systemctl restart docker
   ```
3. Clear Docker cache:
   ```bash
   sudo docker system prune -a
   ```

![Docker management in casaOS](images/docker-management.png)
*Above: Docker container management in casaOS*

#### Network Issues
1. Check if ports are open with:
   ```bash
   sudo netstat -tulpn | grep LISTEN
   ```
2. Verify firewall settings:
   ```bash
   sudo ufw status
   ```
3. Check Docker network settings

#### Update Problems
1. Manually update casaOS:
   ```bash
   curl -fsSL https://get.casaos.io/update | sudo bash
   ```
2. Check logs for errors:
   ```bash
   sudo journalctl -u casaos
   ```

![casaOS update screen](images/casaos-update.png)
*Above: casaOS system update interface*

[Back to Top](#table-of-contents)

## Conclusion

Congratulations! You now have a fully functioning home server running either zimaOS or casaOS. These versatile platforms can serve a wide range of purposes, from media streaming to home automation.

Remember to:
- Keep your system updated regularly
- Back up important configurations and data
- Secure your server with strong passwords
- Consider setting up automatic backups

As you become more comfortable with your home server, you can explore more advanced features like:
- VPN setup for remote access
- Custom Docker containers
- Advanced networking configurations
- Hardware expansions

If you have questions or need help, check out the zimaOS and casaOS community forums or GitHub repositories.

![Server setup complete](images/server-complete.png)
*Above: A complete home server setup running multiple services*

Happy self-hosting!

[Back to Top](#table-of-contents)
