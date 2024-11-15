# rhcsa
bg Display stopped or background jobs
fg     or fg n
kill or kill -9 pid Kill process with id pid
killall processname Kill all processes by name
lsof List all files opened by running processes
pidof processname Get the PID of any process
pkill name Kill process with name 
pmap –x PID [pid]
ps Display all active processes
ps -ef | grep processname Display info of specific process
pstree Display processes in the tree-like diagram
top  or htop Show real time processes
watch -n 5 'ntpq -p'
find  /home -size +100M                        
find /home/usename  -name 'prefix*'   
find /dir/ -mmin num Find files modifed less
grep -r  pattern directory          
grep pattern files Search for pattern in files
grep -i Case insensitive search
grep -r Recursive search
grep -v Inverted search
grep -o Show matched part of file only
find /dir/ -name name* 
whereis command Find binary / source /
locate file Find file 
touch file1
cat file1 file2 Concatenate files and output
less file1 View and paginate file1
file file1 Get type of file1
cp file1 file2 Copy file1 to file2
mv file1 file2 Move file1 to file2
rm file1 Delete file1 (rm -rf )
head file1 Show first 10 lines of file1
tail file1 Show last 10 lines offile1
tail -F file1 Output last lines offile1
echo [text]>>[file_name]
diff [file_name_1] [file_name_2]
tar cf archive.tar directory         
tar cjf archive.tar.bz2 directory 
tar -cvf filename.tar filename
tar czf archive.tar.gz directory   
tar -rvf filename.tar file2.txt
tar -tvf filename.tar
tar xf archive.tar                         
tar xjf archive.tar.bz2                
tar xzf archive.tar.gz                   
unzip filename.zip
unzip filename.zip -d /dirname
unzip -l filename.zip
zip -d filename.zip file4.txt
zip filename.zip file1.txt file2.txt file3.txt
zip filename.zip filename
zip -u filename.zip file4.txt
sed
shutdown  or -r  or -h 0
swapon -s
tab
wc
history, history -c && history -w
gpg -c [file_name] /gpg [file_name.gpg]
crontab –e
alias [new command name]=[command]
at [-V] [-q queue] [-f file] [-mldbv] TIME
finger [username]
groupadd groupname Create a new group
groupdel groupname Remove a group
id Display UID and GID of the current user
last Display information of the last login user
passwd
useradd -c  "full name" -m  username     
userdel -r username Del ete a user account
usermod -aG groupname username Add a user to a specific group
w Display all login users
1st is owner permission, 2nd is group & 3rd is everyone.
4 read (r) 2 write (w) 1 execute (x)
chmod 766 filename Assign full permission to the owner, & read & write permission to group & others
chmod 777 filename Assign full(read, write, and execute) permission to everyone
chmod -R 600 folder Recursively 
chmod -R 777 dirname Assign full permission to the directory and all sub-directories
chmod -x filename Remove the execution permission of any file
chown -R user:group dirname Change the owner all sub-directories
chown usernamefilename Change the ownership of a file
chroot [path] [command]
date Show system datem  timedatectl set date
uptime Show uptime
who & whoami Show your username
man command 
export NAME=value Set $NAME to value
$PATH Executable search path
$HOME Home directory
$SHELL Current shell
pwd Show current directory
mkdir dir Make directory dir
cd dir Change directory to dir
cd .. Go up a directory
ls Options -ahalrt
-a Show all (including hidden)
-R Recursive list
-r Reverse order
-t Sort by last modified
-S Sort by file size
-l Long listing format
-1 One file per line
-m Comma-separated output
-Q Quoted output
ln -s /path/to/file  linkname             
badblocks -s /dev/sda Test for unreadable blocks on disk /dev/sda
df -h or df -i or df -m                                          
du   -ah, -sh,  -h -T  (nc  or ncdu )                              
du -hs Display the size of your current directory
fdisk /dev/sda Create a new partition on /dev/sda device
fdisk -l List all disk partitions
fsck.ext4 /dev/sda1 Check and repair a filesystem for any error
hdparm  -i /dev/sda         
hdparm -tT /dev/sda Perform a read speed test on disk /dev/sda
lsblk Display information about block devices
lsusb -tv Display all USB devices
mkfs.ext4 /dev/sda1 Format the partition named /dev/sda1
umount
mount /dev/sda1 /mnt Mount any partition to any directory
watch df -h                                  
init
insserv
rcconf
rcctl
rc-update
mkfs
mpstat 1                                                       
systemctl enable/disable/start/stop/restart/reload
systemctl hibernate
systemctl list-unit-files
systemctl list-units --type=path --all
systemctl list-units --type=service
systemctl list-units --type=socket --state=LOAD
systemctl suspend
systemd, systemd-analyze,systemd-analyze blame
service ssh start or stop or restart or status
 more -f /var/log/messages
