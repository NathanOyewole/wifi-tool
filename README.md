 # WiFi Tool

A simple script to scan and display available WiFi networks (both saved and unsaved), including details such as SSID, signal strength, and (optionally) saved passwords.

## Features
- **List saved WiFi networks**: Retrieve saved WiFi networks from your system.
- **Scan for available networks**: Detect available WiFi networks within range.
- **Extract saved passwords**: Optionally extract the passwords for saved WiFi networks (only works for networks that have been saved previously).

## Installation

To use this tool, you need a system running Linux (with root privileges). The script is intended for use on Debian-based systems like Ubuntu.

## Prerequiites

Before using the script, ensure that the following packages are installed:
- `iw` (for wireless network interface management)
- `nmcli` (NetworkManager CLI tool, if you're using NetworkManager)
  
To install the required dependencies, run:

```bash
sudo apt update
sudo apt install iw network-manager

Cloning the Repository
First, clone this repository to your local machine:

git clone https://github.com/NathanOyewole/wifi-tool.git
cd wifi-tool

Making the Script Executable
Make the script executable:

chmod +x wifi-scanner.sh

Running the Script
Run the script with root privileges to scan for WiFi networks:

sudo ./wifi-scanner.sh

If you want to save the results (including passwords, if extracted) into a file, you can specify a file output as well:

sudo ./wifi-scanner.sh > output.txt

How the Script Works
The script first checks for available WiFi networks.

It lists both saved WiFi networks and unsaved networks.

For saved networks, it attempts to extract the saved passwords (if available).

The information is displayed on the screen and optionally saved to a file.

Usage
To list all available networks (both saved and unsaved), simply run the script. It will display the following information for each network:

SSID: The name of the WiFi network.

Signal Strength: The strength of the signal (in dBm).

Password: The password for saved networks, if available.

Example output:

Network Name: HomeWiFi
Signal Strength: -40 dBm
Password: myhomepassword

Network Name: PublicWiFi
Signal Strength: -75 dBm
Password: N/A (unsaved network)

```
