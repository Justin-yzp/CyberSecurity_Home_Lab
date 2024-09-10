# Elastic SIEM Home Lab

## Overview

This project demonstrates the deployment of a home lab for Elastic Stack Security Information and Event Management (SIEM) using Elastic Cloud and a Kali Linux virtual machine (VM). It covers the complete lifecycle of SIEM deployment, including agent installation, event generation, log analysis, and dashboard creation. The goal is to provide a hands-on experience in cybersecurity monitoring and incident response.

## Prerequisites

Before you begin, ensure you have:

- VirtualBox or VMware for virtualization.
- Basic understanding of Linux OS and network security concepts.

## Tasks

### Task 1: Set up an Elastic Account

1. **Create a Free Elastic Cloud Account:**
   - Sign up for a free trial at [Elastic Cloud Registration](https://cloud.elastic.co/registration).
   - Log in to the Elastic Cloud console at [Elastic Cloud Console](https://cloud.elastic.co).
   - Click on "Start your free trial."
   - Select "Create Deployment" and choose "Elasticsearch."
   - Choose a region and deployment size, then click "Create Deployment."
   - Wait for the deployment to initialize and then click "Continue."

### Task 2: Setting up the Linux VM

1. **Download and Install Kali Linux:**
   - Obtain the Kali Linux VM image from [Kali Linux Downloads](https://www.kali.org/get-kali/#kali-virtual-machines).
   - Create a new VM in VirtualBox or VMware using the downloaded image.
   - Boot the VM and follow the installation prompts.
   - Log in using the default credentials `kali` for both username and password.

### Task 3: Setting up the Agent to Collect Logs

1. **Install the Elastic Agent:**
   - Access the Elastic SIEM instance.
   - Navigate to the Integrations page by selecting "Integrations" from the Kibana main menu.
   - Search for "Elastic Defend" and install the integration.
   - Copy the provided installation command for Linux and execute it in the Kali terminal.
   - Validate the installation with `sudo systemctl status elastic-agent.service`.

### Task 4: Generating Security Events on the Kali VM

1. **Install and Use Nmap for Network Reconnaissance:**
   - If you're using a non-Kali Linux VM, install Nmap with `sudo apt-get install nmap`.
   - Conduct various Nmap scans to simulate network reconnaissance:
     - Basic scan: `sudo nmap <vm-ip>`
     - SYN scan: `nmap -sS <ip address>`
   - These scans will generate network traffic and security events, providing a basis for analysis.

### Task 5: Querying for Security Events in the Elastic SIEM

1. **Query and Analyze Logs:**
   - In Elastic SIEM, navigate to "Logs" under "Observability."
   - Utilize the search bar to craft queries such as `event.action: "nmap_scan"` or `process.args: "sudo"`.
   - Analyze the results to identify patterns and anomalies.

### Task 6: Create a Dashboard to Visualize Events

1. **Design and Customize Dashboard:**
   - Go to the Elastic web portal and select "Dashboards" under "Analytics."
   - Click "Create dashboard" and add a new visualization.
   - Choose "Area" or "Line" chart type and configure it to display event counts over time.
   - Save your visualizations and assemble them into a comprehensive dashboard to monitor and visualize security events.

### Task 7: Create an Alert

1. **Define and Configure Security Alerts:**
   - Navigate to "Alerts" under "Security."
   - Click "Manage rules" and then "Create new rule."
   - Select "Custom query" and set conditions to detect anomalies such as Nmap scans.
   - Configure alert actions (e.g., email notifications, Slack alerts, webhook integration) and save the rule to enable proactive threat detection.

## Conclusion

This project sets up a functional home lab environment for practicing SIEM operations and cybersecurity monitoring using Elastic Stack. You will gain practical experience with deploying SIEM solutions, generating security events, and analyzing logs for incident detection and response.

## Next Steps

- Expand event generation to include various types of security incidents (e.g., port scans, brute force attacks).
- Fine-tune alert rules and thresholds to improve detection accuracy.
- Explore additional integrations and data sources to enhance the SIEM capabilities.

## Resources

- [Elastic Cloud](https://cloud.elastic.co/)
- [Kali Linux](https://www.kali.org/)
- [Nmap](https://nmap.org/)
- [Elastic SIEM Documentation](https://www.elastic.co/guide/en/security/current/index.html)

---

Feel free to adjust the instructions or add specific details based on your setup or preferences.
