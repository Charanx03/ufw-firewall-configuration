# 🛡️ Task 4: Setup and Use a Firewall on Linux (UFW)

## 🎯 Objective
Configure and test basic firewall rules to allow or block traffic.

## 🧰 Tools
- UFW (Uncomplicated Firewall) on Linux

---

## Step 1: Enable UFW Firewall

First, enable UFW if it is not already active.

```bash
sudo ufw enable
```
## 📸 Screenshot
![01_firewall_enabled](https://github.com/user-attachments/assets/de286b1d-8463-4fe9-9e1a-62fae2d839b6)

## Step 2: List Current Firewall Rules

Check the current rules to understand the starting state.

```bash
sudo ufw status numbered
```

## Step 3: Block Inbound Traffic on Port 23 (Telnet)

Add a rule to block inbound traffic on port 23, commonly used by Telnet.

```bash
sudo ufw deny 23
```
## 📸 Screenshot
![02_rule_blocked_port_23](https://github.com/user-attachments/assets/cb119abc-6491-4a2d-9482-b45a93a0dabe)

## Step 4: Test the Block Rule

Attempt to connect to port 23 locally or remotely to verify the block.

```bash
telnet localhost 23
```
## 📸 Screenshot
![03_telnet_test](https://github.com/user-attachments/assets/4b161eb0-785d-4346-a2f1-90af1fbbec2f)

## Step 5: Allow SSH Access on Port 22

To ensure secure remote access, allow SSH traffic.

```bash
sudo ufw allow 22
```
## 📸 Screenshot
![04_ssh_allowed](https://github.com/user-attachments/assets/b88f158c-03da-44cd-9904-b747dbf8f607)

## Step 6: Remove the Test Block Rule for Port 23

Clean up by removing the block rule on port 23 to restore the original state.

```bash
sudo ufw delete deny 23
```
## 📸 Screenshot
![05_rule_deleted](https://github.com/user-attachments/assets/23e0ac59-9644-4081-8347-9f9805ac5062)

---
## 🔍 Summary: How Firewall Filters Traffic
- UFW is a tool that helps manage which network connections are allowed or blocked.
- You can set rules to allow or deny traffic on certain ports (like 22 for SSH or 23 for Telnet).
- When data tries to come into your computer, UFW checks the rules:
   - If it's allowed, it lets it through.
   - If it's denied, it blocks it.
- This helps protect your system from attackers or unwanted access.







