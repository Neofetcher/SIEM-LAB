# SIEM-LAB
Security information and event management Lab Project 

## Objective

The objective of this SIEM (Security Information and Event Management) lab project is to design and implement a comprehensive security monitoring solution that effectively detects, investigates, and responds to security incidents within an enterprise environment. Through hands-on exercises and simulations, participants will gain practical experience in configuring SIEM tools, creating custom detection rules, analyzing security events, and orchestrating incident response workflows. By the end of the project, participants will have developed a proficient understanding of SIEM technologies and best practices, equipping them with the skills necessary to enhance the security posture of organizations through proactive threat detection and mitigation.

### Skills Learned 

 - Elastic Stack SIEM Configuration and Management: Successfully set up and configured Elastic Stack SIEM in a home lab environment. Demonstrated proficiency in deploying a Kali Linux VM, configuring Elastic Agents for log collection, and forwarding data to the SIEM for effective security event monitoring.
 - Security Event Simulation and Analysis: Acquired hands-on experience in generating and analyzing security events using Nmap on Kali Linux. Proficient in querying Elastic SIEM to identify and investigate security incidents, enhancing skills in network security monitoring and threat detection.
 - Visualization and Alerting in SIEM: Developed a custom dashboard in Elastic SIEM to visualize security events, demonstrating skills in data interpretation and pattern recognition. Successfully created and tested alert rules for detecting specific security events, showing competency in proactive incident response and alert management.

### Tools Used

 - VirtualBox
 - Kali Linux
 - Elastic Cloud Service
   
### Steps

 - Sign up for a free trial to use Elastic Cloud at https://cloud.elastic.co/registration
 - Start your free trial.
 - Create Deployment

![siem create deployment ](https://github.com/Neofetcher/SIEM-LAB/assets/166114015/4f4129b9-fa38-4cbe-a560-d71fd83c478f)


 
 - Download VirtualBox or VMware 
 - Download the Kali Linux https://www.kali.org/get-kali/#kali-platforms
 - Setup your Kali Linux VM
 - Update your Kali Linux

### Setup Elastic 

 - Click on the hamburger menu on the top left, then select +Add Integration at the bottom
 - In the integration Tab, Search for Elastic Defender and select +Add Elastic Defender
 - Installing Elastic agent on your host
 - Copy the commands provided
 - Open terminal on your Kali VM paste the commands and press enter wait for the installtion to complete.

 
 ![kali 1](https://github.com/Neofetcher/SIEM-LAB/assets/166114015/95722f52-6757-4c93-b511-a29efd5ddb17)

 
 - To verify if the agent installed correctly run the following command sudo systemctl status elastic-agent.service

### Generate Security Events on the host

 - Use nmap to generate security events

![image](https://github.com/Neofetcher/SIEM-LAB/assets/166114015/0ca3b380-27eb-436f-9e9c-fe3a544cf9f8)

 - Different nmap commands [ sudo nmap <ip>, sudo nmap -A -p- <ip>, sudo nmap -Ss <ip>, sudo nmap -sT <ip>.

![image](https://github.com/Neofetcher/SIEM-LAB/assets/166114015/22cba9e9-cbbb-45ab-8a23-d3f1739b7cef)

### Querying for Security Events in the Elastic SIEM

 - Go to the hamburger menu select logs under the observability section
 - Check the endpoint.events.process, Cick on the menu and select view details

![image](https://github.com/Neofetcher/SIEM-LAB/assets/166114015/0fcb43b5-8c5c-45bc-95c7-c17d613d8652)

 - Check for the nmap commands that were ran on the host

![image](https://github.com/Neofetcher/SIEM-LAB/assets/166114015/b872b98f-42e8-4f57-b99f-28d745e8e2a7)

### Creating a Dashboard 

 - Go to the hamburger menu, Select Dashboard under the analytics section
 - Select +Create new dashboard, +Create Visualization

![image](https://github.com/Neofetcher/SIEM-LAB/assets/166114015/f16577b8-bb93-4b5b-a2ca-eca9fa8e9edc)

 - Add layers using Horizontal axis and Vertical axis.

![image](https://github.com/Neofetcher/SIEM-LAB/assets/166114015/b6aa452d-d84f-43d0-ad33-292a92a2cd73)

 - After adding different layers the dashboard should look something like this

![image](https://github.com/Neofetcher/SIEM-LAB/assets/166114015/4a10b4cd-a127-4586-814c-432ef49a6f41)

 - Click on the “Save” button to save the visualization and then complete the rest of the settings.

### Creating an Alert 

 - To create an alert go to the hamburger menu and select Alerts under the Security section
 - Click on manage rule, +Create new rules
 - Under "custom query", define the rules using KQL syntax
 - Use the following command for nmap scan alerts

![image](https://github.com/Neofetcher/SIEM-LAB/assets/166114015/8db03afe-923c-4bc8-9636-05655d1313b5)

 - Click on Continue
 - Under the about rule section, Add name and description for the rule
 - Complete the other settings
 - Finally, click the “Create and enable rule” button to create the alert.

## Disclamer
This project is intended for educational purposes only. Use responsibly and only with proper authorization on systems you own or have explicit permission to monitor.

   
