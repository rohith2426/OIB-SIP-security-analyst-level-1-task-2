Perfect! I've created a comprehensive README.md file in your repository. Here's what was included:

```markdown name=README.md url=https://github.com/rohith2426/OIB-SIP-security-analyst-level-1-task-2/blob/main/README.md
# Basic Firewall Configuration with UFW

## 📌 Objective

The objective of this task is to configure a basic firewall using UFW (Uncomplicated Firewall) on a Linux system. The firewall is configured to allow SSH traffic and deny HTTP traffic, ensuring secure remote access while blocking web traffic.

---

## 🛠 Tools Used

- **UFW (Uncomplicated Firewall)** - Simple firewall management tool
- **Linux Operating System** (Ubuntu recommended)
- **Terminal** - Command-line interface

---

## 📂 Project Files

```
.
├── ufw_configuration.sh   # Script to configure firewall rules
├── screenshot.png         # Screenshot showing UFW status and rules
└── README.md              # Documentation of the configuration
```

---

## ⚙ Installation of UFW

First, install UFW on your Linux system.

### Step 1: Update Package Manager
```bash
sudo apt update
```

### Step 2: Install UFW
```bash
sudo apt install ufw
```

### Step 3: Check the Version
```bash
ufw --version
```

---

## 🔧 Firewall Configuration

### 1️⃣ Allow SSH

SSH access is required for remote system management.

**Option A:** Using service name
```bash
sudo ufw allow ssh
```

**Option B:** Using port number
```bash
sudo ufw allow 22
```

### 2️⃣ Deny HTTP Traffic

Block HTTP traffic on port 80.

**Option A:** Using service name
```bash
sudo ufw deny http
```

**Option B:** Using port number
```bash
sudo ufw deny 80
```

### 3️⃣ Enable UFW Firewall

Activate the firewall.

```bash
sudo ufw --force enable
```

### 4️⃣ Check Firewall Status

Verify the firewall rules and status.

```bash
sudo ufw status verbose
```

**Expected output should show:**

- ✅ SSH (port 22) allowed
- ❌ HTTP (port 80) denied
- 🔒 Firewall status: **Active**

---

## 📜 Script Used (ufw_configuration.sh)

```bash
#!/bin/bash

# Install UFW
sudo apt update
sudo apt install ufw -y

# Allow SSH
sudo ufw allow ssh

# Deny HTTP
sudo ufw deny http

# Enable firewall
sudo ufw --force enable

# Show status
sudo ufw status verbose
```

### How to Run the Script:

1. Make the script executable:
   ```bash
   chmod +x ufw_configuration.sh
   ```

2. Execute the script:
   ```bash
   ./ufw_configuration.sh
   ```

---

## 📸 Screenshots

Include screenshots showing the output of:

```bash
sudo ufw status
```

**The screenshot should display:**

- Active firewall status
- Configured firewall rules
- SSH (port 22) in the "Allow" list
- HTTP (port 80) in the "Deny" list

---

## ✅ Expected Results

Upon successful configuration, you should observe:

- ✅ UFW firewall successfully installed
- ✅ SSH traffic allowed on port 22
- ✅ HTTP traffic blocked on port 80
- ✅ Firewall status verified and active
- ✅ All rules properly configured and displayed in `ufw status verbose`

---

## 📋 Configuration Summary

| Rule | Action | Port | Protocol |
|------|--------|------|----------|
| SSH | ALLOW | 22 | TCP |
| HTTP | DENY | 80 | TCP |

---

## 🔐 Security Benefits

1. **SSH Access**: Enables secure remote management via SSH
2. **HTTP Blocking**: Prevents unauthorized web traffic and potential web-based attacks
3. **Simple Management**: UFW provides an easy-to-use interface for firewall management
4. **Default Deny Policy**: Implicit deny for any traffic not explicitly allowed

---

## 📚 Conclusion

This project demonstrates how to configure a basic firewall using UFW in Linux to control network access. By allowing SSH and blocking HTTP, we ensure secure remote management while restricting unnecessary web traffic.

### Key Takeaways:

- UFW is a user-friendly firewall management tool for Linux systems
- Explicit allow/deny rules provide granular control over network traffic
- SSH is essential for secure remote administration
- Regular firewall audits and rule reviews are important for security maintenance

---

## 🔗 Additional Resources

- [UFW Official Documentation](https://help.ubuntu.com/community/UFW)
- [Linux Firewall Basics](https://www.linux.com/training-tutorials/)
- [SSH Security Best Practices](https://www.ssh.com/ssh/security/)

---

**Last Updated**: 2026-03-04  
**Status**: ✅ Complete
```

The README.md file has been successfully created in your repository with:

✅ Complete project overview and objectives  
✅ Step-by-step installation instructions  
✅ Detailed firewall configuration steps  
✅ Executable bash script  
✅ Security benefits and best practices  
✅ Configuration summary table  
✅ Expected results and verification steps  

The file is now available in your GitHub repository and provides comprehensive documentation for the UFW firewall configuration task!
