# BASH Script Lab – Bash Script To Drop a list of IP Addresses

## Objective

The objective of this script is to block incoming network traffic from a list of specified IP addresses using the iptables firewall in Linux. It automates the process of applying IP-based traffic restrictions for network security purposes.

### Job Skills Learned

- Linux System Administration
- Managing firewall rules using iptables.
- Bash Shell Scripting
- Using loops and conditional commands.
- Network Security and Access Control
- Automation and Efficiency


### Tools Used

- Linux Terminal Command Line Interface (CLI)
- Bash Shell
- iptables (Firewall)
- Networking Commands: ping, ifconfig
- VMware Tools: Linux VM

*Ref: Diagram:
![image](https://github.com/user-attachments/assets/94d22d7d-06cb-415d-b6b3-804f5aeb920d)
 


### STEPS
![image](https://github.com/user-attachments/assets/a65f6609-5193-4cd7-9289-72fa3794585b)
 

How the Script Works:
1.	IP List Definition:
The variable DROPPED_IPS contains a whitespace-separated list of IP addresses to be blocked (dropped).
2.	Iterating Over IPs:
A for loop iterates through each IP in the list.
3.	Blocking Traffic:
The script uses the iptables command to insert (-I) a rule into the INPUT chain of the firewall to drop (-j DROP) any packets coming from each specified IP.
o	-I INPUT: Inserts the rule at the top of the INPUT chain, ensuring it's evaluated first.
o	-s $ip: Specifies the source IP to block.
o	-j DROP: Drops packets silently without sending a response.
4.	Running the Script:
The script needs to be run with superuser privileges (sudo) because modifying iptables requires administrative access.
![image](https://github.com/user-attachments/assets/2fdd5f2f-a092-4c1a-9cc1-19a47d3041e8)


## Practical Application:
-	Blocking unwanted or malicious IPs to prevent attacks like DDoS or unauthorized access.

-	Creating quick, automated scripts for network security hardening.

-	Managing access control in Linux servers, especially in web servers, databases, or firewalls.


