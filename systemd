1. Install the httpd package.

[root@localhost]# yum install httpd

2. View all active targets on the system.

[root@localhost]# systemctl list-units --type=target

3. View all targets installed on the disk.

[root@localhost]# systemctl list-units --type=target --all

4. Display the current default target.

[root@localhost]# systemctl get-default

5. Change the default target to the multi-user target if the multi-user target is available.

[root@localhost]#  systemctl list-units --type=target | grep multi-user.target
multi-user.target   loaded active active Multi-User System
root@localhost]# systemctl set-default multi-user.target

6. View all available systemd configuration units.

[root@localhost]# systemctl -t help

7. Find the status of the sshd service.

[root@localhost]# systemctl status sshd.service

8. List all active service unit configuration files.

[root@localhost]# systemctl --type=service
or
[root@localhost]# systemctl list-units --type=service

9. Determine if the httpd service is active.

[root@localhost]# systemctl is-active httpd

10. Determine if the httpd service is enabled and, if it is not enabled, enable it

[root@localhost]# syhstemctl is-enabled httpd

11. View enabled and disabled settings for all units of the type "service".

[root@localhost]# systemctl --type=service --all
or
[root@localhost]# systemctl list-units --type=service -all

12. List all service unit configuration files regardless of whether they are active or not.

[root@localhost]# systemctl list-units --all
