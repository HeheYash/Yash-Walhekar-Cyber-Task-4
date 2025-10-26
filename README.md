# Yash-Walhekar-Cyber-Task-4

## Setup and Use a Firewall on Windows

This repository contains the deliverables for Task 4 of the Cybersecurity Internship program. The objective of this task was to configure and test a basic Windows Firewall rule to block specific network traffic.

---

### Tool Used

* **Platform:** Windows
* **Tool:** Windows Defender Firewall with Advanced Security

---

### Summary: How a Firewall Filters Traffic

A firewall is a network security system that monitors and controls incoming and outgoing network traffic based on a set of predefined security rules. It acts as a filter between a trusted internal network (my computer) and untrusted external networks (the internet).

It works by inspecting data packets and deciding whether to allow or block them based on rules that check for IP addresses, ports (like port 23), and protocols (like TCP).

---

### Process and Steps Performed

To complete this task, I used the "New Inbound Rule Wizard" in Windows Defender Firewall. The exact steps are documented in the screenshots provided in this repository.

1.  **Start:** Opened **Windows Defender Firewall with Advanced Security** and selected **Inbound Rules** (as seen in `Step 1.jpg`).
2.  **New Rule:** Clicked **New Rule...** from the "Actions" pane (as seen in `Step 2.jpg`).
3.  **Rule Type:** (Inferred) Selected the **Port** rule type.
4.  **Protocol and Ports:** Specified the rule to apply to **TCP** and **Specific local ports: 23** (as seen in `Step 3.png`).
5.  **Action:** Chose the **Block the connection** action (as seen in `Step 4.png`).
6.  **Profile:** Applied the rule to all three network profiles: **Domain, Private, and Public** (as seen in `Step 5.png`).
7.  **Name:** Named the rule **"Internship Task 4(Test Rule)"** to complete the wizard (as seen in `Step 6.png`).
8.  **Test:** Opened PowerShell and ran `Test-NetConnection -ComputerName 127.0.0.1 -Port 23` to test the rule.
9.  **Result:** The test **failed** (`TcpTestSucceeded : False`), confirming that the firewall is successfully blocking inbound connections on port 23 (as seen in `Step 7.png`).
10. **Cleanup:** (After testing) The "Internship Task 4(Test Rule)" was deleted to restore the system to its original state.

---

### Deliverables: Screenshots

The following screenshots document the key steps of the process: creating the rule and testing it.

#### Screenshot 1: Final Step of Rule Creation
*(This image shows the name given to the rule just before it was created.)*

![Final Step of Rule Creation](Step%206.png)

#### Screenshot 2: Test Result
*(This image shows the PowerShell output. `TcpTestSucceeded : False` proves the port is successfully blocked.)*

![Test Result](Step%207.png)

---

### Task Outcome

This task provided hands-on experience in configuring and verifying a firewall rule on Windows. It demonstrated how to block a specific port (port 23) to enhance system security by preventing insecure protocols like Telnet.
