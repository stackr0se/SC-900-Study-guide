# Azure DDoS Protection

Distrubuted Denial of Service (DDoS)
- Attacks that makes resource unresponsive

Azure DDoS Protection
- Analyzes network traffic at the network and transport layers; and discards anything that looks like a DDoS attack.
- Always-on traffic monitoring.
- Adaptive real-time tuning.
- DDoS Protection telemetry, monitoring, and alerting.

# Azure Firwall
Azure Firwall protects your Azure Network (VNet) resources from attackers.
- Create or allow deny networ filtering rules.
- Use Microsoft Threat Intelligence feed to alert or filter traffic from/to known malicous IP addresses and domains.
- All outbound virtual network traffic IP addresses are translated to the Azure Firewall public IP to make it harder for attackers to target internal network devices.
- Integration with Microsoft Copilot
<img width="576" height="415" alt="image" src="https://github.com/user-attachments/assets/d60b0664-f0ad-41eb-a6b8-35b140cb9cf7" />

# Web Application Firewall
Centralized protection of your web applications from common exploits and vulnerabilities.
- Protection against threats and intrusions.
- Protects web applications DDoS attacks.
- Patching a known vulnerability in one place.
- Inegration with Microsoft Security Copilot
<img width="595" height="373" alt="image" src="https://github.com/user-attachments/assets/c4c55515-d805-45ae-a77f-aa4fd4382206" />

# Network segmentation and Azure VNet
Reasons for network segmentation
- The ability to group related assets.
- Isolation of resources.
- Governance policies set by the orgaization.

Azure Virtual Network (Vnet)
- Network level containment of resources with no traffic allowed across Vnets or inbound to Vnet.
- Communication needs to be explicitly provisioned.
- Control how resources in a VNet communicate with other resources, the internet, and on-premises networks.
<img width="443" height="293" alt="image" src="https://github.com/user-attachments/assets/0e3a0faa-1373-4621-825a-c774587ebd97" />

# Azure network security groups (NSGs)
Filter network traffic between Azure resources in an Azure virtual network.
- An NSG is made up of inbound and outbound security rules that allow or deny traffic.
- An NSG can contain many rules, the rules are processed based on their assigned priotity.
- When an NSG is created, it includes default inbound and outbound rules.
- You can't remove the default rules, but you can override them by creating new rules with higher priorities.
<img width="276" height="302" alt="image" src="https://github.com/user-attachments/assets/2dd762c2-b984-4693-a962-c8b1a0d65b26" />

# Secure remote access to VMs: Azure Bastion
Azure Bastion - secure connectivity to your VMs from the Azure portal
- RDP and SSH directly in the Azure portal.
- Traverse the corporate firewalls securely.
- No public IP required on Azure VM.
- No need to manage NSGs.
- Protection against port scanning.
- Protect against zero-days exploits
<img width="618" height="392" alt="image" src="https://github.com/user-attachments/assets/70d9cb5f-785f-4bb7-8bf3-31710eac098d" />

# Azure Key Vault 
A cloud service for securely storing and accessing secrets such as API keys, passwords, certificates, or cryptographic keys.
Key vault benefits
- Centralize application secrets.
- Securely store secrets and keys.
- Monitor access and use.
- Simplified administration of application secrets.

Two ters:
- Standard: SW-based encryption.
- Premium-HW security module (HSM) protected keys.
<img width="581" height="380" alt="image" src="https://github.com/user-attachments/assets/cfdd36d6-11d9-4dac-9a88-d444f8fde163" />

