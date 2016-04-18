1. Write a command that issues a statement to the system log with the current uptime information.
Schedule this command to run one minute from now.

[root@localhost]# at now +1 minute

at> logger "The system current uptime is $(uptime)"

2. Wait one minute and check the system log to view the entry. 

[roo@localhost]# journalctl -f

3. Create a new at job that runs at teatime but performs the same log entry as step 1.

[root@localhost]# at teatime

at> logger "The system current uptime is $(uptime)"

4. Turn the uptime script from step one into an executable script file located in /home/user/ called uptimelog.

[root@localhost]# vim /home/user/uptimelog

logger "The system current uptime is $(uptime)"

[root@localhost]# chmod +x /home/user/uptimelog

5. Schedule an anacronjob so that the script runs every 5 days if it has not currently been run; make sure
the job name is uptimelog.

Note: place the entry at the top of the other entries so it is run first.

[root@localhost]# vim /etc/anacrontab

5       0       uptimelog       /home/user/uptimelog

6. Run all anacronjobs regardless of their last run timestamp.

[root@localhost] anacron -f

7. View the anacron timestamps for your uptimelog job.

[root@localhost]# cat /var/spool/anacron/uptimelog

8. Using the same /home/user/uptimelog script, schedule the script to run once a day using cron.

[root@localhost]# cp /home/user/uptimelog /etc/cron.daily/

9. Create a custom scheduled cron that runs the uptimelog every 5 minutes. 

[root@localhost]# vim /etc/cron.d/uptimelog

*/5 * * * * root /home/user/uptimelog
