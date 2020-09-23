# kali CLI commands 
## root directory path:

hspace@kali:~$ cat /etc/passwd | head

root:x:0:0:root:/root:/bin/bash
daemon:x:1:1:daemon:/usr/sbin:/usr/sbin/nologin
bin:x:2:2:bin:/bin:/usr/sbin/nologin
sys:x:3:3:sys:/dev:/usr/sbin/nologin
sync:x:4:65534:sync:/bin:/bin/sync
games:x:5:60:games:/usr/games:/usr/sbin/nologin
man:x:6:12:man:/var/cache/man:/usr/sbin/nologin
lp:x:7:7:lp:/var/spool/lpd:/usr/sbin/nologin
mail:x:8:8:mail:/var/mail:/usr/sbin/nologin
news:x:9:9:news:/var/spool/news:/usr/sbin/nologin

## checking with id:
**** 
hspace@kali:~$ id

uid=1000(hspace) gid=1000(hspace) groups=1000(hspace),24(cdrom),25(floppy),27(sudo),29(audio),30(dip),44(video),46(plugdev),109(netdev),117(bluetooth),131(scanner)
***

## hspace@kali:~$ cat /etc/passwd 

root:x:0:0:root:/root:/bin/bash
daemon:x:1:1:daemon:/usr/sbin:/usr/sbin/nologin
bin:x:2:2:bin:/bin:/usr/sbin/nologin
sys:x:3:3:sys:/dev:/usr/sbin/nologin
sync:x:4:65534:sync:/bin:/bin/sync
games:x:5:60:games:/usr/games:/usr/sbin/nologin
man:x:6:12:man:/var/cache/man:/usr/sbin/nologin
lp:x:7:7:lp:/var/spool/lpd:/usr/sbin/nologin
mail:x:8:8:mail:/var/mail:/usr/sbin/nologin
news:x:9:9:news:/var/spool/news:/usr/sbin/nologin
uucp:x:10:10:uucp:/var/spool/uucp:/usr/sbin/nologin
proxy:x:13:13:proxy:/bin:/usr/sbin/nologin
www-data:x:33:33:www-data:/var/www:/usr/sbin/nologin
backup:x:34:34:backup:/var/backups:/usr/sbin/nologin
list:x:38:38:Mailing List Manager:/var/list:/usr/sbin/nologin
irc:x:39:39:ircd:/var/run/ircd:/usr/sbin/nologin
gnats:x:41:41:Gnats Bug-Reporting System (admin):/var/lib/gnats:/usr/sbin/nologin
nobody:x:65534:65534:nobody:/nonexistent:/usr/sbin/nologin
_apt:x:100:65534::/nonexistent:/usr/sbin/nologin
systemd-timesync:x:101:101:systemd Time Synchronization,,,:/run/systemd:/usr/sbin/nologin
systemd-network:x:102:103:systemd Network Management,,,:/run/systemd:/usr/sbin/nologin
systemd-resolve:x:103:104:systemd Resolver,,,:/run/systemd:/usr/sbin/nologin
mysql:x:104:110:MySQL Server,,,:/nonexistent:/bin/false
tss:x:105:111:TPM software stack,,,:/var/lib/tpm:/bin/false
strongswan:x:106:65534::/var/lib/strongswan:/usr/sbin/nologin
ntp:x:107:112::/nonexistent:/usr/sbin/nologin
messagebus:x:108:113::/nonexistent:/usr/sbin/nologin                                                                                                                  
redsocks:x:109:114::/var/run/redsocks:/usr/sbin/nologin
rwhod:x:110:65534::/var/spool/rwho:/usr/sbin/nologin
iodine:x:111:65534::/var/run/iodine:/usr/sbin/nologin
miredo:x:112:65534::/var/run/miredo:/usr/sbin/nologin
usbmux:x:113:46:usbmux daemon,,,:/var/lib/usbmux:/usr/sbin/nologin
tcpdump:x:114:119::/nonexistent:/usr/sbin/nologin
rtkit:x:115:120:RealtimeKit,,,:/proc:/usr/sbin/nologin
_rpc:x:116:65534::/run/rpcbind:/usr/sbin/nologin
Debian-snmp:x:117:122::/var/lib/snmp:/bin/false
statd:x:118:65534::/var/lib/nfs:/usr/sbin/nologin
postgres:x:119:124:PostgreSQL administrator,,,:/var/lib/postgresql:/bin/bash
stunnel4:x:120:126::/var/run/stunnel4:/usr/sbin/nologin
sshd:x:121:65534::/run/sshd:/usr/sbin/nologin
sslh:x:122:127::/nonexistent:/usr/sbin/nologin
avahi:x:123:128:Avahi mDNS daemon,,,:/var/run/avahi-daemon:/usr/sbin/nologin
nm-openvpn:x:124:129:NetworkManager OpenVPN,,,:/var/lib/openvpn/chroot:/usr/sbin/nologin
nm-openconnect:x:125:130:NetworkManager OpenConnect plugin,,,:/var/lib/NetworkManager:/usr/sbin/nologin
pulse:x:126:132:PulseAudio daemon,,,:/var/run/pulse:/usr/sbin/nologin
saned:x:127:134::/var/lib/saned:/usr/sbin/nologin
inetsim:x:128:136::/var/lib/inetsim:/usr/sbin/nologin
colord:x:129:137:colord colour management daemon,,,:/var/lib/colord:/usr/sbin/nologin
geoclue:x:130:138::/var/lib/geoclue:/usr/sbin/nologingit commands visual code
lightdm:x:131:139:Light Display Manager:/var/lib/lightdm:/bin/false
king-phisher:x:132:140::/var/lib/king-phisher:/usr/sbin/nologin
hspace:x:1000:1000:hspace,,,:/home/hspace:/bin/bash
systemd-coredump:x:999:999:systemd Core Dumper:/:/usr/sbin/nologin
tomcat8:x:133:141::/var/lib/tomcat8:/bin/false
uuidd:x:134:142::/run/uuidd:/usr/sbin/nologin

