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

. htop / nmon for CPU, memory, and process monitoring
. df -h for disk usage
. du -sh for directory-level storage analysis
. ps for identifying resource-intensive processes

Logging:

    System metrics are logged in:


        To configure monitoring tools that allow visibility into system performance, resource utilization, and capacity planning.

