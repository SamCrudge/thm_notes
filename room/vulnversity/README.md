# /room/vulnversity

### NMAP

Command:

```bash
nmap -sV -A -p- -oN nmap/nmap_report.txt 10.10.108.215
```

Ports:

```bash
21
22
139
445
3128
3333
```
21 ftp
22 ssh
139 netbios-ssn smbd
445 netbios-ssn
3128 squid proxy
3333 http 


OS:
Ubuntu

Web Server:
Apache


### GoBuster

Command:
```bash

```

Endpoints found:
```bash
/internal
/css
/fonts
/js
/images/
```

/images/ upload

What isnt allowed: Guessed PHP

Do /room/burpsuitebasics