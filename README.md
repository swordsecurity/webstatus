# Webstatus: Retrieve DNS records, open ports and ssl / whois expiry information from a domain. 

## Features
- Easy script to retrieve status information about a domain
- DNS records
- Port statuses (1=open,0=filtered/closed)
- SSL expiry information
- Whois expiry information

## Prerequisites
To run Webstatus, you'll need the following:
- git
- dnsutils
- nmap

## Install 
Install dependencies via apt.
```
sudo apt-get install git dnsutils nmap
git clone [this repository]
```

##  Usage
```
usage: ./webstatus [domain]
```

##  Example
```
$ ./webstatus github.com
========== DIG Records ============
A    192.30.253.112 
A    192.30.253.113 
MX    10 alt3.aspmx.l.google.com.
MX    10 ALT3.ASPMX.L.GOOGLE.com.
MX    10 alt4.aspmx.l.google.com.
MX    10 ALT4.ASPMX.L.GOOGLE.com.
MX    1 aspmx.l.google.com.
MX    1 ASPMX.L.GOOGLE.com.
MX    5 alt1.aspmx.l.google.com.
MX    5 ALT1.ASPMX.L.GOOGLE.com.
MX    5 alt2.aspmx.l.google.com.
MX    5 ALT2.ASPMX.L.GOOGLE.com.
NS    ns-1283.awsdns-32.org. 
NS    ns-1707.awsdns-21.co.uk. 
NS    ns1.p16.dynect.net. 
NS    ns2.p16.dynect.net. 
NS    ns3.p16.dynect.net. 
NS    ns-421.awsdns-52.com. 
NS    ns4.p16.dynect.net. 
NS    ns-520.awsdns-01.net. 
SOA    ns-1707.awsdns-21.co.uk. awsdns-hostmaster.amazon.com.
TXT    "docusign=087098e3-3d46-47b7-9b4e-8a23028154cd" 
TXT    "v=spf1 ip4:192.30.252.0/22
========== PORT SCAN (22,80,443) ============
22     1
80     0
443     1
========== WHOIS expiry ============
2020-10-09
979
========== SSL Expiry ============
May 17 2018
103
```

# License
GNU AFFERO GENERAL PUBLIC LICENSE
