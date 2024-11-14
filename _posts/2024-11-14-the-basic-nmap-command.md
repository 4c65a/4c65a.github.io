---
title: The basic nmap command
author: 
date: 2024-11-14 15:00:00 +0000
categories: [Tutorial,Networks]
tags: [nmap]
---
# What is NMAP?

Nmap is a network scanner , used to discover hosts and services on a computer network. The nmap utility is  used for network port mapping.

## Basic nmap command

Now, it is a more basic command with which you can scan a private network.

```
nmap 192.168.0.0/24
```

Adding more commands.

```
nmap -sS -p- 192.168.0.0/24
```

The `-sS` flag is one of the most popular scan types, used for scanning the TCP protocol. The `-sS` flag is the fastest way to scan.

The `-p-` flag scans all 65,535 ports.

Now, at a more difficult level, adding more commands in the following way: `-sCV`, `-p 80,443`, `--min-rate 5000`.

```
nmap -sCV -p 80,443  --min-rate 5000 192.168.0.0/24
```
With `-sC`, you execute NSE (Nmap Scripting Engine) scripts to get detailed information about the system. The `-sV` option scans the system to identify services and their versions.

Using `-p`, you can also scan specific ports, and `--min-rate` helps set a minimum rate, allowing you to skip hosts that take too long to scan.

Also you can add multiple IP addresses.
```
nmap -sCV -p 80,443  --min-rate 5000 192.168.0.0 192.168.0.102 192.168.0.100
```

Use scan by fragmentation, used to avoid firewalls.
```
nmap -f 192.168.0.0
```

If you want to know the system used
```
nmap -O 192.168.0.0
```

You can scan UDP ports
```
nmap -sU 192.168.0.0 
```

Scan using TCP connect
```
nmap -sT 192.168.0.0 
```


This is a little tutorial to study the basics of Nmap.

Thank you for reading this post.