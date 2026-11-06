# Kali Linux Lab Setup and Network Configuration

## 1. Introduction

This project documents the installation and configuration of a Kali Linux virtual machine using Oracle VM VirtualBox. It covers the virtual machine configuration, network interface identification, IP addressing, and connectivity verification.

## 2. Lab Objectives

The objectives of this exercise were to:

- Set up a Kali Linux virtual machine.
- Configure the virtual machine using VirtualBox.
- Identify available network interfaces.
- Verify IP address configuration.
- Identify the default network gateway.
- Test local gateway and external network connectivity.
- Verify DNS resolution.

## 3. Lab Environment

| Component | Configuration |
|---|---|
| Host virtualization software | Oracle VM VirtualBox |
| Guest operating system | Kali Linux |
| OS architecture | 64-bit |
| Network interface | eth0 |
| IPv4 address | 10.0.0.2 |
| Subnet mask | 255.255.255.0 |
| Default gateway | 10.0.0.1 |
| RAM allocated | Approximately 5066 MB |

## 4. Network Configuration

The `ip a` command was used to inspect the network interfaces and identify their assigned IP addresses.

The primary network interface identified was `eth0`.

Observed configuration:

- Interface: eth0
- IPv4 address: 10.0.0.2/24
- Network: 10.0.0.0/24
- Broadcast address: 10.0.0.255

The loopback interface was also present with the address 127.0.0.1.

## 5. Network Connectivity Testing

### 5.1 Default Gateway Test

The following command was executed:

`ping -c 4 10.0.0.1`

Result: Four packets were transmitted and four packets were received, with 0% packet loss.

This confirmed connectivity between the Kali Linux virtual machine and its default gateway.

### 5.2 External IP Connectivity Test

The following command was executed:

`ping -c 4 8.8.8.8`

Result: Four packets were transmitted and four packets were received, with 0% packet loss.

This confirmed connectivity to the external IP address used for testing.

### 5.3 DNS Resolution Test

The following command was executed:

`ping -c 4 google.com`

Result: The hostname resolved to an IP address and four packets were received, with 0% packet loss.

This confirmed that DNS resolution and external hostname connectivity were working during the test.

## 6. Results

| Test | Result |
|---|---|
| Kali Linux virtual machine setup | Successful |
| Network interface identification | Successful |
| IP address verification | Successful |
| Default gateway connectivity | Successful |
| External IP connectivity | Successful |
| DNS resolution | Successful |

## 7. Conclusion

The Kali Linux virtual machine was successfully configured in VirtualBox. The network interface received an IPv4 address, and connectivity tests confirmed communication with the default gateway and an external network address.

Hostname resolution was also verified using a ping test to google.com.

This exercise provided practical experience with Linux network interface inspection, IP configuration, gateway connectivity, and basic network troubleshooting.

## 8. Evidence

Screenshots supporting the lab activities are available in the repository's `screenshots` directory.

- VirtualBox configuration
- Kali Linux network interface configuration
- Gateway connectivity test
- External connectivity and DNS resolution tests
