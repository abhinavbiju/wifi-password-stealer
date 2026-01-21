# Wi-Fi Password Gatherer (Educational Use Only)

This project demonstrates how Windows stores and exposes Wi-Fi profile information using the built-in netsh command. The Python script retrieves the currently connected Wi-Fi network profile and displays the stored configuration, including the password if it is already saved on the machine.

This repository is created strictly for educational, research, and cybersecurity learning purposes.
It does not, and cannot, break into networks or access credentials that the device does not already have stored.

# Legal & Ethical Disclaimer

## This script:

Works only for Wi-Fi networks the local Windows device already has a saved profile for

Does not bypass or exploit any security measures

Must only be used on systems you own or have explicit permission to analyze

Misuse of this script may violate local, state, or federal law.
You are solely responsible for using this project ethically and legally.

# Purpose

This project exists to help learners understand:

How Windows stores Wi-Fi profiles

How netsh commands reveal wireless configuration data

How Python can automate system information gathering

How credential exposure occurs on endpoints, and how to defend against it

This knowledge supports cybersecurity training and responsible security research.

# Requirements

Windows 10 or Windows 11

Python 3.x

Standard user or administrator privileges (depending on system configuration)

# Installation
git clone https://github.com/<your-username>/<your-repo>
cd <your-repo>

# Usage

## Run the script:

python wifi.py


## The script will:

Detect the currently connected Wi-Fi SSID

Check if the Windows system has a stored profile for that SSID

Retrieve the complete profile using:

netsh wlan show profiles "<SSID>" key=clear


Save the results to wificreds.txt

Automatically open the file in Notepad

# Output Example

A typical output file may include:

SSID name              : HomeNetwork
Authentication         : WPA2-Personal
Security key           : Present
Key Content            : examplepassword123

# Project Structure
wifi.py           # Main script
wificreds.txt     # Generated Windows Wi-Fi profile report (created when run)
README.md         # Documentation

# Security Awareness

This project illustrates important security concepts:

Any user with local access to a machine can view saved Wi-Fi passwords

Sensitive Wi-Fi networks should avoid storing credentials on shared devices

Strong endpoint security prevents unauthorized local access

Admins should audit wireless profiles regularly

# Educational Use Only

This project is intended for:

Cybersecurity students

IT and security professionals

Researchers studying Windows Wi-Fi management

Home users auditing their own devices

Do not use this tool for unauthorized access of any kind.
