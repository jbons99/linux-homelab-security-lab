# Linux Homelab Security Lab

Self-hosted Ubuntu infrastructure lab focused on Linux administration, secure deployment, reverse proxies, monitoring, automation, and operational security.

## Overview

This project documents my self-hosted infrastructure environment used to deploy and monitor personal applications, automation services, and development tools.

The lab is designed to demonstrate practical experience with Linux server administration, secure remote access, firewall configuration, reverse proxying, monitoring, and deployment workflows.

## Technologies Used

- Ubuntu Server
- nginx
- Docker
- PM2
- Cloudflare
- UFW Firewall
- SSH key-based authentication
- Git / GitHub
- Uptime Kuma
- Node.js / Python services

## Key Features

- Self-hosted Ubuntu server environment
- nginx reverse proxy configuration
- HTTPS / SSL deployment
- Cloudflare DNS and security protection
- UFW firewall rules to reduce exposed attack surface
- SSH key-only authentication with password login disabled
- PM2 process management for long-running services
- Docker-based service hosting
- Uptime monitoring and alerting
- Git-based deployment workflow

## Security Hardening Implemented

- Disabled SSH password authentication
- Enabled SSH key-based login
- Disabled root login
- Configured UFW firewall rules
- Restricted internal application ports to LAN access
- Blocked sensitive dotfiles such as `.env` and `.git`
- Monitored nginx access logs for scanner and bot activity
- Used Cloudflare bot protection and managed challenges

## Architecture

```text
Internet
   ↓
Cloudflare
   ↓
nginx Reverse Proxy
   ↓
Hosted Applications / PM2 Services / Docker Containers
   ↓
Monitoring & Logs
```

## Infrastructure Monitoring

The environment uses Uptime Kuma to continuously monitor service availability, latency, and infrastructure health across deployed applications and services.

![Uptime Kuma Dashboard](Screenshot%20KumaUptime.png)


## Process Management

PM2 is used to manage long-running backend services, automate restarts on failure, and monitor application uptime across deployed applications.

![PM2 Status](Screenshot%20Pm2-status.png)
