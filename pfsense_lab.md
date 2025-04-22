# 🔐 Securing pfSense Firewall Lab

This project demonstrates how to secure a pfSense firewall by removing insecure and unneeded services, scanning for open ports using `nmap`, zenmap and configuring secure protocols.

## 🧪 Lab Overview

In this lab, I worked with the pfSense open-source firewall, widely used for network security. The goal was to identify and close unnecessary ports and services, and configure the firewall to accept only secure connections.

## 🎯 Objectives

- ✅ Scan open ports on pfSense using `nmap` and 'Zenmap'
- ✅ Close unnecessary and insecure ports
- ✅ Add a secure service to the pfSense firewall

## 🔧 Tools Used

- 🖥️ pfSense Firewall
- 🌐 nmap (Network Mapper)
- 💻 Virtual Machine / Lab Environment

## 🛠️ Steps Performed

1. **Initial nmap Scan**
   - Identified all open ports on the pfSense firewall
   - Example command used:
     ```bash
     nmap <pfSense_IP>
     ```
     ![Screenshot (97)](https://github.com/user-attachments/assets/cea6c13d-9cde-49bd-ae1a-4a3cac60eda0)


     
2. **Port Scan Using Zenmap**

    - Run a scan using Zenmap GUI for visual output
   
    - Profile used: "Intense Scan"
  
     ![Screenshot (99)](https://github.com/user-attachments/assets/bdcce544-c3eb-4813-8f6c-82f9d94c3bfa)


   
    - Exported results to XML/HTML for reporting

2. **Analyzed Services**
   
   - Identified unnecessary services (e.g., Telnet, FTP)
     
3. **Disabled Insecure Protocols**
   - Disabled unneeded services from pfSense web UI
     
     Steps to Disable Services:
     
     Review NAT Port Forwards
     
     Go to: Firewall > NAT > Port Forward
     
     Review each rule:
     
     If it’s not needed (e.g., old remote access, game server, IP camera, etc.) — delete or disable it.
     
     Click the trash icon to delete or the check icon to disable.

     ![Screenshot (103)](https://github.com/user-attachments/assets/fe44e9bd-f135-4d47-9646-38603522c3ac)


4. **Enabled Secure Services**
   - Configured SSH
     
     Review NAT Port Forwards
     
     Go to: Firewall > NAT > Port Forward
     
     Destination port range: SSH (or 2222 if you customized the port)


     ![Screenshot (105)](https://github.com/user-attachments/assets/c177edbc-df83-4362-81e4-a66f5fe75259)
     


     ![Screenshot (107)](https://github.com/user-attachments/assets/60bd3314-9af0-48f1-bcdb-e41c89e635f8)


   

6. **Final nmap Scan**
   - Verified only necessary secure ports are open

    Using nmap
  
     ![Screenshot (108)](https://github.com/user-attachments/assets/a6c9c80f-f420-4fbe-8726-15840ba1f5cb)

   Using zenmap

    ![Screenshot (109)](https://github.com/user-attachments/assets/f30ead48-ef36-41ce-b022-63a65dd7575c)



## 📚 Learning Outcome

- Gained hands-on experience with network scanning and firewall configuration
- Improved understanding of minimizing attack surfaces
- Learned to use `nmap` effectively for security audits

