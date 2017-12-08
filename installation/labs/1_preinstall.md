# 1_preinstall.md

# Swappiness 1:
```
root@ip-172-31-23-126 vm]# cat /proc/sys/vm/swappiness
1

[root@ip-172-31-26-157 vm]# cat /proc/sys/vm/swappiness
1

[root@ip-172-31-22-225 vm]# cat /proc/sys/vm/swappiness
1

[root@ip-172-31-21-240 vm]# cat /proc/sys/vm/swappiness
1

[root@ip-172-31-20-123 vm]# cat /proc/sys/vm/swappiness
1
```
# Huge Pages:
```
[[root@ip-172-31-23-126 vm]# echo 'never' > /sys/kernel/mm/transparent_hugepage/defrag
[root@ip-172-31-23-126 vm]# cat /sys/kernel/mm/transparent_hugepage/defrag
always madvise [never]


[root@ip-172-31-26-157 vm]# echo 'never' > /sys/kernel/mm/transparent_hugepage/defrag
[root@ip-172-31-26-157 vm]# cat /sys/kernel/mm/transparent_hugepage/defrag
always madvise [never]


[root@ip-172-31-22-225 vm]# echo 'never' > /sys/kernel/mm/transparent_hugepage/defrag
[root@ip-172-31-22-225 vm]# cat /sys/kernel/mm/transparent_hugepage/defrag
always madvise [never]

[root@ip-172-31-21-240 vm]# echo 'never' > /sys/kernel/mm/transparent_hugepage/defrag
[root@ip-172-31-21-240 vm]# cat /sys/kernel/mm/transparent_hugepage/defrag
always madvise [never]


[root@ip-172-31-20-123 vm]# echo 'never' > /sys/kernel/mm/transparent_hugepage/defrag
[root@ip-172-31-20-123 vm]# cat /sys/kernel/mm/transparent_hugepage/defrag
always madvise [never]][[root@ip-172-31-23-126Vm]#Echo'never']
```

