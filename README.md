# Invisinet - Bypass College Firewall with Ease

## Table of Contents

- [Project Overview](#project-overview)
- [Motivation](#motivation)
- [Features](#features)
- [Setup and Installation](#setup-and-installation)
- [Usage](#usage)
- [Configuration](#configuration)

## Project Overview

Tired of your college firewall blocking access to your favorite sites like Spotify and Netflix? Look no further! This project is your ultimate solution to bypass those annoying restrictions. By leveraging AWS's powerful EC2 instances with elastic IPs and the robust OpenVPN, you and your friends can enjoy a seamless, unrestricted internet experience.

## Motivation
<img width="707" alt="Screenshot 2024-07-02 at 8 41 48 AM" src="https://github.com/a6ar55/MY-secure-VPN/assets/117556787/61f9e728-2e87-4e83-9c6e-d91c42116c78">

Living on a campus with a restrictive firewall can be frustrating, especially when you can't access essential resources or entertainment platforms. After discovering that even popular VPN services were blocked, I took matters into my own hands. Using AWS services, I crafted a custom VPN solution that breaks free from these digital chains, ensuring that students can surf the web freely and enjoy a better online experience.


## Features

- Secure VPN connection using OpenVPN
- Auto-scaling EC2 instance to handle multiple connections
- Easy setup and configuration

## Setup and Installation

### Prerequisites

- AWS account
- Basic knowledge of AWS services (EC2, Elastic IP, Auto Scaling)
- OpenVPN Connect client installed on your device

### Steps




1. **Create an EC2 Instance:**
   - Launch an EC2 instance using the OpenVPN AMI from the AWS Marketplace.
   - Attach an Elastic IP to the instance.

2. **Configure Auto Scaling:**
   - Add the EC2 instance to an Auto Scaling group to handle multiple connections.

3. **Initialize OpenVPN:**
   - SSH into the server as `openvpnas`.
   - Initialize OpenVPN configurations and enable traffic routing through the VPN server.

4. **Access OpenVPN Admin Portal:**
   - Open your browser and go to `https://<public-ip-address>:993/admin`.
   - Configure the VPN settings and set the DNS servers:
     - Primary DNS: `1.1.1.1` (Cloudflare)
     - Secondary DNS: `8.8.8.8` (Google)

5. **Install OpenVPN Connect Client:**
   - Install the OpenVPN Connect client on your device.
   - Connect to the VPN server and route your traffic through it.

```Connected! Welcome to the Open Internet!```


![WhatsApp Image 2024-07-01 at 22 15 49](https://github.com/a6ar55/MY-secure-VPN/assets/117556787/3a85ddac-d7c2-4b6e-b1db-b43b6fdf6a7d)
       <img width="328" alt="Screenshot 2024-07-01 at 10 17 36 PM" src="https://github.com/a6ar55/MY-secure-VPN/assets/117556787/37cf7af6-6342-4293-b50f-3312a13c2bb4">


## Usage

1. Launch the OpenVPN Connect client on your device.
2. Enter the VPN server details and connect.
3. Enjoy unrestricted access to the internet.

## Configuration

### DNS Settings

- Primary DNS: `1.1.1.1` (Cloudflare)
- Secondary DNS: `8.8.8.8` (Google)

### OpenVPN Settings

Access the admin portal at `https://<public-ip-address>:993/admin` to configure additional settings as per your requirements.


