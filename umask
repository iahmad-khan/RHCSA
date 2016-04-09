1. View current umask permissions and then, for the current shell session, set umask permissions to 0.

[root@localhost ~]# umask

0022

[root@localhost ~]# umask 0

[root@localhost ~]# umask

0000

[root@localhost ~]# 

Note: umask will add leading zeros

2. Navigate into the /tmp directory and touch file1 and dir1 and view current permissions.

[root@localhost user]# cd /tmp

[root@localhost tmp]# touch file1

[root@localhost tmp]# mkdir dir1

[root@localhost tmp]# ls -l

total 0

drwxrwxrwx. 2 root root 6 May  1 11:10 dir1

-rw-rw-rw-. 1 root root 0 May  1 11:10 file1 

[root@localhost tmp]# 

3. Mask permissions for the "other" users to write a file when created, then touch file2 and view permissions.

Tip: If file permissions start at 666 and you want to "remove/mask" permissions for other users to read and write,
then you will need to subtract the octoal notation representing write permissions which is 2. 

[root@localhost tmp]# umask 002

[root@localhost tmp]# touch file2

[root@localhost tmp]# ls -l

total 0

drwxr-xr-x. 2 root root 6 May  1 11:10 dir1

-rw-rw-rw-. 1 root root 0 May  1 11:10 file1

-rw-rw-r--. 1 root root 0 May  1 11:13 file2

[root@localhost tmp]# 

Tip: umask 002 resulting in default permissions on newly created files of 664 (no execute and you "masked" write permissions).

4. Mask write access for group members and the write for "other" permissions, then touch file3 and view permissions.

[root@localhost tmp]# umask 022

[root@localhost tmp]# touch file3

[root@localhost tmp]# ls -l

-rw-r--r--. 1 root root 0 May  1 11:16 file3

[root@localhost tmp]# 

5. Mask read and write permissions for the owner of a file and leave read/write for both group 
and other permissions, then touch file4 and mkdir dir3 and view permissions.

[root@localhost tmp]# umask 600

[root@localhost tmp]# touch file4

[root@localhost tmp]# mkdir dir3

[root@localhost tmp]# ls -l

total 0

d--xrwxrwx. 2 root root 6 May  1 11:18 dir3

----rw-rw-. 1 root root 0 May  1 11:18 file4

[root@localhost tmp]# 

6. Mask all permissions including execute permissions on new directories, then touch file5.

[root@localhost tmp]# umask 777

[root@localhost tmp]# touch file5

Tip: Setting umask 666 would mask all permissions on files but leave execute on directories. 
Directories need execute permissions in order for someone to "change into the directory".

7. Mask read/write access for group for non-privileged users and other permissions and make these changes persistent.

[root@localhost ]#vim /etc/bashrc

if [ $UID -gt 199 ] && [ "`id -gn`" = "`id -un`" ]; then

    umask 066

else

    umask 022

fi

[root@localhost ]#vim /etc/profile

if [ $UID -gt 199 ] && [ "`id -gn`" = "`id -un`" ]; then

    umask 066

else

    umask 022

fi

Note: In order for users to have sudo privileges (a privileged user), they generally will have a 
primary group of "wheel". What the script says if the primary/effective group does not match the username  
(remember generally users primary/effective group will be the same as the username) then consider 
the user a privileged user.