# Interfaces:
```
[root@ip-172-31-23-126 vm]# ifconfig
eth0: flags=4163<UP,BROADCAST,RUNNING,MULTICAST>  mtu 9001
        inet 172.31.23.126  netmask 255.255.240.0  broadcast 172.31.31.255
        inet6 fe80::40e:f6ff:fe89:19ac  prefixlen 64  scopeid 0x20<link>
        ether 06:0e:f6:89:19:ac  txqueuelen 1000  (Ethernet)
        RX packets 116041  bytes 168991210 (161.1 MiB)
        RX errors 0  dropped 0  overruns 0  frame 0
        TX packets 39649  bytes 2829660 (2.6 MiB)
        TX errors 0  dropped 0 overruns 0  carrier 0  collisions 0

lo: flags=73<UP,LOOPBACK,RUNNING>  mtu 65536
        inet 127.0.0.1  netmask 255.0.0.0
        inet6 ::1  prefixlen 128  scopeid 0x10<host>
        loop  txqueuelen 1  (Local Loopback)
        RX packets 6  bytes 416 (416.0 B)
        RX errors 0  dropped 0  overruns 0  frame 0
        TX packets 6  bytes 416 (416.0 B)
        TX errors 0  dropped 0 overruns 0  carrier 0  collisions 0



[root@ip-172-31-26-157 vm]# ifconfig
eth0: flags=4163<UP,BROADCAST,RUNNING,MULTICAST>  mtu 9001
        inet 172.31.26.157  netmask 255.255.240.0  broadcast 172.31.31.255
        inet6 fe80::42e:69ff:feb8:f3a2  prefixlen 64  scopeid 0x20<link>
        ether 06:2e:69:b8:f3:a2  txqueuelen 1000  (Ethernet)
        RX packets 115204  bytes 168628237 (160.8 MiB)
        RX errors 0  dropped 0  overruns 0  frame 0
        TX packets 42732  bytes 3094957 (2.9 MiB)
        TX errors 0  dropped 0 overruns 0  carrier 0  collisions 0

lo: flags=73<UP,LOOPBACK,RUNNING>  mtu 65536
        inet 127.0.0.1  netmask 255.0.0.0
        inet6 ::1  prefixlen 128  scopeid 0x10<host>
        loop  txqueuelen 1  (Local Loopback)
        RX packets 6  bytes 416 (416.0 B)
        RX errors 0  dropped 0  overruns 0  frame 0
        TX packets 6  bytes 416 (416.0 B)
        TX errors 0  dropped 0 overruns 0  carrier 0  collisions 0





[root@ip-172-31-22-225 vm]# ifconfig
eth0: flags=4163<UP,BROADCAST,RUNNING,MULTICAST>  mtu 9001
        inet 172.31.22.225  netmask 255.255.240.0  broadcast 172.31.31.255
        inet6 fe80::416:31ff:fe0a:84e  prefixlen 64  scopeid 0x20<link>
        ether 06:16:31:0a:08:4e  txqueuelen 1000  (Ethernet)
        RX packets 114382  bytes 168347846 (160.5 MiB)
        RX errors 0  dropped 0  overruns 0  frame 0
        TX packets 46055  bytes 3272124 (3.1 MiB)
        TX errors 0  dropped 0 overruns 0  carrier 0  collisions 0

lo: flags=73<UP,LOOPBACK,RUNNING>  mtu 65536
        inet 127.0.0.1  netmask 255.0.0.0
        inet6 ::1  prefixlen 128  scopeid 0x10<host>
        loop  txqueuelen 1  (Local Loopback)
        RX packets 6  bytes 416 (416.0 B)
        RX errors 0  dropped 0  overruns 0  frame 0
        TX packets 6  bytes 416 (416.0 B)
        TX errors 0  dropped 0 overruns 0  carrier 0  collisions 0





[root@ip-172-31-21-240 vm]# ifconfig
eth0: flags=4163<UP,BROADCAST,RUNNING,MULTICAST>  mtu 9001
        inet 172.31.21.240  netmask 255.255.240.0  broadcast 172.31.31.255
        inet6 fe80::4fa:a7ff:fe04:fe9e  prefixlen 64  scopeid 0x20<link>
        ether 06:fa:a7:04:fe:9e  txqueuelen 1000  (Ethernet)
        RX packets 114494  bytes 168347108 (160.5 MiB)
        RX errors 0  dropped 0  overruns 0  frame 0
        TX packets 42555  bytes 2971896 (2.8 MiB)
        TX errors 0  dropped 0 overruns 0  carrier 0  collisions 0

lo: flags=73<UP,LOOPBACK,RUNNING>  mtu 65536
        inet 127.0.0.1  netmask 255.0.0.0
        inet6 ::1  prefixlen 128  scopeid 0x10<host>
        loop  txqueuelen 1  (Local Loopback)
        RX packets 6  bytes 416 (416.0 B)
        RX errors 0  dropped 0  overruns 0  frame 0
        TX packets 6  bytes 416 (416.0 B)
        TX errors 0  dropped 0 overruns 0  carrier 0  collisions 0




[root@ip-172-31-20-123 vm]# ifconfig
eth0: flags=4163<UP,BROADCAST,RUNNING,MULTICAST>  mtu 9001
        inet 172.31.20.123  netmask 255.255.240.0  broadcast 172.31.31.255
        inet6 fe80::4bf:4fff:fefe:62b8  prefixlen 64  scopeid 0x20<link>
        ether 06:bf:4f:fe:62:b8  txqueuelen 1000  (Ethernet)
        RX packets 114424  bytes 168431349 (160.6 MiB)
        RX errors 0  dropped 0  overruns 0  frame 0
        TX packets 31223  bytes 2194219 (2.0 MiB)
        TX errors 0  dropped 0 overruns 0  carrier 0  collisions 0

lo: flags=73<UP,LOOPBACK,RUNNING>  mtu 65536
        inet 127.0.0.1  netmask 255.0.0.0
        inet6 ::1  prefixlen 128  scopeid 0x10<host>
        loop  txqueuelen 1  (Local Loopback)
        RX packets 6  bytes 416 (416.0 B)
        RX errors 0  dropped 0  overruns 0  frame 0
        TX packets 6  bytes 416 (416.0 B)
        TX errors 0  dropped 0 overruns 0  carrier 0  collisions 0

```

