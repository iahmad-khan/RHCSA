1. While working in the user root's home directory, create a tar archive of the entire /var/log directory and name the tar file logs.tar.

[root@localhost ~]# tar -cvf logs.tar /var/log

2. List the contents of the tar archive into standard output.

[root@localhost ~]# tar -tf logs.tar

3. Using gzip, compress the tar file appropriately.

[root@localhost ~]# gzip logs.tar

4. Extract the contents of the log.tar.gz directory into /root/var/log.

[root@localhost ~]# tar -zxvf logs.tar.gz

5. Using star, create an archive of the contents of the newly created log directory in /root/var/log into a
tar file called user-logs.tar. Be sure to preserve the entire path structure so that the archive indicates 
exactly where the file belonged. ie. /root/var/log should preceed every file in the archive.

[root@localhost ~]# yum install star

[root@localhost ~]# star -c /root/var/log f=user-logs.tar 

star: 205 blocks + 0 bytes (total of 2099200 bytes = 2050.00k).

6. List the contents of the star tar file.

[root@localhost ~]# star -t f=user-logs.tar

7. Compress the star archive into a bzip2 compressed file.

[root@localhost ~]# yum install bzip2

[root@localhost ~]# bzip2 user-logs.tar

8. Decompress the star archive into the /root home directory. 

[root@localhost root]# star -bz -x f=user-logs.tar.bz2
