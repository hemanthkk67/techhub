## websites to start recon

1)shodan.io
 
 SHODAN is designed to help the user find specific nodes (desktops, servers, routers, switches, etc.) with specific content

##### I have login and found api key and  used shodan for finding information about uber.com using google dorks 
eg. apache hostname:.uber.com
       apache 2.2.1

   2)censys.io
 i have used censys.io to found the protocols and ipv4 hosts ,website backend servers information for indeed.com 

3)crt.sh
used crt.sh for indeed.com to find the regestered domains certifications validation information ,issuer names, etc

4)archive.org
i found the 2010 year snapshots for the flickr.com and website view, its behaviour using waybackmachine 

5)mxtoolbox.com
https://www.stationx.net/nmap-cheat-sheet/
founded ip address, hostname using mxtoolbox also information observered like spf, dmarc records,whois etc.


6)kitterman
  checked spf records where exist for flickr.com 

7)greynoise.io

GreyNoise is a system that collects and analyzes data on Internet-wide scanners. GreyNoise collects data on benign scanners such as Shodan.io, as well as malicious actors like SSH and telnet worms.

The data is collected by a network of sensors deployed around the Internet in various datacenters, cloud providershttps://www.stationx.net/nmap-cheat-sheet/, and regions.


8)hunter.io

I observed this is an email finder and email verifier tool which allows to perform domain search for email addresses.

9)recon.dev

10)spiderfoot.net(OSINT)

## Tools

1) ### dig

used dig tool to finding dns record types, dns paths,nameservers ..etc

dig flickr.com.com txt (Query TXT record)

dig flickr.com cname (Query CNAME record)

dig flickr.com ns (Query NS record)

dig flickr.com A (Query A record)

2)nmap
  
  finded target open ports, os detection, vuln script cve  details 
  
  followed from below nmap cheatsheet concepts
  
  https://www.stationx.net/nmap-cheat-sheet/

3) ### amass

#finding with org name 
 
 ~amass intel -org uber
 
 #to get an ip for domain
 
 ~ amass enum -src -ip -d uber.com  
 
 #with cidr finding new domains 
 
 ~amass intel -ip -cidr 104.154.0.0/15

#finding dns names using asn number 

~amass intel -asn 63086

#for looking subdomains 

~amass enum -d -ip -src uber.com

#It uses a bunch of OSINT sources as well as active brute-forcing and clever permutations to quickly identify hundreds,of subdomains on a domain
 
 ~amass -active -brute -o hosts.txt -d uber.com

4) ### aquatone
   
   finding the subdomains scanning, information,takeover possiblities for flickr.com
   
   ~aquatone-discover --domain indeed.com
  
  ~aquatone-takeover --domain indeed.com
   
   ~aquatone-scan --domain indeed.com --ports 80,443,
   

5) ### sublist3r

finding subdomains 

~python sublist3r.py -h

~python sublist3r.py -d indeed.com

    To enumerate subdomains of specific domain and show only subdomains which have open ports 80 and 443 :

~python sublist3r.py -d indeed.com -p 80,443

    To enumerate subdomains of specific domain and show the results in realtime:

~python sublist3r.py -v -d indeed.com

    To enumerate subdomains and enable the bruteforce module:

~python sublist3r.py -b -d indeed.com

    To enumerate subdomains and use specific engines such Google, Yahoo and Virustotal engines

~python sublist3r.py -e google,yahoo,virustotal -d indeed.com


6)gobuster(dir bruteforce)

used to find the possible hidden directories for bruteforcing

~gobuster -h

~gobuster -e -u https://www.uber.com/ -w /usr/share/wordlists/dirb/common.txt
~.

