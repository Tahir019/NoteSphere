
# Accenture Network Security & Cloud Computing Notes

## Table of Contents
1. [Router Commands and Access Control](#router-commands-and-access-control)
   - [Router Privilege Levels](#router-privilege-levels)
   - [Key Commands for Access Control](#key-commands-for-access-control)
2. [Access Control Lists (ACLs)](#access-control-lists-acls)
   - [Understanding ACLs](#understanding-acls)
   - [Types of ACLs](#types-of-acls)
   - [Examples of ACL Configuration](#examples-of-acl-configuration)
3. [Network Security Devices](#network-security-devices)
   - [Types of Network Security Devices](#types-of-network-security-devices)
   - [Active vs. Passive Devices](#active-vs-passive-devices)
4. [Cloud Service Providers](#cloud-service-providers)
   - [Key Differences Between Cloud and Data Centers](#key-differences-between-cloud-and-data-centers)
   - [Major Cloud Providers](#major-cloud-providers)
   - [Choosing a Cloud Provider](#choosing-a-cloud-provider)
5. [Common Cyber Attacks](#common-cyber-attacks)
   - [Types of Cyber Attacks](#types-of-cyber-attacks)
   - [Mitigation Strategies](#mitigation-strategies)
6. [Encryption Algorithms](#encryption-algorithms)
   - [Symmetric vs. Asymmetric Encryption](#symmetric-vs-asymmetric-encryption)
   - [Overview of DES and AES](#overview-of-des-and-aes)
7. [Hybrid Storage in Cloud Services](#hybrid-storage-in-cloud-services)
   - [Benefits of Hybrid Storage](#benefits-of-hybrid-storage)
   - [Cloud Providers and Hybrid Storage](#cloud-providers-and-hybrid-storage)

---

## Router Commands and Access Control

### Router Privilege Levels
- **Privilege Levels**: Routers use different privilege levels to restrict access to certain commands. For example:
  - Level 0: No access
  - Level 1: User access (basic commands)
  - Level 15: Full access (all commands)

### Key Commands for Access Control
- **`show running-configuration`**: Displays the current configuration of the router.
- **`show ip interface`**: Displays the status of all interfaces along with any access lists applied to them. This command is essential to confirm if an access list is enabled on a specific interface.

## Access Control Lists (ACLs)

### Understanding ACLs
- **Definition**: An Access Control List (ACL) is a set of rules used to control network traffic and reduce network attacks. ACLs filter traffic based on IP addresses, protocols, and ports.

### Types of ACLs
1. **Standard ACLs**: Filter traffic based only on the source IP address. 
   - Example: Denying traffic from a specific subnet.
2. **Extended ACLs**: Filter traffic based on source and destination IP addresses, protocols, and ports.
   - Example: Allowing HTTP traffic to a web server from any host.

### Examples of ACL Configuration
- **Denying a Subnet**:
  ```bash
  access-list 10 deny 172.16.48.0 0.0.15.255
  ```
  This command denies all traffic from the subnet `172.16.48.0/20`.

- **Permitting SMTP Traffic**:
  ```bash
  access-list 110 permit tcp any host 1.1.1.1 eq smtp
  ```
  This command allows SMTP traffic only to the host `1.1.1.1`.

## Network Security Devices

### Types of Network Security Devices
1. **Firewalls**: Monitors and controls incoming and outgoing network traffic based on predetermined security rules.
2. **Antivirus Scanners**: Actively scans network traffic for malware and other threats.
3. **Intrusion Detection Systems (IDS)**: Monitors network traffic for suspicious activity and sends alerts.

### Active vs. Passive Devices
- **Active Devices**: Actively engage with network traffic (e.g., firewalls, IDS).
- **Passive Devices**: Monitor network traffic without interfering (e.g., network tap).

## Cloud Service Providers

### Key Differences Between Cloud and Data Centers
- **Cloud Computing**: Offers on-demand resources over the internet, with providers responsible for hardware and maintenance. This model allows for scalability, flexibility, and reduced costs.
- **Data Centers**: Organizations maintain their own physical servers, requiring responsibility for maintenance, upgrades, and downtime.

### Major Cloud Providers
- **Amazon Web Services (AWS)**: Offers a wide range of services, including computing power, storage, and machine learning.
- **Microsoft Azure**: Strong integration with Microsoft products, offering a range of services including AI and IoT.
- **Google Cloud Platform (GCP)**: Known for big data and machine learning services.
- **Oracle Cloud**: Focuses on database solutions and enterprise applications.

### Choosing a Cloud Provider
When selecting a cloud provider, consider:
- **Backup Support**: Some providers offer robust backup solutions, while others do not.
- **Service Capabilities**: Ensure the provider supports the technologies you plan to use (e.g., Linux, Windows).
- **Scalability**: Evaluate the provider's ability to scale services as your needs grow.

## Common Cyber Attacks

### Types of Cyber Attacks
1. **E-mail Bombing**: An attacker sends a large number of emails to overwhelm a user's inbox.
2. **Spoofing**: Attackers forge the sender’s address to make an email appear to be from a trusted source.
3. **Denial of Service (DoS)**: An attack that disrupts service to users, making a service unavailable.

### Mitigation Strategies
- **Implement Firewalls**: Protect your network by blocking unauthorized access.
- **Use Anti-virus Software**: Regularly scan and update to protect against malware.
- **Educate Users**: Provide training on recognizing phishing attacks and safe internet practices.

## Encryption Algorithms

### Symmetric vs. Asymmetric Encryption
- **Symmetric Encryption**: Uses the same key for both encryption and decryption (e.g., AES, DES).
- **Asymmetric Encryption**: Uses a pair of keys—public and private—for encryption and decryption (e.g., RSA).

### Overview of DES and AES
- **Data Encryption Standard (DES)**: 
  - A symmetric-key algorithm that encrypts data in 64-bit blocks.
  - Uses a 56-bit key, making it vulnerable to brute-force attacks.
  
- **Advanced Encryption Standard (AES)**: 
  - A more secure symmetric-key algorithm that supports key sizes of 128, 192, or 256 bits.
  - Operates in multiple rounds (e.g., 10 rounds for AES-128) to enhance security.

## Hybrid Storage in Cloud Services

### Benefits of Hybrid Storage
- **Flexibility**: Combines the benefits of both on-premises and cloud storage.
- **Scalability**: Easily scale resources based on demand.
- **Cost-Effectiveness**: Optimize storage costs by using cloud resources for less critical data while maintaining sensitive data on-premises.

### Cloud Providers and Hybrid Storage
- **AWS**: Offers solutions for hybrid storage like AWS Storage Gateway.
- **Azure**: Provides Azure Stack for hybrid cloud environments.
- **Google Cloud**: While focused more on public cloud, it offers some solutions for hybrid storage.

---

## Conclusion
These detailed notes cover essential concepts in Network Security and Cloud Computing as highlighted in the Accenture questions. Understanding these concepts will enhance your technical knowledge and prepare you for assessments and practical applications in the field.
```