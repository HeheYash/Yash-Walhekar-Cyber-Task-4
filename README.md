# Yash-Walhekar-Cyber-Task-4

# Elevate Labs - Cybersecurity Internship: Task 4
## Setup and Use a Firewall on Windows

This repository contains the deliverables for Task 4 of the Cybersecurity Internship program. The objective of this task was to configure and test a basic Windows Firewall rule to block specific network traffic.

### Tool Used

* **Platform:** Windows
* **Tool:** Windows Defender Firewall with Advanced Security

### Summary: How a Firewall Filters Traffic

A firewall is a network security system that monitors and controls incoming and outgoing network traffic based on a set of predefined security rules. It acts as a filter between a trusted internal network (my computer) and untrusted external networks (the internet).

It works by inspecting data packets and deciding whether to allow or block them based on rules that check for IP addresses, ports (like port 23), and protocols (like TCP).

---

### Process and Steps Performed

To complete this task, I used the "New Inbound Rule Wizard" in Windows Defender Firewall. The entire process is documented in the screenshots below.

1.  **Start:** Opened **Windows Defender Firewall with Advanced Security** and selected **Inbound Rules**. (See: `Step 1.jpg`)
2.  **New Rule:** Clicked **New Rule...** from the "Actions" pane to start the wizard. (See: `Step 2.jpg`)
3.  **Protocol and Ports:** Specified the rule to apply to **TCP** and **Specific local ports: 23**. (See: `Step 3.png`)
4.  **Action:** Chose the **Block the connection** action. (See: `Step 4.png`)
5.  **Profile:** Applied the rule to all three network profiles: **Domain, Private, and Public**. (See: `Step 5.png`)
6.  **Name:** Named the rule **"Internship Task 4(Test Rule)"** to complete the wizard. (See: `Step 6.png`)
7.  **Test:** Opened PowerShell and ran `Test-NetConnection -ComputerName 127.0.0.1 -Port 23` to test the rule. The test **failed** (`TcpTestSucceeded : False`), confirming the block was active. (See: `Step 7.png`)
8.  **Cleanup:** After testing, the "Internship Task 4(Test Rule)" was deleted to restore the system to its original state.

---

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

---

### Task Outcome

This task provided hands-on experience in configuring and verifying a firewall rule on Windows. It demonstrated how to block a specific port (port 23) to enhance system security by preventing insecure protocols like Telnet.
