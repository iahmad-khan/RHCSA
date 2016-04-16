1. View the system uptime and load average.

[root@localhost ~]# uptime
 09:53:07 up 16:32,  3 users,  load average: 1.02, 1.00, 0.69
[root@localhost ~]# 

2. View the system uptime and load average that also shows what users are logged into the system and what the user is doing.

[root@localhost ~]# w
 09:53:37 up 16:33,  3 users,  load average: 1.01, 1.00, 0.70
USER     TTY        LOGIN@   IDLE   JCPU   PCPU WHAT
user  pts/1     09:18    1.00s  0.10s  5.32s /usr/libexec/gnome-terminal-server
[root@localhost ~]# 

3. Using the proc file system and wc,display the number of processors your system has. This is important in order to calculate the load average of the system. (Please note your number of CPUs will vary depending on your system and may not match the exact lab number.)

[root@localhost]# grep "model name" /proc/cpuinfo | wc -l

4. Calculate the 1, 5, and 15 minute load averages for the system.

There are two processors as a result of our previous command.

[root@localhost ~]# grep "model name" /proc/cpuinfo | wc -l
2
[root@localhost ~]# 

For each processor 1 is 100%. If you have 1 processor and your load average is 1.2 then your load is greater than 100%. If you have 2 processors and your load is 2 then your load is 100%. Below we are going to learn how to calculate this number.

[root@localhost ~]# uptime

 09:42:20 up 16:21,  3 users,  load average: 1.04, 0.72, 0.35

Per CPU load average calculation formula: load average / # of cpu

Per CPU load average calculation 1 Minute load average: 1.04 / 2 = 52%

Per CPU load average calculation 5 Minute load average: .72 / 2 = 36%

Per CPU load average calculation 15 Minute load average: .35 / 2 = 17.5%
