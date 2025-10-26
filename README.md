# Yash-Walhekar-Cyber-Task-4

## Setup and Use a Firewall on Windows

This repository will hold the deliverables of the Task 4 of Cybersecurity Internship program. This task had the intention of configuring and testing a simple windows firewall rule to limit a certain network traffic.

### Tool Used

* **Platform:** Windows
* **Hardware/software:** Windows Defender Firewall with Advanced Security.

### Summary: How a Firewall Filters Traffic

A firewall is a network defense system that will observe and control the traffic that moves within a network and that which exits it without disobedience to a collection of established security rules. It serves as a blocker between a set of trusted internal network (my computer) and the non-trusted external networks (the internet).

It operates on the principle of examining data packets and either permitting or rejecting them depending on rules that examine such data packets against IP address, ports (such as port 23), and protocols (such as TCP).

### Process and Steps Performed

In order to accomplish this task, I applied the New Inbound Rule wizard of windows defender firewall. The whole procedure is recorded in the following screen shots.

1.  **Start:** Opened **Windows Defender Firewall with Advanced Security** and selected **Inbound Rules**. (See: `Step 1.jpg`)
2.  **New Rule:** Clicked **New Rule...** from the "Actions" pane to start the wizard. (See: `Step 2.jpg`)
3.  **Protocol and Ports:** Specified the rule to apply to **TCP** and **Specific local ports: 23**. (See: `Step 3.png`)
4.  **Action:** Chose the **Block the connection** action. (See: `Step 4.png`)
5.  **Profile:** Applied the rule to all three network profiles: **Domain, Private, and Public**. (See: `Step 5.png`)
6.  **Name:** Named the rule **"Internship Task 4(Test Rule)"** to complete the wizard. (See: `Step 6.png`)
7.  **Test:** Opened PowerShell and ran `Test-NetConnection -ComputerName 127.0.0.1 -Port 23` to test the rule. The test **failed** (`TcpTestSucceeded : False`), confirming the block was active. (See: `Step 7.png`)
8.  **Cleanup:** After testing, the "Internship Task 4(Test Rule)" was deleted to restore the system to its original state.

### Deliverables: All Step Screenshots

Here are all 7 screenshots documenting the process from start to finish.

**Step 1: Open Inbound Rules**
![Open Inbound Rules](Step%201.png)

**Step 2: Create New Rule**
![Create New Rule](Step%202.png)

**Step 3: Specify Protocol and Port**
![Specify Protocol and Port](Step%203.png)

**Step 4: Specify Action (Block)**
![Specify Action](Step%204.png)

**Step 5: Specify Profile**
![Specify Profile](Step%205.png)

**Step 6: Name the Rule**
![Name the Rule](Step%206.png)

**Step 7: Test the Rule (PowerShell)**
![Test the Rule](Step%207.png)

### Task Outcome

This assignment helped to get more practical experience on how to configure and test a windows firewall rule. It showed how it was possible to block a certain port (port 23) to improve the security of the system by blocking dangerous protocols, such as Telnet.