# Hosts

```
[root@ip-172-31-23-126 vm]# cat /etc/hosts
127.0.0.1   localhost localhost.localdomain localhost4 localhost4.localdomain4
::1         localhost localhost.localdomain localhost6 localhost6.localdomain6

172.31.23.126   ip-172-31-23-126.us-east-2.compute.internal ip-172-31-23-126
172.31.26.157   ip-172-31-26-157.us-east-2.compute.internal ip-172-31-26-157
172.31.22.225   ip-172-31-22-225.us-east-2.compute.internal ip-172-31-22-225
172.31.21.240   ip-172-31-21-240.us-east-2.compute.internal ip-172-31-21-240
172.31.20.123   ip-172-31-20-123.us-east-2.compute.internal ip-172-31-20-123
```

# Services
```

[root@ip-172-31-23-126 vm]# systemctl status nscd
● nscd.service - Name Service Cache Daemon
   Loaded: loaded (/usr/lib/systemd/system/nscd.service; disabled; vendor preset: disabled)
   Active: active (running) since Tue 2017-12-05 13:32:31 UTC; 4s ago
  Process: 30369 ExecStart=/usr/sbin/nscd $NSCD_OPTIONS (code=exited, status=0/SUCCESS)
 Main PID: 30370 (nscd)
   CGroup: /system.slice/nscd.service
           └─30370 /usr/sbin/nscd



Dec 05 13:32:31 ip-172-31-23-126.us-east-2.compute.internal nscd[30370]: 30370 monitoring file `/etc/hosts` (4)
Dec 05 13:32:31 ip-172-31-23-126.us-east-2.compute.internal nscd[30370]: 30370 monitoring directory `/etc` (2)
Dec 05 13:32:31 ip-172-31-23-126.us-east-2.compute.internal nscd[30370]: 30370 monitoring file `/etc/resolv.conf` (5)
Dec 05 13:32:31 ip-172-31-23-126.us-east-2.compute.internal nscd[30370]: 30370 monitoring directory `/etc` (2)
Dec 05 13:32:31 ip-172-31-23-126.us-east-2.compute.internal nscd[30370]: 30370 monitoring file `/etc/services` (6)
Dec 05 13:32:31 ip-172-31-23-126.us-east-2.compute.internal nscd[30370]: 30370 monitoring directory `/etc` (2)
Dec 05 13:32:31 ip-172-31-23-126.us-east-2.compute.internal nscd[30370]: 30370 disabled inotify-based monitoring for file `/etc/netgroup...ctory
Dec 05 13:32:31 ip-172-31-23-126.us-east-2.compute.internal nscd[30370]: 30370 stat failed for file `/etc/netgroup'; will try again late...ctory
Dec 05 13:32:31 ip-172-31-23-126.us-east-2.compute.internal nscd[30370]: 30370 Access Vector Cache (AVC) started
Dec 05 13:32:31 ip-172-31-23-126.us-east-2.compute.internal systemd[1]: Started Name Service Cache Daemon.
Hint: Some lines were ellipsized, use -l to show in full.




[root@ip-172-31-23-126 vm]# systemctl status ntpd
● ntpd.service - Network Time Service
   Loaded: loaded (/usr/lib/systemd/system/ntpd.service; disabled; vendor preset: disabled)
   Active: active (running) since Tue 2017-12-05 13:35:13 UTC; 15s ago
  Process: 30406 ExecStart=/usr/sbin/ntpd -u ntp:ntp $OPTIONS (code=exited, status=0/SUCCESS)
 Main PID: 30407 (ntpd)
   CGroup: /system.slice/ntpd.service
           └─30407 /usr/sbin/ntpd -u ntp:ntp -g

Dec 05 13:35:13 ip-172-31-23-126.us-east-2.compute.internal ntpd[30407]: Listen and drop on 1 v6wildcard :: UDP 123
Dec 05 13:35:13 ip-172-31-23-126.us-east-2.compute.internal ntpd[30407]: Listen normally on 2 lo 127.0.0.1 UDP 123
Dec 05 13:35:13 ip-172-31-23-126.us-east-2.compute.internal ntpd[30407]: Listen normally on 3 eth0 172.31.23.126 UDP 123
Dec 05 13:35:13 ip-172-31-23-126.us-east-2.compute.internal ntpd[30407]: Listen normally on 4 lo ::1 UDP 123
Dec 05 13:35:13 ip-172-31-23-126.us-east-2.compute.internal ntpd[30407]: Listen normally on 5 eth0 fe80::40e:f6ff:fe89:19ac UDP 123
Dec 05 13:35:13 ip-172-31-23-126.us-east-2.compute.internal ntpd[30407]: Listening on routing socket on fd #22 for interface updates
Dec 05 13:35:13 ip-172-31-23-126.us-east-2.compute.internal ntpd[30407]: 0.0.0.0 c016 06 restart
Dec 05 13:35:13 ip-172-31-23-126.us-east-2.compute.internal ntpd[30407]: 0.0.0.0 c012 02 freq_set kernel 0.000 PPM
Dec 05 13:35:13 ip-172-31-23-126.us-east-2.compute.internal ntpd[30407]: 0.0.0.0 c011 01 freq_not_set
Dec 05 13:35:20 ip-172-31-23-126.us-east-2.compute.internal ntpd[30407]: 0.0.0.0 c614 04 freq_mode




[root@ip-172-31-26-157 vm]# systemctl status ntpd
● ntpd.service - Network Time Service
   Loaded: loaded (/usr/lib/systemd/system/ntpd.service; disabled; vendor preset: disabled)
   Active: active (running) since Tue 2017-12-05 13:40:33 UTC; 21s ago
  Process: 30162 ExecStart=/usr/sbin/ntpd -u ntp:ntp $OPTIONS (code=exited, status=0/SUCCESS)
 Main PID: 30163 (ntpd)
   CGroup: /system.slice/ntpd.service
           └─30163 /usr/sbin/ntpd -u ntp:ntp -g

Dec 05 13:40:33 ip-172-31-26-157.us-east-2.compute.internal ntpd[30163]: Listen normally on 2 lo 127.0.0.1 UDP 123
Dec 05 13:40:33 ip-172-31-26-157.us-east-2.compute.internal ntpd[30163]: Listen normally on 3 eth0 172.31.26.157 UDP 123
Dec 05 13:40:33 ip-172-31-26-157.us-east-2.compute.internal ntpd[30163]: Listen normally on 4 lo ::1 UDP 123
Dec 05 13:40:33 ip-172-31-26-157.us-east-2.compute.internal ntpd[30163]: Listen normally on 5 eth0 fe80::42e:69ff:feb8:f3a2 UDP 123
Dec 05 13:40:33 ip-172-31-26-157.us-east-2.compute.internal ntpd[30163]: Listening on routing socket on fd #22 for interface updates
Dec 05 13:40:33 ip-172-31-26-157.us-east-2.compute.internal systemd[1]: Started Network Time Service.
Dec 05 13:40:33 ip-172-31-26-157.us-east-2.compute.internal ntpd[30163]: 0.0.0.0 c016 06 restart
Dec 05 13:40:33 ip-172-31-26-157.us-east-2.compute.internal ntpd[30163]: 0.0.0.0 c012 02 freq_set kernel 0.000 PPM
Dec 05 13:40:33 ip-172-31-26-157.us-east-2.compute.internal ntpd[30163]: 0.0.0.0 c011 01 freq_not_set
Dec 05 13:40:40 ip-172-31-26-157.us-east-2.compute.internal ntpd[30163]: 0.0.0.0 c614 04 freq_mode




[root@ip-172-31-22-225 vm]# systemctl start ntpd
[root@ip-172-31-22-225 vm]# systemctl status ntpd
● ntpd.service - Network Time Service
   Loaded: loaded (/usr/lib/systemd/system/ntpd.service; disabled; vendor preset: disabled)
   Active: active (running) since Tue 2017-12-05 13:40:38 UTC; 21s ago
  Process: 30186 ExecStart=/usr/sbin/ntpd -u ntp:ntp $OPTIONS (code=exited, status=0/SUCCESS)
 Main PID: 30187 (ntpd)
   CGroup: /system.slice/ntpd.service
           └─30187 /usr/sbin/ntpd -u ntp:ntp -g

Dec 05 13:40:38 ip-172-31-22-225.us-east-2.compute.internal ntpd[30187]: Listen normally on 2 lo 127.0.0.1 UDP 123
Dec 05 13:40:38 ip-172-31-22-225.us-east-2.compute.internal ntpd[30187]: Listen normally on 3 eth0 172.31.22.225 UDP 123
Dec 05 13:40:38 ip-172-31-22-225.us-east-2.compute.internal ntpd[30187]: Listen normally on 4 lo ::1 UDP 123
Dec 05 13:40:38 ip-172-31-22-225.us-east-2.compute.internal ntpd[30187]: Listen normally on 5 eth0 fe80::416:31ff:fe0a:84e UDP 123
Dec 05 13:40:38 ip-172-31-22-225.us-east-2.compute.internal ntpd[30187]: Listening on routing socket on fd #22 for interface updates
Dec 05 13:40:38 ip-172-31-22-225.us-east-2.compute.internal systemd[1]: Started Network Time Service.
Dec 05 13:40:39 ip-172-31-22-225.us-east-2.compute.internal ntpd[30187]: 0.0.0.0 c016 06 restart
Dec 05 13:40:39 ip-172-31-22-225.us-east-2.compute.internal ntpd[30187]: 0.0.0.0 c012 02 freq_set kernel 0.000 PPM
Dec 05 13:40:39 ip-172-31-22-225.us-east-2.compute.internal ntpd[30187]: 0.0.0.0 c011 01 freq_not_set
Dec 05 13:40:45 ip-172-31-22-225.us-east-2.compute.internal ntpd[30187]: 0.0.0.0 c614 04 freq_mode
[root@ip-172-31-22-225 vm]#






[root@ip-172-31-21-240 vm]# systemctl start ntpd
[root@ip-172-31-21-240 vm]# systemctl status ntpd
● ntpd.service - Network Time Service
   Loaded: loaded (/usr/lib/systemd/system/ntpd.service; disabled; vendor preset: disabled)
   Active: active (running) since Tue 2017-12-05 13:40:43 UTC; 22s ago
  Process: 30172 ExecStart=/usr/sbin/ntpd -u ntp:ntp $OPTIONS (code=exited, status=0/SUCCESS)
 Main PID: 30173 (ntpd)
   CGroup: /system.slice/ntpd.service
           └─30173 /usr/sbin/ntpd -u ntp:ntp -g

Dec 05 13:40:43 ip-172-31-21-240.us-east-2.compute.internal ntpd[30173]: Listen normally on 2 lo 127.0.0.1 UDP 123
Dec 05 13:40:43 ip-172-31-21-240.us-east-2.compute.internal ntpd[30173]: Listen normally on 3 eth0 172.31.21.240 UDP 123
Dec 05 13:40:43 ip-172-31-21-240.us-east-2.compute.internal ntpd[30173]: Listen normally on 4 lo ::1 UDP 123
Dec 05 13:40:43 ip-172-31-21-240.us-east-2.compute.internal ntpd[30173]: Listen normally on 5 eth0 fe80::4fa:a7ff:fe04:fe9e UDP 123
Dec 05 13:40:43 ip-172-31-21-240.us-east-2.compute.internal ntpd[30173]: Listening on routing socket on fd #22 for interface updates
Dec 05 13:40:43 ip-172-31-21-240.us-east-2.compute.internal systemd[1]: Started Network Time Service.
Dec 05 13:40:43 ip-172-31-21-240.us-east-2.compute.internal ntpd[30173]: 0.0.0.0 c016 06 restart
Dec 05 13:40:43 ip-172-31-21-240.us-east-2.compute.internal ntpd[30173]: 0.0.0.0 c012 02 freq_set kernel 0.000 PPM
Dec 05 13:40:43 ip-172-31-21-240.us-east-2.compute.internal ntpd[30173]: 0.0.0.0 c011 01 freq_not_set
Dec 05 13:40:50 ip-172-31-21-240.us-east-2.compute.internal ntpd[30173]: 0.0.0.0 c614 04 freq_mode





[root@ip-172-31-20-123 vm]# systemctl start ntpd
[root@ip-172-31-20-123 vm]# systemctl status ntpd
● ntpd.service - Network Time Service
   Loaded: loaded (/usr/lib/systemd/system/ntpd.service; disabled; vendor preset: disabled)
   Active: active (running) since Tue 2017-12-05 13:40:47 UTC; 23s ago
  Process: 30161 ExecStart=/usr/sbin/ntpd -u ntp:ntp $OPTIONS (code=exited, status=0/SUCCESS)
 Main PID: 30162 (ntpd)
   CGroup: /system.slice/ntpd.service
           └─30162 /usr/sbin/ntpd -u ntp:ntp -g

Dec 05 13:40:47 ip-172-31-20-123.us-east-2.compute.internal ntpd[30162]: Listen normally on 2 lo 127.0.0.1 UDP 123
Dec 05 13:40:47 ip-172-31-20-123.us-east-2.compute.internal ntpd[30162]: Listen normally on 3 eth0 172.31.20.123 UDP 123
Dec 05 13:40:47 ip-172-31-20-123.us-east-2.compute.internal ntpd[30162]: Listen normally on 4 lo ::1 UDP 123
Dec 05 13:40:47 ip-172-31-20-123.us-east-2.compute.internal ntpd[30162]: Listen normally on 5 eth0 fe80::4bf:4fff:fefe:62b8 UDP 123
Dec 05 13:40:47 ip-172-31-20-123.us-east-2.compute.internal ntpd[30162]: Listening on routing socket on fd #22 for interface updates
Dec 05 13:40:47 ip-172-31-20-123.us-east-2.compute.internal ntpd[30162]: 0.0.0.0 c016 06 restart
Dec 05 13:40:47 ip-172-31-20-123.us-east-2.compute.internal ntpd[30162]: 0.0.0.0 c012 02 freq_set kernel 0.000 PPM
Dec 05 13:40:47 ip-172-31-20-123.us-east-2.compute.internal ntpd[30162]: 0.0.0.0 c011 01 freq_not_set
Dec 05 13:40:47 ip-172-31-20-123.us-east-2.compute.internal systemd[1]: Started Network Time Service.
Dec 05 13:40:55 ip-172-31-20-123.us-east-2.compute.internal ntpd[30162]: 0.0.0.0 c614 04 freq_mode






[root@ip-172-31-26-157 vm]# systemctl start nscd
[root@ip-172-31-26-157 vm]# systemctl status nscd
● nscd.service - Name Service Cache Daemon
   Loaded: loaded (/usr/lib/systemd/system/nscd.service; disabled; vendor preset: disabled)
   Active: active (running) since Tue 2017-12-05 13:42:10 UTC; 22s ago
  Process: 30172 ExecStart=/usr/sbin/nscd $NSCD_OPTIONS (code=exited, status=0/SUCCESS)
 Main PID: 30173 (nscd)
   CGroup: /system.slice/nscd.service
           └─30173 /usr/sbin/nscd

Dec 05 13:42:10 ip-172-31-26-157.us-east-2.compute.internal nscd[30173]: 30173 monitoring directory `/etc` (2)
Dec 05 13:42:10 ip-172-31-26-157.us-east-2.compute.internal nscd[30173]: 30173 monitoring file `/etc/resolv.conf` (5)
Dec 05 13:42:10 ip-172-31-26-157.us-east-2.compute.internal nscd[30173]: 30173 monitoring directory `/etc` (2)
Dec 05 13:42:10 ip-172-31-26-157.us-east-2.compute.internal nscd[30173]: 30173 monitoring file `/etc/services` (6)
Dec 05 13:42:10 ip-172-31-26-157.us-east-2.compute.internal nscd[30173]: 30173 monitoring directory `/etc` (2)
Dec 05 13:42:10 ip-172-31-26-157.us-east-2.compute.internal nscd[30173]: 30173 disabled inotify-based monitoring for file `/etc/netgroup...ctory
Dec 05 13:42:10 ip-172-31-26-157.us-east-2.compute.internal nscd[30173]: 30173 stat failed for file `/etc/netgroup'; will try again late...ctory
Dec 05 13:42:10 ip-172-31-26-157.us-east-2.compute.internal nscd[30173]: 30173 Access Vector Cache (AVC) started
Dec 05 13:42:10 ip-172-31-26-157.us-east-2.compute.internal systemd[1]: Started Name Service Cache Daemon.
Dec 05 13:42:29 ip-172-31-26-157.us-east-2.compute.internal nscd[30173]: 30173 checking for monitored file `/etc/netgroup': No such file...ctory
Hint: Some lines were ellipsized, use -l to show in full.
[root@ip-172-31-26-157 vm]#




