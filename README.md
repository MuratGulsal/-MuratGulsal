# Tor ProxyChains Kali Linux VM project | How to be anonymous in Kali Linux 

## Objective
The Tor ProxChains Kali Linux VM project is intended to anonymise your identity. 

### Skills Learned
- Advanced understanding of ProxyChains concepts and practical application.
- How to maintain anonymity and bypass network restrictions. In Kali Linux for penetration testing distribution 
- How to conceal the identity of the user during security assessments.

### Tools Used
- Oracle Virtualbox Kali Linux Machine.

## Steps
## Install tor and make sure it is running
To install tor command: sudo apt install tor 
 
![Sudo apt install tor  ](https://github.com/MuratGulsal/-MuratGulsal/assets/88938361/97143fe0-c497-4ff7-ae35-43d3b69c6184)

To start tor service: sudo service tor start 

Check tor service status: sudo service tor status 

![Service Tor Status  ](https://github.com/MuratGulsal/-MuratGulsal/assets/88938361/f116ee58-0f36-41b6-a994-b87b77aef32c)

Ctrl + C to exit for service tor status

## Install and configure proxychains4 

To install proxychains4: sudo apt install proxychains4 

![sudo apt install proxy](https://github.com/MuratGulsal/-MuratGulsal/assets/88938361/263717f3-4c73-4676-ba78-e50a471ad0f8)

To configure proxychains4 : sudo nano /etc/proxychains4.conf
  
You will see the same file type in the terminal. "#" means bash language comments. If there is no "#" hash at the beginning of the line, it is active and running. if there is a "#" hash at the beginning of the line, it is inactive and not running.  

![nano 1 ](https://github.com/MuratGulsal/-MuratGulsal/assets/88938361/0829ba35-6cd4-4d19-ba5f-26c6e1dd778e)

There is three types of proxychains; Dynamic, Strict and Random   

We are going to use Dynamic chain, remove Dynamic chain hash  

To be sure Strict chain and Random chain has a # at the beginning of the line.

![nano 2 ](https://github.com/MuratGulsal/-MuratGulsal/assets/88938361/ec8897b3-e816-41a9-ad7d-406b7dc2f3b3)

Remove proxy_dns and Proxy DNS requests - no leak for DNS data

Tips: Removing proxy DNS and no leak for DNS data provide to you fully anonymous. 

![nano 3 ](https://github.com/MuratGulsal/-MuratGulsal/assets/88938361/6ed12042-01b2-489d-bb49-f41c4f5610ca)

Add your socks5 127.0.0.1 9050 in the last line of the proxy list 

To save your progresses: CTRL + O and enter and CTRL + X 

SOCKS is an Internet protocol that makes easy communication between a client application and a server through a proxy server

We are almost there. 

sudo service tor restart

proxychains4 firefox 

![nano 4 ](https://github.com/MuratGulsal/-MuratGulsal/assets/88938361/0778e9d6-a58f-4357-a4f2-e8dc687ca5b5)

Finally 

![nano 5 ](https://github.com/MuratGulsal/-MuratGulsal/assets/88938361/38de8a38-51f2-4e9f-ad03-174674a24d9d)

Thanks for join my journey  
See you with next project 
