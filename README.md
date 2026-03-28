# Cybersecurity-Lab-2
# Lab 2: Network Service Auditing & Automated Credential Testing
Overview
This laboratory focuses on identifying network services, simulating a brute-force attack against a local SSH server, and analysing the resulting traffic patterns. The objective is to understand how automated tools exploit weak credentials and how these activities appear from a network monitoring perspective.
## 1. Phase 1: Environment Setup & Service Deployment
Objective: To establish a controlled target environment by deploying a standard network service. In this phase, an OpenSSH server is installed and activated on the local Kali Linux instance. This service will serve as the primary target for subsequent security auditing and brute-force simulation.

![image](https://github.com/user-attachments/assets/48dcdfc4-4c0e-4965-9cf2-ec862e91dda4)


## 2. Phase 2: Service Discovery & Port Scanning
Objective: To verify the target service's availability and identify the network attack surface. Using Nmap, the local host is scanned to confirm that port 22 (SSH) is open and actively listening for incoming connections. This phase ensures the environment is correctly configured before the simulation begins.

![image](https://github.com/user-attachments/assets/e1ce879f-522b-430d-9f51-ee3336980378)


## 3. Phase 3: Attack Preparation & Wordlist Creation
Objective: To configure necessary assets for a brute-force simulation. Custom wordlists containing targeted usernames and common passwords are generated to simulate a real-world dictionary attack. This phase illustrates the fundamental requirement for structured data in automated security testing.

![image](https://github.com/user-attachments/assets/066c4454-2442-4c41-b45b-2e061311d6ea)

## 4. Phase 4: Automated Brute-Force Simulation
Objective: To simulate a high-speed dictionary attack against the identified SSH service. Using Hydra, the generated wordlists are utilised to attempt various credential combinations systematically. This phase demonstrates how automated tools can identify weak or reused passwords through rapid iteration.

![image](https://github.com/user-attachments/assets/2f7c6056-ced4-4d7a-84e1-635f925bbb9e)


## 5. Phase 5: Traffic Analysis & Packet Inspection
Objective: To monitor and analyse the network signature of an automated brute-force attack. Using Wireshark on the loopback interface, the captured traffic reveals a rapid sequence of TCP handshakes and SSHv2 protocol exchanges. This granular visibility allows for the identification of automated credential stuffing by observing high-frequency connection patterns from a single source.

 ![image](https://github.com/user-attachments/assets/f3ae12fa-ab52-4ee1-82c3-d80d5b4f5f7c)


## 6. Phase 6: Custom Python Automation
Objective: To develop and execute a standalone Python tool for automated credential validation. By utilising the Paramiko library, the manual brute-force process is streamlined into a programmatically driven sequence. This phase demonstrates the ability to automate security auditing tasks, allowing for efficient verification of identified credentials through a custom scripted interface.

![image](https://github.com/user-attachments/assets/fe8e0a85-ef36-4f4e-9dd7-d9cfdf6bfffc)



# Conclusion
The successful completion of Lab 2 demonstrates the critical relationship between service configuration, automated auditing, and network visibility. Through the deployment of an SSH server and the subsequent execution of dictionary-based attacks, the vulnerability of weak credentials to high-speed automation was clearly illustrated.

Furthermore, the integration of protocol analysis via Wireshark and custom Python scripting highlights the dual nature of modern security: the ability to both execute and detect sophisticated automated tasks. This laboratory provides a foundational understanding of the "noisy" signatures left by brute-force tools and emphasises the necessity of robust password policies and continuous monitoring in securing network infrastructure.
