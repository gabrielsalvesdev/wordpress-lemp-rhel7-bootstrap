# wordpress-lemp-rhel7-bootstrap

Shell script to bootstrap a WordPress environment on Red Hat / CentOS 7 using
NGINX, PHP 7.4, MariaDB, and basic HTTPS/HTTP2 preparation on Google Cloud VM instances.

## Overview

This project automates the initial setup of a WordPress server by installing
the required packages, preparing the web stack, downloading WordPress, and
applying the first configuration steps on a RHEL/CentOS 7 based machine.

It was created as a practical infrastructure automation exercise focused on
self-managed WordPress hosting in cloud environments.

## What it does

- Updates the system packages.
- Installs EPEL and Remi repositories.
- Installs and configures:
  - NGINX
  - PHP 7.4 and required extensions
  - MariaDB
- Prepares basic HTTPS/HTTP2 settings in NGINX.
- Downloads and extracts the latest WordPress release.
- Moves WordPress into the web root.
- Adjusts ownership and permissions.
- Creates the initial `wp-config.php` file.

## Environment

- Google Cloud virtual machine
- Red Hat / CentOS 7
- NGINX
- PHP 7.4
- MariaDB
- WordPress

## Usage

Clone the repository and run the script on a compatible server:

```bash
git clone https://github.com/gabrielsalvesdev/Criar-Site-WordPress-Redhat.git
cd Criar-Site-WordPress-Redhat
chmod +x setup.sh
./setup.sh
```

## Important notes

- This project was designed for Red Hat / CentOS 7 based environments.
- Some package versions and repositories used here are tied to older ecosystems.
- Before using it in production, review:
  - database credentials
  - WordPress security settings
  - SSL certificate configuration
  - firewall and network exposure
  - service hardening

## Limitations

This script performs the initial bootstrap only. It does not fully automate:

- domain configuration
- secure MariaDB hardening
- full Certbot/Let's Encrypt setup
- WordPress post-install wizard
- production-grade hardening

## Why this project exists

The goal of this project is to document and automate the manual process of
bringing up a classic WordPress stack in a cloud VM, turning repetitive server
setup into a reproducible shell-based workflow.

## License

This project is available under the license defined in this repository.