[root@ip-172-31-22-225 vm]# systemctl status nscd
● nscd.service - Name Service Cache Daemon
   Loaded: loaded (/usr/lib/systemd/system/nscd.service; disabled; vendor preset: disabled)
   Active: active (running) since Tue 2017-12-05 13:42:19 UTC; 44s ago
  Process: 30195 ExecStart=/usr/sbin/nscd $NSCD_OPTIONS (code=exited, status=0/SUCCESS)
 Main PID: 30196 (nscd)
   CGroup: /system.slice/nscd.service
           └─30196 /usr/sbin/nscd

Dec 05 13:42:19 ip-172-31-22-225.us-east-2.compute.internal nscd[30196]: 30196 monitoring directory `/etc` (2)
Dec 05 13:42:19 ip-172-31-22-225.us-east-2.compute.internal nscd[30196]: 30196 monitoring file `/etc/resolv.conf` (5)
Dec 05 13:42:19 ip-172-31-22-225.us-east-2.compute.internal nscd[30196]: 30196 monitoring directory `/etc` (2)
Dec 05 13:42:19 ip-172-31-22-225.us-east-2.compute.internal nscd[30196]: 30196 monitoring file `/etc/services` (6)
Dec 05 13:42:19 ip-172-31-22-225.us-east-2.compute.internal nscd[30196]: 30196 monitoring directory `/etc` (2)
Dec 05 13:42:19 ip-172-31-22-225.us-east-2.compute.internal nscd[30196]: 30196 disabled inotify-based monitoring for file `/etc/netgroup...ctory
Dec 05 13:42:19 ip-172-31-22-225.us-east-2.compute.internal nscd[30196]: 30196 stat failed for file `/etc/netgroup'; will try again late...ctory
Dec 05 13:42:19 ip-172-31-22-225.us-east-2.compute.internal nscd[30196]: 30196 Access Vector Cache (AVC) started
Dec 05 13:42:19 ip-172-31-22-225.us-east-2.compute.internal systemd[1]: Started Name Service Cache Daemon.
Dec 05 13:42:38 ip-172-31-22-225.us-east-2.compute.internal nscd[30196]: 30196 checking for monitored file `/etc/netgroup': No such file...ctory
Hint: Some lines were ellipsized, use -l to show in full.



[root@ip-172-31-21-240 vm]# systemctl status nscd
● nscd.service - Name Service Cache Daemon
   Loaded: loaded (/usr/lib/systemd/system/nscd.service; disabled; vendor preset: disabled)
   Active: active (running) since Tue 2017-12-05 13:42:23 UTC; 1min 12s ago
  Process: 30181 ExecStart=/usr/sbin/nscd $NSCD_OPTIONS (code=exited, status=0/SUCCESS)
 Main PID: 30182 (nscd)
   CGroup: /system.slice/nscd.service
           └─30182 /usr/sbin/nscd

Dec 05 13:42:23 ip-172-31-21-240.us-east-2.compute.internal nscd[30182]: 30182 monitoring directory `/etc` (2)
Dec 05 13:42:23 ip-172-31-21-240.us-east-2.compute.internal nscd[30182]: 30182 monitoring file `/etc/resolv.conf` (5)
Dec 05 13:42:23 ip-172-31-21-240.us-east-2.compute.internal nscd[30182]: 30182 monitoring directory `/etc` (2)
Dec 05 13:42:23 ip-172-31-21-240.us-east-2.compute.internal nscd[30182]: 30182 monitoring file `/etc/services` (6)
Dec 05 13:42:23 ip-172-31-21-240.us-east-2.compute.internal nscd[30182]: 30182 monitoring directory `/etc` (2)
Dec 05 13:42:23 ip-172-31-21-240.us-east-2.compute.internal nscd[30182]: 30182 disabled inotify-based monitoring for file `/etc/netgroup...ctory
Dec 05 13:42:23 ip-172-31-21-240.us-east-2.compute.internal nscd[30182]: 30182 stat failed for file `/etc/netgroup'; will try again late...ctory
Dec 05 13:42:23 ip-172-31-21-240.us-east-2.compute.internal nscd[30182]: 30182 Access Vector Cache (AVC) started
Dec 05 13:42:23 ip-172-31-21-240.us-east-2.compute.internal systemd[1]: Started Name Service Cache Daemon.
Dec 05 13:42:42 ip-172-31-21-240.us-east-2.compute.internal nscd[30182]: 30182 checking for monitored file `/etc/netgroup': No such file...ctory
Hint: Some lines were ellipsized, use -l to show in full.




][root@ip-172-31-20-123 vm]# systemctl status nscd
● nscd.service - Name Service Cache Daemon
   Loaded: loaded (/usr/lib/systemd/system/nscd.service; disabled; vendor preset: disabled)
   Active: active (running) since Tue 2017-12-05 13:42:26 UTC; 1min 25s ago
  Process: 30193 ExecStart=/usr/sbin/nscd $NSCD_OPTIONS (code=exited, status=0/SUCCESS)
 Main PID: 30194 (nscd)
   CGroup: /system.slice/nscd.service
           └─30194 /usr/sbin/nscd