***

## hspace@kali:~$  cat /etc/passwd | tail

saned:x:127:134::/var/lib/saned:/usr/sbin/nologin
inetsim:x:128:136::/var/lib/inetsim:/usr/sbin/nologin
colord:x:129:137:colord colour management daemon,,,:/var/lib/colord:/usr/sbin/nologin
geoclue:x:130:138::/var/lib/geoclue:/usr/sbin/nologin
lightdm:x:131:139:Light Display Manager:/var/lib/lightdm:/bin/false
king-phisher:x:132:140::/var/lib/king-phisher:/usr/sbin/nologin
hspace:x:1000:1000:hspace,,,:/home/hspace:/bin/bash
systemd-coredump:x:999:999:systemd Core Dumper:/:/usr/sbin/nologin
tomcat8:x:133:141::/var/lib/tomcat8:/bin/false
uuidd:x:134:142::/run/uuidd:/usr/sbin/nologin
***
### hspace@kali:~$ sudo cat /etc/shadow | grep root

root:$6$Cug5CfpKh4tdIbCi$F5hgmISlY81ePpAkaTsXwSqAy6Yr/AfjoCBPlGR/LbD.h2R3W1fZAuBtsObmrVFJ6fbw/y4iTHq.QZqs.Wb.L.:18439:0:99999:7:::

Checking ifconfig:

### hspace@kali:~$ ifconfig

bash: ifconfig: command not found
hspace@kali:~$ /usr/bin/ifconfig
bash: /usr/bin/ifconfig: No such file or directory
hspace@kali:~$ echo $PATH
/usr/local/bin:/usr/bin:/bin:/usr/local/games:/usr/games
***

### hspace@kali:~$ export PATH=$PATH:/usr/sbin

hspace@kali:~$ ifconfig
eth0: flags=4099<UP,BROADCAST,MULTICAST>  mtu 1500
        ether b4:b5:2f:c6:68:60  txqueuelen 1000  (Ethernet)
        RX packets 0  bytes 0 (0.0 B)
        RX errors 0  dropped 0  overruns 0  frame 0
        TX packets 0  bytes 0 (0.0 B)
        TX errors 0  dropped 0 overruns 0  carrier 0  collisions 0
        device interrupt 20  memory 0xf7c00000-f7c20000  

lo: flags=73<UP,LOOPBACK,RUNNING>  mtu 65536
        inet 127.0.0.1  netmask 255.0.0.0
        inet6 ::1  prefixlen 128  scopeid 0x10<host>
        loop  txqueuelen 1000  (Local Loopback)
        RX packets 4506  bytes 895047 (874.0 KiB)
        RX errors 0  dropped 0  overruns 0  frame 0
        TX packets 4506  bytes 895047 (874.0 KiB)
        TX errors 0  dropped 0 overruns 0  carrier 0  collisions 0

wlan0: flags=4163<UP,BROADCAST,RUNNING,MULTICAST>  mtu 1500
        inet 192.168.43.138  netmask 255.255.255.0  broadcast 192.168.43.255
        inet6 fe80::3ca4:f1d6:bdbe:a8c9  prefixlen 64  scopeid 0x20<link>
        inet6 2409:4070:2516:2cae:978c:3b84:76ec:a3e5  prefixlen 64  scopeid 0x0<global>
        ether 20:e0:17:0d:d2:f8  txqueuelen 1000  (Ethernet)
        RX packets 27671  bytes 3540775 (3.3 MiB)
        RX errors 0  dropped 0  overruns 0  frame 0
        TX packets 28531  bytes 4727130 (4.5 MiB)
        TX errors 0  dropped 0 overruns 0  carrier 0  collisions 0

