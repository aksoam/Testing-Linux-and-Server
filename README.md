# Testing-Linux-and-Server
# Overview
This repository contains the implementation for setting up and managing a secure, monitored, and well-maintained development environment as part of a DevOps assignment.

The objective of this project is to assist a Senior DevOps Engineer in:

    Monitoring system performance
    Managing user access securely
    Automating and verifying backups for web servers

The environment is configured for two developers:

    Sarah – Apache Web Server
    Mike – Nginx Web Server

# DevOps System Administration

System Monitoring, User Management, and Backup Configuration Prepared By: Fresher DevOps Engineer Environment: Linux Server Users: Sarah and Mike
# 1. Introduction

This report documents the implementation of system monitoring, user management, access control, and automated backup configuration for a development environment. The objective of this task is to ensure a secure, well-monitored, and properly maintained system that follows operational and security best practices.

The activities were carried out to support two developers, Sarah and Mike, under the guidance of a Senior DevOps Engineer. The implementation includes monitoring tools, secure user account management, password policies, and automated backup mechanisms for Apache and Nginx web servers.
# 2. Task 1: System Monitoring Setup
Configured system monitoring tools to ensure visibility into system health and performance.

Tools & Commands Used:

    .   htop / nmon for CPU, memory, and process monitoring
    .   df -h for disk usage
    .   du -sh for directory-level storage analysis
    .   ps for identifying resource-intensive processes

Logging:

    System metrics are logged in:


        To configure monitoring tools that allow visibility into system performance, resource utilization, and capacity planning.

For RHEL 9

Enable the CodeReady Builder repository (required for some EPEL dependencies):
        
        RHEL 9:-- sudo subscription-manager repos --enable codeready-builder-for-rhel-9-$(arch)-rpms

![alt text](<Screenshot/htop repo.png>)

1. Install htop (Preferred) or nmon

    On RHEL / CentOS / Rocky / AlmaLinux
        sudo dnf install htop -y

    On Ubuntu / Debian
        sudo apt install htop -y


    (Optional – install nmon)
        sudo dnf install nmon -y


# Monitoring Tools Installation
    The following tools were used:
    htop / nmon – for CPU, memory, and process monitoring
    df          – to monitor disk usage
    du          – to identify directory-wise disk consumption  


Installation (for Fedora-based systems):
sudo dnf install epel-release -y
sudo dnf install htop nmon -y

![alt text](<Screenshot/htop install.png>)

![alt text](<Screenshot/htop install1.png>)

![nmon](<Screenshot/nmon install.png>)


2. Monitor System Resources

            htop      - provides real-time CPU, memory, and process usage.
            nmon      - provides performance statistics and system load.
            df -h     - displays filesystem usage.
            du -sh *  - identifies space usage per directory.
            df -hT    - Identifies name read able

![htop provides real-time CPU, memory, and process usage](<Screenshot/htop monitor.png>)

![nmon provides performance statistics and system load](<Screenshot/nmon monitor.png>)

![df -h displays filesystem usage. ](Screenshot/df-h.png)

![du -sh * identifies space usage per directory.](Screenshot/du-sh.png)

![df -hT Identifies name read able ](Screenshot/df-ht.png)

# Task 2: User Management and Access Control
Created secure user accounts with isolated workspaces and enforced password policies.

Users Created:
        sarah
        mike

Workspace Directories:

        Sarah: /home/sarah/workspace
        Mike: /home/mike/workspace

Security Controls:

        Directory permissions set to 700
        Ownership restricted to respective users
        Password expiration enforced every 30 days
        Password warning enabled before expiry
