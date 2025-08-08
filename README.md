# Elevate-Labs-Task-4

DATE: 08.08.2025

Objective:  Configure and test basic firewall rules to allow or block traffic.

STEP 1 - Open firewall configuration tool (Terminal for UFW)

bash cmd -sudo ufw status

If inactive, enable it:

bash cmd-sudo ufw enable
 UFW is now active and ready to filter network traffic.

STEP 2-List current firewall rules

bash cmd- sudo ufw status numbered
“Status: active” was shown.

STEP 3- Add a rule to block inbound traffic on port 23 (Telnet)

bash cmd-sudo ufw deny 23

STEP 4-Test the rule

bash cmd-telnet localhost 23
Port 23 is blocked; the connection is refused.

STEP 5-Add a rule to allow SSH (port 22)

bash cmd-sudo ufw allow 22
 It Ensures SSH remains accessible for remote administration.

 STEP 6- Remove the test block rule to restore original state

 bash cmd- sudo ufw status numbered
 
The Result :

Rules 1 & 3: Block Telnet (port 23) for IPv4 and IPv6

Rules 2 & 4: Allow SSH (port 22) for IPv4 and IPv6

Then remove Telnet block:


bash cmd- sudo ufw delete 1
sudo ufw delete 3

STEP 7- Document commands used

sudo ufw enable
sudo ufw status numbered
sudo ufw deny 23
telnet localhost 23
sudo ufw allow 22
sudo ufw delete 1
sudo ufw delete 3

STEP 8- SUMMARY 
( What I learned) 

A firewall monitors incoming and outgoing packets based on rules.
It decides whether to allow, deny, or reject traffic based on:

Port number (e.g., 22 for SSH, 23 for Telnet)

Protocol (TCP, UDP)

IP address (source/destination)

UFW applies rules in order and enforces them at the kernel level using iptables.

On this Task:

-->I blocked Telnet (port 23) to improve security.

-->I allowed SSH (port 22) to maintain remote access.

-->I verified the block with Telnet and confirmed a connection refusal.

Outcome: Basic firewa l management skils and understanding of network traffic filtering

( ATTACHED WITH SCREENSHOTS ON LINUX)







