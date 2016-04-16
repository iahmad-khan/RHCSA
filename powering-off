1. Using the shutudown command, schedule a shutdown for five minutes from now and notify all users on the system of the shutdown.

[root@localhost]# shutdown +5 shutdown messages goes here

2. Using the shutdown command, reboot the machine immediately without delay.

[root@localhost]# shutdown -r now
[root@localhost]# shutdown -r 

3. Using systemctl, shutdown the system.

[root@localhost]# shutdown now 

or

[root@localhost]# shutdown +0 

Alternatively, not using the shutdown command.

[root@localhost]# init 0

[root@localhost]# systemctl halt

4. Schedule the system for a shutdown at 1:00am in the morning.

[root@localhost]# shutdown 01:00 

5. Cancel the scheduled 1:00am shutdown.

[root@localhost]# shutdown -c

6. Using systemctl, reboot the the system.

[root@localhost]# systemctl reboot

7. Using any method of your choice, power off the system.

[root@localhost]# systemctl halt
[root@localhost]# systemctl poweroff
[root@localhost]# shutdown -P
[root@localhost]# init 0
