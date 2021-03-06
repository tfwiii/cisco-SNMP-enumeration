Cisc0wn - Cisco SNMP Script
============================================

Cisco SNMP enumeration, brute force, config downloader and password cracking script.

Released as open source by NCC Group Plc - http://www.nccgroup.com/

Developed by Daniel Compton, daniel dot compton at nccgroup dot com

Fixed and updated by Tom Watson, tom dot watson at nccgroup dot com

https://github.com/nccgroup/cisco-SNMP-enumeration

Released under AGPL see LICENSE for more information

Installing  
=======================
    git clone https://github.com/nccgroup/cisco-SNMP-enumeration.git


How To Use	
=======================
    ./cisc0wn.sh


Features	
=======================

* Checks SNMP is enabled on the route
* Brute forces the SNMP Read Only and Read Write community strings (can edit which wordlist it uses in script header)
* Enumerates information such as IOS version,  hostname, Arp table, Routing table, interface list and IP addresses using the RO or RW community string.
* If RW community was found it will then download the router config automatically.
* It then searches and displays any enable or telnet passwords in clear text.
* If it finds Cisco type 7 encoded enable or telnet passwords it will auto decode them.
* It will display the Enable secret type 5 password and attempt to crack the MD5. It uses John first with its built in wordlist for speed. If this fails it will try and full crack.

Requirements   
=======================
* Metasploit http://www.metasploit.com

Tested on Backtrack 5 and Kali.


Screen Shot    
=======================
<img src="http://www.commonexploits.com/wp-content/uploads/2012/06/3.png" alt="Screenshot" style="max-width:100%;">

<img src="http://www.commonexploits.com/wp-content/uploads/2012/06/121.png" alt="Screenshot" style="max-width:100%;">

Change Log
=======================

Version 1.6 - Updated to reflect changes in metasploit filesystem use, made grep case insensitive to avoid false negatives, added new location for community string file & moved from the deprecated msfcli to msfconsole -x syntax
Version 1.5 - Official release.
