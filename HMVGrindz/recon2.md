#Url/link
https://hackmyvm.eu/hmvgrind/srv-01.php
#Concept 
bit deep Recon
#Challenge Description
Now, I wanna know how many users have /bin/hmv as their default shell?
- Oki.
#Method of Solving
I have used the cat/etc/passwd command to look for all the file roots that have passwords and then we grepped -e :
 Find and count user accounts that have /bin/hmv in their /etc/passwd entry

''''
l0n2536:~$ cat /etc/passwd
root:x:0:0:root:/root:/bin/sh
bin:x:1:1:bin:/bin:/sbin/nologin
daemon:x:2:2:daemon:/sbin:/sbin/nologin
lp:x:4:7:lp:/var/spool/lpd:/sbin/nologin
sync:x:5:0:sync:/sbin:/bin/sync
shutdown:x:6:0:shutdown:/sbin:/sbin/shutdown
halt:x:7:0:halt:/sbin:/sbin/halt
mail:x:8:12:mail:/var/mail:/sbin/nologin
news:x:9:13:news:/usr/lib/news:/sbin/nologin
uucp:x:10:14:uucp:/var/spool/uucppublic:/sbin/nologin
cron:x:16:16:cron:/var/spool/cron:/sbin/nologin
ftp:x:21:21::/var/lib/ftp:/sbin/nologin
sshd:x:22:22:sshd:/dev/null:/sbin/nologin
games:x:35:35:games:/usr/games:/sbin/nologin
ntp:x:123:123:NTP:/var/empty:/sbin/nologin
guest:x:405:100:guest:/dev/null:/sbin/nologin
nobody:x:65534:65534:nobody:/:/sbin/nologin
bot:x:1000:1000::/home/bot:/bin/sh
hmvb0t1:x:1001:1001::/home/hmvb0t1:/bin/hmv
hmvb0t11:x:1002:1002::/home/hmvb0t11:/bin/hmv
hmvb0t21:x:1003:1003::/home/hmvb0t21:/bin/hmv
hmvb0t321:x:1004:1004::/home/hmvb0t321:/bin/hmv
n0b0dy:x:1005:1005::/home/n0b0dy:/bin/sh
l0n2536:~$ cat /etc/passwd | grep -e "bin/hmv"
hmvb0t1:x:1001:1001::/home/hmvb0t1:/bin/hmv
hmvb0t11:x:1002:1002::/home/hmvb0t11:/bin/hmv
hmvb0t21:x:1003:1003::/home/hmvb0t21:/bin/hmv
hmvb0t321:x:1004:1004::/home/hmvb0t321:/bin/hmv
l0n2536:~$ cat /etc/passwd | grep -e "bin/hmv" | wc
        4         4       184
l0n2536:~$ 



'''''
#