/var/log/auth.log: Auth logs 
/var/log/boot.log: System Boot log 
/var/log/daemon.log:  related OS
/var/log/debug: Debug logs 
/var/log/httpd/: Apache access and error logs
/var/log/kern.log: Kernel logs 
/var/log/maillog: Mail server logs 
/var/log/mysqld.log: MySQL database  
/var/log/yum.log: Yum command logs
cat, tail -f , less, head /var/log/messages
grep -i error /var/log/messages
sudo dmesg | grep 'error' | more 
sudo dmesg | grep -i -E 'error|warn|failed'
journalctl _SYSTEMD_UNIT=sshd.service
journalctl -b  boot log
journalctl --dmesg
journalctl -f  -r  -nx 
journalctl -k -b -1  kernel
journalctl -k -g failed
journalctl -p info
journalctl --since "1 days ago"
journalctl --since yesterday
journalctl -u sshd.service
zcat – Displays all the contents of logfile.gz
zgrep – Search inside a compressed file
zmore – See the file in pages, without decompressing
cat  /proc/meminfo              
cat /etc/issue
cat /etc/redhat-release     
cat /proc/cpuinfo
cat /proc/cpuinfo              
dmidecode | less
chkconfig
env
export [variable_name]=[variable_value]
uname -a Show system and kernel
head -n1 /etc/issue Show distribution
ulimit
unset [variable_name]
update-rc.d
free or free -h                        
lshw | less
lsof ,lsof  -u user                                               
lspci (or -v for verbose),lspci -tv                          
lsusb (or -v for verbose), 
iostat
curl [options] [URL],wget 
rsync  -avz  /home server:/backups/   
rsync -a  /home /backups/                 
scp file.txt  server:/tmp           
scp -r server:/var/www  /tmp            
scp server:/var/www/*.html  /tmp    
program &                                                                       
Files: tar · pv · cat · tac · chmod · grep · diff · sed · ar · man · pushd · popd · fsck · testdisk · seq · fd · pandoc · cd · $PATH · awk · join · jq · fold · uniq · journalctl · tail · stat · ls · fstab · echo · less · chgrp · chown · rev · look · strings · type · rename · zip · unzip · mount · umount · install · fdisk · mkfs · rm · rmdir · rsync · df · gpg · vi · nano · mkdir · du · ln · patch · convert · rclone · shred · srm · scp · gzip · chattr · cut · find · umask · wc · tr
"Processes:  alias · screen · top · nice · renice · progress · strace · systemd · tmux · chsh · history · at · batch · free · which · dmesg · chfn · usermod · ps · chroot · xargs · tty · pinky · lsof · vmstat · timeout · wall · yes · kill · sleep · sudo · su · time · groupadd · usermod · groups · lshw · shutdown · reboot · halt · poweroff · passwd · lscpu · crontab · date · bg · fg · pidof · nohup · pmap Networking netstat · ping · traceroute · ip · ss · whois · fail2ban · bmon · dig · finger · nmap · ftp · curl · wget · who · whoami · w · iptables · ssh-keygen · ufw · arping · firewalld
"
"Logs - ls -l  /var/log cat /var/log/messages
The Authorization Log:  sudo command or user logins,
The Daemon Log:  Bluetooth and SSH.
The Debug Log: applications that log to syslogd.
The Kernel Log: ctivity involving the Linux kernel.
The System Log:  types of global activity on your system.
The Fail Log:  failed logins
who, last and lastb read logs like utmp,wtmp,btmp
utmdump, systemctl, sudo lastlog, last | grep ""logged in""
grep, tail, head, sort, w and last reboot
journalctl -b,-f,-n, -k, -p.-u NUM, crit, journalctl --list-boots
journalctl --since “YYYY-MM-DD HH:MM:SS” --until “YYYY-MM-DD HH:MM:SS”
journalctl -b -NUM -n
cat /var/log/auth.log | grep 'Authentication failure'"