Dec 05 13:42:26 ip-172-31-20-123.us-east-2.compute.internal nscd[30194]: 30194 monitoring directory `/etc` (2)
Dec 05 13:42:26 ip-172-31-20-123.us-east-2.compute.internal nscd[30194]: 30194 monitoring file `/etc/resolv.conf` (5)
Dec 05 13:42:26 ip-172-31-20-123.us-east-2.compute.internal nscd[30194]: 30194 monitoring directory `/etc` (2)
Dec 05 13:42:26 ip-172-31-20-123.us-east-2.compute.internal nscd[30194]: 30194 monitoring file `/etc/services` (6)
Dec 05 13:42:26 ip-172-31-20-123.us-east-2.compute.internal nscd[30194]: 30194 monitoring directory `/etc` (2)
Dec 05 13:42:26 ip-172-31-20-123.us-east-2.compute.internal nscd[30194]: 30194 disabled inotify-based monitoring for file `/etc/netgroup...ctory
Dec 05 13:42:26 ip-172-31-20-123.us-east-2.compute.internal nscd[30194]: 30194 stat failed for file `/etc/netgroup'; will try again late...ctory
Dec 05 13:42:26 ip-172-31-20-123.us-east-2.compute.internal nscd[30194]: 30194 Access Vector Cache (AVC) started
Dec 05 13:42:26 ip-172-31-20-123.us-east-2.compute.internal systemd[1]: Started Name Service Cache Daemon.
Dec 05 13:42:45 ip-172-31-20-123.us-east-2.compute.internal nscd[30194]: 30194 checking for monitored file `/etc/netgroup': No such file...ctory
Hint: Some lines were ellipsized, use -l to show in full.

```
[[root@ip-172-31-23-126Vm]#Echo'never']: 
