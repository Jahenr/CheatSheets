## How to Use Nmap
Nmap can be used in a variety of ways depending on the user's level of technical expertise.

| Technical Expertise | Usage |
|:--------------------|:------|
| Beginner            | [Zenmap](https://nmap.org/zenmap/) the graphical user interface for Nmap |
| Intermediate        | [Command line](https://nmap.org/) |
| Advanced            | Python scripting with the [Python-Nmap](https://pypi.org/project/python-nmap/) package |

### Command Line
```shell
nmap [ <Scan Type> ...] [ <Options> ] { <target specification> }
```
## Basic Scanning Techniques
The `-s` switch determines the type of scan to perform.
| Nmap Switch | Description                 |
|:------------|:----------------------------|
| **-sA**     | ACK scan                    |
| **-sF**     | FIN scan                    |
| **-sI**     | IDLE scan                   |
| **-sL**     | DNS scan (a.k.a. list scan) |
| **-sN**     | NULL scan                   |
| **-sO**     | Protocol scan               |
| **-sP**     | Ping scan                   |
| **-sR**     | RPC scan                    |
| **-sS**     | SYN scan                    |
| **-sT**     | TCP connect scan            |
| **-sW**     | Windows scan                |
| **-sX**     | XMAS scan                   |

# Scan a Single Target
```shell
nmap [target]
```
# Scan Multiple Targets
```shell
nmap [target1, target2, etc]
```
# Scan a List of Targets
```shell
nmap -iL [list.txt]
```
# Scan a Range of Hosts
```shell
nmap [range of IP addresses]
```
# Scan an Entire Subnet
```shell
nmap [ip address/cdir]
```
# Scan Random Hosts
```shell
nmap -iR [number]
```
# Exclude Targets From a Scan
```shell
nmap [targets] --exclude [targets]
```
# Exclude Targets Using a List
```shell
nmap [targets] --excludefile [list.txt]
```
# Perform an Aggresive Scan
```shell
nmap -A [target]
```
# Scan an IPv6 Target
```shell
nmap -6 [target]
```
# Perform a Fast Scan
```shell
nmap -F [target]
```
# Scan Specific Ports
```shell
nmap -p [port(s)] [target]
```
# Scan Ports by Name
```shell
nmap -p [port name(s)] [target]
```
# Scan Ports by Protocol
```shell
nmap -sU -sT -p U:[ports],T:[ports] [target]
```
# Scan All Ports
```shell
nmap -p 1-65535 [target]
```
# Scan Top Ports
```shell
nmap --top-ports [number] [target]
```
# Perform a Sequential Port Scan
```shell
nmap -r [target]
```
# Attempt to Guess an Unknown OS
```shell
nmap -O --osscan-guess [target]
```
# Service Version Detection
```shell
nmap -sV [target]
```
# Troubleshoot Version Scan
```shell
nmap -sV --version-trace [target]
```
# Perform a RPC Scan
```shell
nmap -sR [target]
```
