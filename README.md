
# 🔐 Basic Device Security Lab (Cisco Packet Tracer)

## 🎯 Objective
Apply basic security configurations on Cisco routers and switches using Packet Tracer. Learn hostname configuration, password setting, encryption, and configuration saving.

---

## 🛠 Requirements
- Cisco Packet Tracer (latest version)
- Lab File: `Day 04 Lab - Basic Device Security.pkt`

---

## 🧪 Lab Tasks & Commands

### 1. Change Hostnames
```bash
Router> enable
Router# configure terminal
Router(config)# hostname R1

Switch> enable
Switch# configure terminal
Switch(config)# hostname SW1
```

### 2. Set Unencrypted Enable Password
```bash
R1(config)# enable password CCNA
SW1(config)# enable password CCNA
```

### 3. Exit and Test the Password
```bash
R1(config)# exit
R1# exit
R1> enable
# Use password: CCNA
```

### 4. View the Password in Running Config
```bash
R1# show running-config
```

### 5. Encrypt All Passwords
```bash
R1(config)# service password-encryption
SW1(config)# service password-encryption
```

### 6. Recheck Config for Encrypted Passwords
```bash
R1# show running-config
```

### 7. Set Encrypted Enable Secret
```bash
R1(config)# enable secret Cisco
SW1(config)# enable secret Cisco
```

### 8. Exit and Re-enter Privileged EXEC Mode
```bash
R1> enable
# Use password: Cisco
```

### 9. Identify Encryption Types
```bash
R1# show running-config
# enable password = type 7
# enable secret = type 5
```

### 10. Save Running to Startup Config
```bash
R1# copy running-config startup-config
```

---

## 📁 Files
- `Day 04 Lab - Basic Device Security.pkt`

---

## 🧠 Key Concepts
- Use `enable secret` instead of `enable password` for better security.
- Always run `service password-encryption` to protect future passwords.
- Save config regularly to prevent loss on reboot.

