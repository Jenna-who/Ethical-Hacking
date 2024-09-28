
# Getting Started with Nmap

## Before we start

### Prerequisite
A basic understanding of networking concepts such as IP addresses, ports, and protocols (TCP/UDP) is essential. Familiarity with command-line interfaces (CLI) is also helpful since Nmap is primarily used via the terminal.

### Why use Nmap?
Nmap (Network Mapper) is an essential tool for network scanning and security auditing. It helps you discover devices on a network, identify open ports, and check for vulnerabilities. Whether you're managing a network or interested in security, Nmap will become a go-to tool.

### Installation
If you're using Kali Linux, Nmap is pre-installed. For other Linux distributions, install it via the package manager:

- **Debian/Ubuntu:**
  ```bash
  sudo apt install nmap
  ```
- **CentOS/RHEL:**
  ```bash
  sudo yum install nmap
  ```

- **Windows:**
  Download the installer from the Nmap website.

- **macOS:**
  If you’re on macOS, install Nmap via Homebrew:
  ```bash
  brew install nmap
  ```

## Basic Usage

Nmap follows a simple syntax:

```bash
nmap [options] <target>
```

- **[options]**: Modify the scan type or add features.
- **<target>**: The IP address or hostname you want to scan.

### Common Nmap Commands

Here are some commonly used Nmap commands:

- **Basic Scan**  
  Scans the top 1,000 most common ports on a target:
  ```bash
  nmap <target>
  ```

- **Full Port Scan**  
  Scans all 65,535 ports, providing a complete picture:
  ```bash
  nmap -p- <target>
  ```

- **Service and Version Detection**  
  Identifies services running on open ports and attempts to determine their version:
  ```bash
  nmap -sV <target>
  ```

- **Operating System Detection**  
  Tries to detect the target's operating system:
  ```bash
  nmap -O <target>
  ```

- **Aggressive Scan**  
  Combines several scans (OS detection, version detection, script scanning, and traceroute):
  ```bash
  nmap -A <target>
  ```

- **Scan Specific Ports**  
  Use this to scan a range of ports, or just specific ones:
  ```bash
  nmap -p 22,80,443 <target>
  ```

- **Stealth Scan (SYN Scan)**  
  Conducts a stealthy scan that is less likely to be detected by firewalls:
  ```bash
  nmap -sS <target>
  ```

- **Ping Scan**  
  Finds live hosts in a network without scanning ports:
  ```bash
  nmap -sn <target>
  ```

- **Scan a Subnet**  
  Scans an entire subnet or IP range:
  ```bash
  nmap 192.168.1.0/24
  ```

- **Scan Multiple Targets**  
  You can list multiple IPs or ranges in a single scan:
  ```bash
  nmap <target1> <target2> <target3>
  ```

---

