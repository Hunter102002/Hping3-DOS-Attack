# hping3 DoS Attack Simulation

## Objective

Conducted a controlled Denial of Service (DoS) attack simulation on a Windows 10 machine to understand the impact and mitigation of network-based attacks.

### Skills Learned

- Packet Crafting: Using hping3 to create and send custom TCP SYN packets for targeted DoS attacks.
- Network Scanning: Utilizing Nmap to discover and enumerate open ports on the target machine.
- System Impact Analysis: Monitoring system response and resource consumption during the DoS attack.
- Linux Command Line: Executing attack commands and analysis from a Kali Linux environment.

### Tools Used

- Kali Linux: As the attack platform for executing hping3 and Nmap commands.
- hping3: For generating TCP SYN flood traffic to simulate a DoS attack.
- Nmap: For scanning the target system to identify vulnerable open ports.
- Task Manager: For monitoring the impact on system resources during the attack on the Windows 10 machine.

### Outcome
This project successfully demonstrated the process and impact of a DoS attack on a Windows 10 system. It showcased essential skills in packet crafting, network scanning, system impact analysis, and effective use of the Linux command line within a cybersecurity context.

## Steps

Ping both machines to ensure communication between machines

![Screenshot 2024-08-19 150418](https://github.com/user-attachments/assets/9f30c8a3-01ba-4cb6-9af2-78bfda4ffffc)

![Screenshot 2024-08-19 150445](https://github.com/user-attachments/assets/dbb17e0b-b3e7-4d9e-a8fb-7bae4bf687f4)

-----------------------------------------------------------------------------------------------

Run an NMAP scan on the target machine 

![Screenshot 2024-08-19 150522](https://github.com/user-attachments/assets/6dc5229c-1bde-471c-9906-ecd695c97917)

-----------------------------------------------------------------------------------------------

Run an hping scan on the machine to get more information (--rand-source) to stay anonymous 

![Screenshot 2024-08-19 150750](https://github.com/user-attachments/assets/478b7146-6e39-4756-a95b-77185279233d)

-----------------------------------------------------------------------------------------------

Get a baseline for the target machine usage by opening task manager -> Performance 

![Screenshot 2024-08-19 151041](https://github.com/user-attachments/assets/efd13380-24eb-45fb-9d89-eeb2eca76a68)

-----------------------------------------------------------------------------------------------

Run an attack on the target machine (-c). How many packets (-d) the size of the packets (-p) is for the port we are targeting 135. (--flood) is for a flood attack 

![Screenshot 2024-08-19 151442](https://github.com/user-attachments/assets/d9987433-349e-4c8c-aea8-cb4290391d10)

![Screenshot 2024-08-19 151138](https://github.com/user-attachments/assets/db27ec50-1ae4-489a-a77c-51c91bf1a678)

-----------------------------------------------------------------------------------------------

Now another attack but this time we are going to increase the size of the attack (--data)


![Screenshot 2024-08-19 153025](https://github.com/user-attachments/assets/9c53a3f0-8b51-4b75-9491-152c4ca942ae)

![Screenshot 2024-08-19 151428](https://github.com/user-attachments/assets/2f57b342-4ce7-443c-8629-61b1d12c46ba)

-----------------------------------------------------------------------------------------------
From here, we can configure our firewall settings to try to deny these flood attacks on the vulnerable machine.
