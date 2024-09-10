# Elastic SIEM Home Lab

## Introduction

In today's rapidly evolving cybersecurity landscape, having a robust and dynamic Security Information and Event Management (SIEM) system is crucial for effective threat detection, incident response, and overall security posture management. This project demonstrates a home lab setup for Elastic SIEM, leveraging the Elastic Stack to collect, analyze, and visualize security events. This hands-on experience is invaluable for Security Operations Centers (SOCs) and cybersecurity professionals, as it provides practical skills in configuring SIEM systems, analyzing logs, and creating actionable alerts.

## Overview

This guide outlines the steps to set up a home lab using Elastic SIEM and Kali Linux. By following this tutorial, you'll gain practical experience in:

- Setting up a free Elastic Cloud instance.
- Configuring Kali Linux and the Elastic Agent.
- Generating security events and analyzing them in Elastic SIEM.
- Creating dashboards and alerts to monitor and respond to security incidents.

## Prerequisites

- VirtualBox or VMware
- Basic knowledge of Linux and virtualization software
- Understanding of SIEM concepts and log management

## Tasks

### Task 1: Set Up an Elastic Account

1. Sign up for a free trial at [Elastic Cloud](https://cloud.elastic.co/registration).
2. Log in and create a new deployment for Elasticsearch.
3. Select your preferred region and deployment size.
4. Wait for the deployment to be ready.

### Task 2: Setting Up the Linux VM

1. Download Kali Linux from [Kali's official website](https://www.kali.org/get-kali/#kali-virtual-machines).
2. Create a new VM in VirtualBox or VMware using the Kali VM file.
3. Complete the Kali installation and log in with default credentials.

### Task 3: Setting Up the Agent to Collect Logs

1. Navigate to the Integrations page in your Elastic SIEM instance.
2. Install Elastic Defend on your Kali VM.
3. Run the installation command on Kali and verify installation with `sudo systemctl status elastic-agent.service`.

### Task 4: Generating Security Events

1. Install Nmap (if not pre-installed) using `sudo apt-get install nmap`.
2. Perform network scans with `sudo nmap <vm-ip>` and other Nmap commands to generate security events.

### Task 5: Querying for Security Events

1. Access the “Logs” tab in Elastic SIEM.
2. Use search queries to filter logs, such as `event.action:"nmap_scan"`.

### Task 6: Creating a Dashboard

1. Go to the “Dashboards” section in Elastic SIEM.
2. Create a new dashboard and add visualizations to track event counts over time.

### Task 7: Creating an Alert

1. Navigate to the “Alerts” section.
2. Create a new rule with a custom query to detect Nmap scans.
3. Set alert actions, such as email notifications or Slack messages.

## Skills

- **Elastic SIEM**: Configuration, log analysis, and dashboard creation.
- **Kali Linux**: Installation and configuration for generating security events.
- **Elastic Agent**: Installation and management for log forwarding.
- **Nmap**: Network scanning and vulnerability assessment.
- **Querying**: Log filtering and event analysis in Elastic SIEM.
- **Dashboarding**: Visualization of security events and metrics.
- **Alerting**: Creation and management of security alerts for incident detection.

## Conclusion

By completing this lab, I have acquired hands-on experience with Elastic SIEM, which is a critical component of modern cybersecurity infrastructure. This setup enhances my understanding of SIEM functionalities and prepares me for real-world security monitoring and incident response tasks.

Feel free to reach out with any questions or feedback regarding this guide.

## Sources

- [A Simple Elastic SIEM Lab](https://medium.com/@aali23/a-simple-elastic-siem-lab-6765159ee2b2)
- [Elastic SIEM Tutorial Video](https://www.youtube.com/watch?v=2XLzMb9oZBI)

---
