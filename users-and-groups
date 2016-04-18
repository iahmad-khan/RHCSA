1. Create two new users called starbuck and apollo. For each user, assign the password "student" without quotes.

[root@localhost user]# useradd starbuck

[root@localhost user]# passwd starbuck

Changing password for user starbuck.

New password: 

Retype new password: 

passwd: all authentication tokens updated successfully.

[root@localhost user]# useradd apollo

[root@localhost user]# passwd apollo

Changing password for user apollo.

New password: 

Retype new password: 

passwd: all authentication tokens updated successfully.

[root@localhost user]# 

2. Modify starbuck's GECOS to say "pilot".

[root@localhost user]# usermod -c pilot starbuck

3. View apollo's user id and group id information.

[root@localhost user]# id apollo

uid=1003(apollo) gid=1003(apollo) groups=1003(apollo)

Note: Your gid/uid might not match that of what is displayed in this lab. You can modify that 
using the usermod command and groupmod command.

4. Create a third account as a system account named "viper".

[root@localhost user]# useradd -r viper

5. Create a new group called "Galactica" and a folder named galactica in /home/groups/.

[root@localhost user]# groupadd Galactica; mkdir -p /home/groups/galactica

6. Create a second new group called "colonial-one" and a folder named colonial-one in /home/groups/.

[root@localhost user]# groupadd colonial-one; mkdir -p /home/groups/colonial-one

7. Modify starbuck's account so her primary group is "galactica".

[root@localhost user]# usermod -g Galactica starbuck

[root@localhost user]# usermod -g Galactica starbuck

[root@localhost user]# groups starbuck

starbuck : Galactica

[root@localhost user]# id starbuck

uid=1002(starbuck) gid=1005(Galactica) groups=1005(Galactica)

[root@localhost user]# 

8. Modify viper's account so that its primary group is "viper" and it belongs to both the "galactica" 
and "colonial-one" supplementary groups.

Note: when we created the viper user, it created a group called viper and assigned it as 
the viper user's primary group.

[root@localhost user]# usermod -aG Galactica,colonial-one viper

[root@localhost user]# id viper

uid=1004(viper) gid=1004(viper) groups=1004(viper),1005(Galactica),1006(colonial-one)

[root@localhost user]# 

9. Modify directory permissions for each group directory so that the respective group name owns 
the group and has read/write/execute permissions on the directory.

[root@localhost groups]# chown :colonial-one -R colonial-one

[root@localhost groups]# chown :Galactica -R galactica

[root@localhost groups]# chmod g+rwX colonial-one/

[root@localhost groups]# chmod g+rwX galactica/

10. Apply special permission bits to the "galactica" folder so that, regardless of the user's 
primary group, any directories or files created in the "galactica" folder are owned by the "galactica" group.

[root@localhost groups]# chmod g+s galactica/

11. Change the "viper" user password and login to the system as the viper user. 
Notice viper's primary group is "viper". Navigate into the /home/groups/galactica directory 
and touch file1 then view permissions.

[viper@localhost galactica]$ touch test1

[viper@localhost galactica]$ ls -al

total 0

drwxrwsr-x. 2 root     Galactica 29 Apr 28 11:36 .

drwxr-xr-x. 4 root     root      41 Apr 28 11:12 ..

-rw-rw-r--. 1 viper    Galactica  0 Apr 28 11:36 file1

[viper@localhost galactica]$ 

You will notice that even though vipers current logged in/primary group is "viper", when the
file was created it was created with the permissions of the "parent" directory since the SGID bit was set. 

12. Modify the user apollo so that the user has authentication but cannot login to a shell terminal

[root@localhost ~]# usermod -s /sbin/nologin apollo
