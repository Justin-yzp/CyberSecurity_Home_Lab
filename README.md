# Elastic SIEM Home Lab

## Overview

This project demonstrates how to set up a home lab for Elastic Stack Security Information and Event Management (SIEM) using Elastic Cloud and a Kali Linux virtual machine (VM). It covers the process of setting up an Elastic account, installing and configuring a Kali Linux VM, deploying the Elastic Agent, generating and analyzing security events, and creating dashboards and alerts in Elastic SIEM.

## Prerequisites

Before you start, ensure you have:

- VirtualBox or VMware installed.
- Basic knowledge of Linux and virtualization software.

## Tasks

### Task 1: Set up an Elastic Account

1. **Create a Free Elastic Cloud Account:**
   - Sign up for a free trial at [Elastic Cloud Registration](https://cloud.elastic.co/registration).
   - Log in to the Elastic Cloud console at [Elastic Cloud Console](https://cloud.elastic.co).
   - Click on "Start your free trial."
   - Click on "Create Deployment" and select "Elasticsearch."
   - Choose a region and deployment size, then click "Create Deployment."
   - Wait for the configuration to complete, then click "continue."

### Task 2: Setting up the Linux VM

1. **Download and Install Kali Linux:**
   - Download Kali Linux VM from [Kali Linux Downloads](https://www.kali.org/get-kali/#kali-virtual-machines).
   - Create a new VM in VirtualBox or VMware using the downloaded file.
   - Start the VM and follow the installation prompts.
   - Log in using the credentials `kali` for both username and password.

### Task 3: Setting up the Agent to Collect Logs

1. **Install the Elastic Agent:**
   - Log in to the Elastic SIEM instance.
   - Navigate to the Integrations page by clicking on the Kibana main menu, then select "Integrations."
   - Search for "Elastic Defend" and install it.
   - Copy the provided installation command for Linux and paste it into the Kali terminal.
   - Verify installation with `sudo systemctl status elastic-agent.service`.

### Task 4: Generating Security Events on the Kali VM

1. **Install and Use Nmap:**
   - If using a non-Kali Linux VM, install Nmap with `sudo apt-get install nmap`.
   - Run various Nmap scans: `sudo nmap <vm-ip>`, `nmap -sS <ip address>`, etc., to generate security events.

### Task 5: Querying for Security Events in the Elastic SIEM

1. **Query Logs:**
   - In Elastic SIEM, navigate to "Logs" under "Observability."
   - Use the search bar to enter queries such as `event.action: "nmap_scan"` or `process.args: "sudo"`.
   - Review search results and details.

### Task 6: Create a Dashboard to Visualize Events

1. **Create and Customize Dashboard:**
   - Navigate to the Elastic web portal and click on "Dashboards" under "Analytics."
   - Click "Create dashboard" and add a new visualization.
   - Select "Area" or "Line" chart type and configure it to show event counts over time.
   - Save the visualization and dashboard.

### Task 7: Create an Alert

1. **Define and Configure Alert:**
   - Go to "Alerts" under "Security."
   - Click "Manage rules" and then "Create new rule."
   - Choose "Custom query" and set conditions to detect Nmap scan events.
   - Configure alert actions (e.g., email, Slack, webhook) and save the rule.

## Conclusion

This project sets up a complete home lab environment for practicing security monitoring and incident response using Elastic SIEM. You will gain practical experience with configuring SIEM tools, generating and analyzing security events, and creating alerts and dashboards.

## Next Steps

- Generate various types of security events and analyze them in Elastic SIEM.
- Test and fine-tune the alert configurations.
- Explore additional integrations and data sources to enhance your SIEM setup.

## Resources

- [Elastic Cloud](https://cloud.elastic.co/)
- [Kali Linux](https://www.kali.org/)
- [Nmap](https://nmap.org/)
- [Elastic SIEM Documentation](https://www.elastic.co/guide/en/security/current/index.html)

---

Feel free to adjust the instructions or add any specific details based on your setup or preferences.
