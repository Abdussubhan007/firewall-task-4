# firewall-task-4

# Task 4 – Windows Firewall Configuration (Cyber Security Internship)

## Objective
To configure and test basic firewall rules on Windows to allow or block traffic, and gain an understanding of how firewall rules manage network ports.

## Tools Used
- Operating System: Windows 10/11  
- Firewall Tool: Windows Defender Firewall with Advanced Security  
- Command Line Tool: Command Prompt (cmd)  
- Telnet Client: Installed using Windows Features  

## Steps Performed

### 1. Open Firewall Settings  
- Accessed Windows Defender Firewall using `wf.msc`.  
- Screenshot taken showing main interface.

### 2. View Current Rules  
- Opened Inbound Rules and Outbound Rules to see default settings.

### 3. Block Port 23 (Telnet)  
- Created a new Inbound Rule to block TCP traffic on port 23 (Telnet).  
- Named the rule `Block Telnet Port 23`.

### 4. Test Rule  
- Attempted to connect using:  
  `telnet 127.0.0.1 23`  
- Connection failed with error:  
  “Could not open connection to the host, on port 23: Connect failed”  
- ✅ Indicates port 23 was successfully blocked.

### 5. Remove the Rule  
- Deleted the firewall rule named `Block Telnet Port 23`.

### 6. Retest Telnet  
- Retried `telnet 127.0.0.1 23`  
- Connection still failed — this is expected because Windows does not run a Telnet server by default.

## Testing Summary
- Port 23 remained inaccessible before and after removing the rule.
- Verified using:  
  `netstat -an | find ":23"`  
- This confirms the firewall rule was effective and no local service was available.

## Screenshots
All screenshots from each step are included in this repository:
- step1_firewall_open.png  
- step2_rules_list.png  
- step3_block_rule.png  
- step4_telnet_test.png  
- step5_rule_deleted.png

## Outcome
- Gained hands-on experience with Windows Firewall  
- Learned how to create, test, and delete inbound rules  
- Understood how firewalls control traffic through ports
