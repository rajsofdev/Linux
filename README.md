# Linux
 

#ls

#clear

#touch :- create empty files

#pwd = current working directory

#cat filename = show the file content

#cat > filename = to write something in file and redirect it then press Ctrl + C to exit and save thhe file

#clear = it clear the screen

#cd = change directory

#cd -= it will take to last change directory

#cd ~ = it will take to home directory

#cd ..= go back to one directory

#mkdir DirectoryName= to make directory

#mkdir directory1 directory2 directory3 = make multiple directory 

#mkdir –p 1/2/3/4/5/6 = make directory inside the directory
#rmdir directoryname= remove empty directory, rmdir does not work on non-empty directory

#rm –rf = it remove non empty directory without asking anything, it delete the file or directory forcefully without any confirmation.

#rm –i filename = it ask whether you wants to remove the file or not

#history = to know what command I have typed 

#!<command number> = it will execute the command which is available in history

#history – c = to remote the history from the history command

#uname – a= tell the machine name and its details version etc

#date = show the date of machine

#date +%F = show the full date

#date +%D-%M-%Y = show the full date wit – format

#touch filename{1..100}.txt = create file filename from 1 to 100 with .txt

#cate filename= see the content

#cp filename <destination path> = copy the file from source to destination 

#cp *.txt <destination path> = copy all the .txt file 

#ls –ltr filename = see the file details or properties

  #cp –pv filename <destination address> = copy the file without changing its properties

  #cp –Rv directory_name <Destination address> = copy directory from one location to other

  #mv filename <destination path> = file will move to destination address

  #mv filename newfilename = it will change the filename or it will rename the file

  #rm –i filename = delete with confirmation 

  #rm –f filename = remove the file without confirmation it delete forcefully

  #rm – r directory name = remote the directory without confirmation it delete forcefully

  #rm –rf directory/filename = it delete the directory without confirmation along with files 

  #ls = simply show the files or directory

  #ls – la = show the files and directory with permission or with properties

  #ls –d = show directory only

  #ls –ld = same

  #ls –m = show file using cama list

  #df = show partition

  #df –h = show partition in human readable format 

  #df –T = current path 

  #more = read more log file, q to quit it

  #who = currently logged in account 

  #who –r = run level
#who –H = show who logged in and when
#who – a = show when system logged in and who along with IP addre
#w = similar as above, show how many user logged in
#ps = list the process
#ps  - aux = all running process with details
#ps –U <username> = details about user
#chmode = change the permission of file
#chmode +/-/<permission number> <filename> = to change rwe permission, read = 4, write = 2, execute = 1, it will have 3 digit number, first have user, second have group and third have others
#chown = changing file or directory ownership
#chown <Username or group name>:<root> <filename> = change the file permission to root
#chgrp = for group
#du –sh /<patch> = show the size of files
#tar –cvzf <filename for compress> /<patch of the file> = zip the path file into file name as a zip
#tar –xvf <zipped file name> = unzip the file
#scp <filename> root:<IPaddress>: /<filepath on remote machine> = copy the file from remote to the host client machine with filename. Copy the content to filepath
#find / –iname <filename> = it will show the file patch
#updatedb = update the database

Standard input(stdin = in alphabetic, in number its 0, symbol <) is a input which is given for a command like – ls etch
Starndard output(stdout = in alphabetic, in number its 1, symbol >) is which comes in result
Standard error(stderr = in alphabetic, in number its 2, symbol 2>) its occurred while executing any standard input

#ls /root 2> /temp/errors = errors will be redirected in given path errors and it will show the error in redirected errors file
#ls /root >> /temp/errors 2>&1 = it will append the error and details in that file, you can see the file output while using cat command
#cat /temp/errors = it will show the output
>> = use for append
>= use for write it in the file
#sudo tails –n <number of lines> /var/log/messages > /home/raj/loglies20 = Top n lines transferred to other file
#mail –s “testig stdin mail subject” raj@localhost < /temp/errors = it will send the mail in mail body
#mail = it will open the mail in texting 

Grep command with Regular expression 
#grep –V = grep version 
#grep = use to filter the output
#grep raj < /etc/password = it will take input from the password file and filter then show only raj line which is available in file, < = use for input.
#grep –V = version of grep command
#grep <string to search> filename = show the searched string line
#grep –i <string> <file name>= -i ignore the case sensitive 
#grep –v <String name to ignore the line> <file name>= show remaining string
#grep –vi <string to un-match> = it will show rest of the file content which is matching, it ignore the case sensitive as –I mentioned.
#grep <String> -A 2 <filename> = it will match the string then it will print after 2 line
#grep <stirng to search> –C 1 <file name> = one line up and one line below
#grep –B = it will show up line after matching the file
#grep “demo$” <filename> = it will print the line which had demo in end of the line, $ represent the end of the line.
#echo $GREP_COLOR = show the colour
#export GREP_COLOR = ‘1;30;42’ = it will change the matching colour to yellow for green use 1;30;42
#ls –la | grep “Raj” = show the raj output matching lines


Figlet Arching and Compressing = 
Having three method to compress the file : Gzip and bzip 
	Gzip – gun zip
	Bzip – bun zip
	Normal zip
#du –sh . = it will show the files and directory
#tar –cvf <filename_with.tar> <filename1 filename2 which need to archive> = it will archive the files, the cvf denote as c – create, v – verbose, f – all the files
#du –sh <filename> = to see the file size
#tar –cvzf <filename_with.tar.gz> <filename1 filename2 which need to archive> = archive and compress by gun zip, this archive file will have the less size compare to original file
We can update the archive with ne files or after modifying the file. 
#tar – uvf archive.tar *.txt = it will update the files in archived .tar file and update the new files in that, it does not update in compressed file. 
#tar –tf <archive name > = to list the all archive files
#tar –xvf <archive file> = to extract the archive file, x- extract, v- verbose, f – files
#du –sh *.txt = it will show all the .txt files details with size
#tar –cvjf compress.tar.bz2 *.txt = it will compress all the .txt file with name of compress.tar.bz2, it’s a bun zip method to compress the file
#tar –xzvf <compressed filename> = extract the file using the gunzip
#zip test.zip *.txt = all the file compressed using the normal zip method
#zip -9 –r  test1.zip /<filepathname which need to zip> -x /<give path which you need to exclude in zip> =  it will compress more highly, 9-use for high compressing and –r use for directory
#zip –cvjf *.txt –x /<path to exclude in archive> = it will exclude the file which is placed after –x  position.
#zip –d <zipped filename> <path to delete the file from the zip> = it will delete the file from the zipped directory, the will be deleted from the zip
#unzip <filename> = it will unzip the file


 Vi and vim command = to edit configuration files
Command mode
	dd – delete current cursor positioned line
	d5d or 5dd = Delete 5 linnes below of the cusor position
	x – delete single character left to right
	5x – delete 5 characters left to right
	yy – copy line current cursor position line
	y5y or 5yy – copy 5 lines below the cursor
	p- past the copied lines below the cursor
	P- past copied line above the cursor
	dw – delete the single word
	u– undo last action
	U – undo all the changes to the current line
	j– join the line
	.- redo last action 
	w- will move to the beginning of the next word
	nw – will move the nth word beginning 
	b – will move beginning of the previous word
	nb – will move begininning of nth previous words
	{ - move backward one paragraph
	} – move forward one paragraph
	0-will go to home posion
	$- will go to end of the line position
	k– use of upp
	h– move from right to left
	j-move to down
	i-move left to right
	Shift+G = go to last line of the file
	Shift+h == go to first line of screen
	Shift+z = save & quit
	/stringName = search particular word in the file
	n-search strings from the top to bottom
	N-search from bottom to top

Insert Mode
	i-insert Data before the cursor position 
	I-insert content starting of the line
	a=it will append current line characters
	A=it will append the characters from end of the line
	o=it will insert a new line below the cursor
	O=it will insert a new line above the cursor
	S=substitute the stream
	r=replace the current character
	‘home’ key to go to home of the line
	‘end’ key to go end of the line

Execute – Mode
	Esc key to change the mode to execute mode
	:q- Quit file
	:w=writ file
	:wq= save and quit.
	:x=save and quit
	:q!= quit forcefully
	:wq!=sae and exit forcefully
	:1=got o first line of the file
	:set nu=set the line numbers
:set nonu= remove line number 
	:<specify line number> = specified line number.
	:r /root/test = copy the content of test file in ursor current position
	:r !date = the command output will paste in current cursor position
	%s /<oldstring>/<newstring>/g = it will substitute the old word with new word, g use for global, use c at place of c if you wants to control the replacement like single or all string


MAN command to get help
Mam mam- get man help 
 
#man man = show all the details
#man passwd = show the password file usage, type / and search any string it will highlight like example /all
#man –s 5 passwd = show the manually use of command details for developers 
#man –k printf = short details of prinf, it will show the  matching and its descriptions
#man –s 5 –k password = it will show the password details
#pinfo = its same as man command
#info = also same as the man
#whereis = provide the exact path where that command is stored, for example whereis ls or whereis python
#echo $PATH = it will show the path
#whatis passwd = it will tell about the command

OpenSSH Server and Client Configuration -
telnet is not providing any security, it send the data in plain text.
Using SSH the data will be encrypted and it does not send the data in plain text, ssh does verify using the key from server
To install the SSh server we need to type the command – yum install openssh-server, then login with root user and re-start it using systemctl restart sshd and then enable it while typing systemctl sshd enable
vi /etc/ssh/sshd_config = it will open sshd configuration file and add a line below port 22 as Protocol 2 then go to do authentication permit, below Password Authentication as yes at below
Banner = it give some message beforelogin to ssh
PermitRootLoginn no = keep this login as no, if we put yes then any remote user can login as root and they can do anything in machine
#usePam = 
#allowGroups sshusers = its allow sshusers to login 
#adduser <username> = to add the user in server machine
#groupadd sshusers = add the sshusers in machine
#usermod –aG raj sshusers = it give the raj permission to sshusers group
#cat /etc/passwd = it will show how many users are there
#passwd <username> = it will reset the user password
#cat /etc/passwd | grep user = to filter and check the user details 
#id <username> = to know the user id and it’s a part of which group or not
#sudo –s = login as admin
#ssh <username>@<serverIP> = it will connect remotely using ssh service
#systemctl status sshd = it will show the ssd status 
#vi /etc/issue.net = edit and type Welcome to $HOSTNAME $USER then save and exit, when any user login the will get this message. It will give you welcome message

 
#ssh-keygen –t rsa = it will generate the key 
Copy these key file to remote server to avoid login again and again, generate keygen at client machine and run below command to copy the key to server.
#ssh-copy-id <username>@<serverip> = it will copy the id to remote and it will create a file on server for authentication , if you login again from that machine then it will not ask any password while login
#man –s 5 sshd-config = it will show the details.

If you forget the password and wants to reset it then re-start the machine and interrupt while booting using space bar key and then hit e key for edit the kernel go down and you will find the linux16 line then go to end of the line and add rd.break console=tty1
 
Press ctrl + x to start the machine, you will see the single user mode only and you will see the root user then run mount command, it will show all the mounted command
#mount sysroot = it will mount sysroot
#mount | grep sysroot
#mount –o remount,rw /sysroot = it will give read write permission
#mount | grep sysroot = to check the details
#chroot /sysroot
#passwd = to change the password
#touch /.autorelabel = create this file carefully then exit from the process then reboot the machine 

Securely Copy Data :- 
Securely copy the Files from one server to another server
scp = secure copy 
#scp <Filename which you need to copy> <username>@<destination_serverip>:/<destination file patch> = it will send the file from the source server to destination server.
#scp <multiple file name> <destination path> = this will copy the multiple files to destination server
#scp –r <Directory name> <destination user name>@<destination IP>:/<path to store date> = it will transfer the directory to destination address.
#scp –C filename <destination user name>@ .. = it will compress the data and send to destination file
The copied data date and time will be change if we follow above command, if you wants to preserve the date and time then use below command
#scp –rvp <file name which you want to send> <username>@ .. = it will send directory with preserved file stamp, we can remove r for files if you don’t want to copy directory.
#scp –l 500 <filename > = it will reduce the bandwidth to 500Kbps

Listening and Managing Processes:- 
A program loaded into memory and executed is called a process
	The first new process will be created by a fork() system call, which is system pd PID1
	A new process is normally created when an existing process makes an exact copy of itself in memory. The child process will have the same environment as its parent, but only the process ID number is different
Process types and states
	Foreground process - initiated and controlled through a terminal session.
	Background Process - Automatic process not connected to a Terminal
Sleep 300 &
#ps –aux | grep <process id ex 2798> = it will show the process 

There are many types of process states
	1 Running – The Process is either running or it is ready to run.
	2 Waiting – The Process is waiting for an event or for a resource.
	3 Stopped – The Process has been stopped, usually by receiving a STOP Signal.
	4 Orphaned – If the process exits with children still running, those children are orphans. It will be taken by other process, need to google.
	5 Zombie – This is a halted process which, for some reason, still has a task_struct date structure in the task vector. 
 

 
#pstree = use to see all the parent and child process
#ps –aux –z = the process which is died as zombie process
#ps –a = it will show all the running process currently
#ps –e = it will show all the running process currently
#ps –r = it will show all the process owned by you
#ps –fU <username> = view process of that particular user
#ps –fG <usergroup> = view all process by groups of users
#ps –eo pid, ppid, user,cmd = view custom fields
#ps – ef  = it will show all the process 
#ps –ef | grep sleep = it will show sleep process
#ps –C http= search with name process
#jobs = command show the backend running command
#fg %<process id>= to bring the command to for-ground from the background
#kill -<process id> = to kill or terminate the process
#pgrep –u root = it will show all the root process which is running
#pgrep –u root ssh – root process with ssh
#preg –l = 
#kill –l = show all the process 
-20  is the highest priority value and 20 is the lowest priority value
#ps –aux = it will show all the process which is running


Create Partitions :- 
Disk Partitioning – 
#fdisk –l = show al the partitions of the hard drive
#sudo fdisk –l = same as above if the permission denied
#df –h = it will show the disk usage partition
Only 4-primary partitioned can be made in hard drive or you can make 3 primary partition and rest you can make n number of logical partition.
#ls /sys/class/scsi_host/ | while read host ; do echo “---” > /sys/class/scsi_host/$host/scan ; done = run this command to scan the attached scsi hard drive or do re-start the machine to show the attached hard drive.
#fdisk –l = it will show all the hard drive which is attached externally
#fdisk –l  /dev/sdb = check the hard drive
#fdisk /dev/sdb = to make partition then type m, it will show all the option for partition
N = to make new partition 
Then select the primary or extended as p or e
Then select the sector for hard drive size just hit enter and given +5G = for 5GB partition
Now the partition is created then type p to list the sector of partition, wq is write and quite it after partition. This will be not known by kernel so we need to run below command.
#partprobe /dev/sdb = this partition will be updated in kernel
#mkfs.ext /dev/sdb1 = it will make file system, it will create blocks in memory, its called master block, supper block, Inode block and data block
#mount /dev/sdb1 /part1/ = it will mound the hard drive


Simple Commands which use normally
#poweroff = it will shutdown the machine
#reboot= it will reboot the machine, we can use systemctl reboot also
#last = it will show the user login details 
#last <username> to see the user login details
#tree /etc = it will show all the directory tree
#stat <filename or directotry name> =It will user for security reason, it show when this file get modified or change etc
#cat <filename> | wc = it will show the number of lines, word and char. We can see separately using |wc –l for line, -c for char and –w for words
#whereis <command name> = it will show the path of command
#man <command name> = see the command details
#df –h or df = use to see the storage
#df –hT = to see the file system of the directory also
#du –sh <file or directory name > = to see the file or directory size


Nano  = its Plan text editor, we can directly edit in note pad editor
	Nano provides more feature than PICO
	Coloured test for writing scripting language example: C, C++, Scripting and Perl .ETC 
	Smoothing scrolling
	Simple control Keys
	Regular Expressing support to search Text in file
	Multiple buffers to Do undo Redo and Edit text
#nano <filename> = to create file using nano editor
	Alt + Spacebar = word by word moving, up arrow and down arrow key use to move up down, Ctrl + A beginning of the line, Ctrl + E use for end of the line, Ctrl + U or F10 – to past the copied line, Alt + t to cut the line, Alt + u to copy the line, Ctrl + M  - new line, Ctrl + d – to delete. F2 to save the file. Ctrl + x to exit from the file
#nano /etc/nanorc = it’s a nano configuration file, scroll down and at below of the line which has include “/usr/share/nano/*.nanorc” add include “/usr//share/nano/sh.nanorc”. you can add the language like, sh, c+, perl, etc when you write then it will give you colouring 

Creating and Deleting Partitions -
	Partitioning is nothing but creating logical regions of the hard disk/storage
	Store different types of data
 
Steps for creating Partition –
	Attach new disk to the server
	Scan for new hardware changes or reboot
	fdisk /dev/newdiskname
	n, part type, specify size and save & exit
	udevadm settle
	Make file system
	Mount and add fstab entry for permanent mount
#lsblk = it will show the drive details
#fdisk –l = to check whether the new hard drive added or not, reboot the machine or scan the new hardware to detect the added storage
#udevadm trigger = then run #fdisk –l to check again I no then then run below command
#fdisk /dev/new disk name = to create a new partition, n-new partition, e –extended, p- for primary partition, +<size of partition in GB>G – give size of partition G-denote for GB, then you can exit while typing wq: , if you wants to continue create then follow the same procedure
#mkfs.xfs /dev/<partitionname>= make that drive as xfs drive using this command, you can choose as file system you wants to make.
#mkdir /<directoryname to mound the partition> = create directory to mount it, suppose create data1 directory then mount using below command
#mount /dev/<partitionname> /<directory to mount ex data1> = it will mount the partition
Steps for Delete Partition –
	Run Final archive backup
	Bring down applications hosted on partition 
	Un-mount mount point
	Delete partition using fdisk/gdisk utilities 
	Destroy the HDD
#unmount /<partition name> = it will unmont the partition
#fdisk /dev/<hddname> = follow and press d to delete the partition
#udevadm trigger = to update it, then the partition will be deleted

After re-start the machine the mount disc will be removed so to fix this and add into kernel we need to follow below command #vi /etc/fstab
Then add the entry here - /dev/sdb1	/part1	ext4	default 0 0
Save and exit
Mount –a = to check
Df – h = it will show mounted partition – now if we reboot the machine then also the partition will be there. If you wants to delete the partition then we need to go to fstab and remove it
Vi /etc/fstab = comment or delete the live which you wants to delete the partition then run umount /part1 to delete permanently. It will un-mount the partition from the entry. Sometime the partition will not delete if you wants to delete as might be somebody will be using it so we have to kill that process then we can delete it.
Df – h= you can check from here,
Fsdisk /dev/sdb = print the partition then hit d to delete and give number to delete the partition 
#partprobe /dev/sdb = to update the partition 

LVM – logical Volume Manager

LVM is used for the following purposes: Creating single logical volumes of multiple physical volumes or entire hard disks (somewhat similar to RAID 0, but more similar to JBOD), allowing for dynamic volume resizing
To increase the partition we need to unmount it then make it offline then increase the partition size and mount them again so there is a lot of down time will be given. Its time taken. To avoid such thing and to increase the storage the LVM comes in picture. 
LVM gives more sophisticated result to increase the volume size.
If we write the date of 100mb in a single drive so we add 3 hard drive and each will take 20 second to finish the writing. We will make logical volume to make fast writing.
Add the external hard drive in machine from virtual box then run fdisk –l to list all the hard drive attached with machine
#fdisk /dev/sdb = make single partition the save and quit using wq
#fdisk /dev/sdc = make as above, sdb and sdc both are externally added hard drive
#fdisk –l /dev/sdb = to see the partition details of sdb drive, similarly you can see the sdc partition. These partition are not in linux LVM, its only into linux standard partition then we need to convert into LVM to create logcal partition to add in group
#fdisk /dev/sdb = then type t then type L to see all the code to convert all the partition then type 8e to convert the partition to LVM as LVM partition code is 8e then save and exit then verify once and update the partition using partprobe /dev/sdb and then sdc also 
#fdisk –l /dev/sdb = now you can see both volume will be converted into lvm.
#pvcreate /dev/sdb1 = Make partition using this command after converting into LVM, similarly make sdc1
 
#pvs = to see the partitions, how many pv is exists, physical volume
#vgcreate VG0 /dev/sdb1 /dev/sdc1 = it will create the volume group. Where sdb1 and sdc1 will part of this group, we can add many partition in this group after creating lvm partition
#vgs = to see the volume created details, we can also use vgdisplay <VG name like VG0> to see the details.
 
Now we are going to create logical volume using below command
#lvcreate –n lv0 –L 4G VG0 = it will create 4GB logical volume, to see the logical volumes you can type lvs. Similarly you can create lv1, lv2 etc local volume.
 
#lvdisplay /dev/VG0/lv1 = it will provide total size and details of lv0
#lvdisplay /dev/VG0 = to see all the logical volume of VG0 group in details 
Now you can create file system and mount them to logical volume permanently using below command 
# mdfs.ext4 /dev/VG0/lv0 then hit enter it will format the partition, similarly we can make xfs file system using #mkfs.xfs /dev/VG0/lv1
#mkdir /ext4part = to make directory to mount for ext4 and similarly we can make xfs file system like mkdir /xfspart.
# vi /etc/fstab = edit the file and add the file system using /dev/VG0/lv0	/ext4part 	ext4	default	 1	2 = similarly you can add lv1 also like /xfspart xfs defaults 1 2 
Mount –a = to mount it
Df –h = you can see the partition here

How to extend the file system without interrupting the process
Earlier we see how to create a logical volume and how to mount them permanently but how to extend the file system without interrupting we will see here.
#sudo vgs = to see if we have any existing free VG space or not.
 
#pvdisplay –m = will give you details information how many physical extend are used. Physical extent is a block sizes.
#lvdisplay /dev/VG0/lv0= to see the logical volume details
#lvs = to see the lcs
#mount = see the mounted details
 
#lvextend –L +1G /dev/VG0/lv0= extending 1GB in logical volume lv0, it will take the 1Gb from the free space of VG0 and add in logical volume.
#df –h /ext4part = you can see the partition size here it will be extended
The extended size will be not added in file system so it will not show in file system so we need to add it in existing lv follow below command, 
#resize2fs /dev/VG0/lv0, now it will show the exact size of extended size of file system.
#df –h = see thhe file system.
Similarly we can add in lv1 but to extend the file system you need to run the command #xfs_growfs /dev/VG0/lv1 , it will beextened the FS.

Reduce LVM --
Backup partition data
UN-MOUNT Partition
Check Block level errors and fix it 
Resize file system
Reduce LVMS sizes 
Mount and use
How to reduce LVMS size ======
1.	Shutdown all the applications/databases which are hosted in lvm
2.	Compoeted backup
3.	Unmount lvm file system
4.	Hashout enty in /etx/fstab
5.	Ext2/ext3/ext4
6.	Check for any errors
1-	No xfs reduce  its having completely different menthod
#vi /etc/fstab = disable or commend or remove entry
#unmount /ext4part/ = unmount it
#df –h = see 
#e2fsck –f /dev/VG0/lv0 = to checkthe file details if there is any error available
#resize2fs /dev/VG0/lv0 1G = it will reduce 1GB from the file, you can remove as you wish while giving the reduce size. 
#lvreduce –L 1G /dev/VG0/lv0 = the partition file system reduce to 1GB
Then got o #vi /etc/fstab and uncomment the file system then mount it #mount –a to mount again with reduced size

How Swap File System Works. ===
Memory swapping to boost the speed.
#fdisk –l /dev/sdc = it will show the file size here
#free –m = swap memory it will show
#fdisk /dev/sdc = make partition and swap the memory, 82 is the code which will made th swap memory, wq save and quit
#partprobe /dev/sdc = to update it and to see you can type #fdisk –l /dev/sdc1
#mkswap /dev/sdc1 = to make swap of particular partition 
Now we will mount the partition 
#vi /etc/fstab 
/dev/sdc1	swap	 swap	 default 	0	0= save as wq 
#swapon –s = it will show the file system
#swapon –a= it will add the swap partition
Now you can see swap –s then free –m
#swapoff /dev/sdc1 = it will off the swap to check you can use swapon –s.
#blkid /dev/sdc1 = in order to verify the swap is on or not
#sar –A = details about how many pages in and out

Create Users =========
There are 3types of user in Linux – 
(1), supper user or administrator user or root user, UDI will be 0, 
(2) – normal users which is created by root user and it’s has the UID 1000 in RHCSA and now a days its increase from 1000 to 65000. 
(3) Service user like ftp, nfs, nfsnobody, vsftpd etc services, the id start from 1 to 999. The services which is created by system or to perform the other services its created called service users.
#useradd = to create user and it will modify following files home, login shell, group, .bash_profile, .bash_logout, -/etc/passwd, etc/shadow, etc/gshadow(this will modify only while using group users, users), etc/skel, etc/group
#cat /etc/passwd = it will have all the system users entry, chrony – use for time management, these has all the system services entry.
After user it use x it means the password is encrypted, When user logged in then it will show default bin/bash shell, only one primary group can be assigned but we can assign multiple secondary group.
#cat /etc/default/useradd = it will show default user in this file, this user never be inactive. Whenever user created the default details will be taken from here like home directory, skel, group etc
#cd /etc/skel = then run ls –la – it will all the hidden files and you can create some file like default file, whenever a user created then this default files will copy to user home directory directly
#cat /etc/login.defs = it will have login definition like password expire details, where mail save like /var/spool/mail it store. It will have the encryption method.
#useradd test1 = create test1 user, then change the password using sudo permission then check in passwd file whether user entry has done or not, to check #cat /etc/passwd | grep test1
#cat /etc/group | grep test1 = to check whether test1 group is created or not
#cat /etc/shadow | grep test1 = to see the password file for test
#cd /home/ = go to home and run ls command to check the user directory then go totest1 and see the default file is created there or not.
#useradd –u 2000 –g test1 –G test1, rk, user1 –c “Administrator for user of RHCSA” –s /bin/bash –d /opt/rhcsa –e 2021-07-25 –p Password1R RHCSA= create user in customized way, u – user id, -g = primary group, G- secondary group, c – comment like “Administrator user for RHCA”, -s – set the shell path,  d – specify the home path, e- expiry date for this user like YYYY-MM-DD, -p – for password ex Password then give username RHCSA.

How to change user properties – 
#usermod = use to change user properties, modify the user.
#usermod –l <new user name> <old user name> = it will change the old username to new user name
#usermod –aG rk,user1 spiderman=it will add the user spiderman to multiple group like rk and user1 etc, -aG - append the group
#id spiderman = to see all the group which is added with spiderman
#usermod –g user1 spiderman = it will add in primary group from older to new group of user1. To check the spiderman group status please use below command
#id spiderman = check the status
#usermod –s /sbin/nologin spiderman = it will stop user to login using remote, it will not have the login shell
#usermod –s /bin/bash spiderman = it will provide shell to login
#cat /etc/shells = to see all the login shells
#usermod –L spiderman = observe the user login attempt, you can see the login or locked activity then run cat /etc/shadow | grep spiderman – it will show the exclamatory markk if the user is locked, after running this command it will get locked and you can see in shadow file
#usermod –U spiderman = it will unlock the user for login, it will not have exclamatory mark in shadow file
#usermod –f spiderman = if you wants to inactive user completely
#usermode –c “user commend” spiderman = you can add the user comment
#chage –l spiderman = to see the account details 
 
 
#chage –m 0 –M 90 –W 10 –E YYYY-MM-DD spiderman = it will change the account details, m- minimum password change day, -M – change the maximum password change, -W no of warning, -E password expiry date.
 
#groupadd <group_name> = to create the group we use this command
#cat /etc/group= you can see the group names here and its details
#uusermod –G <Group name> <username> = to add the users into secondary group, G –use for secondary group
#groupmod –ptest <group username> = if you wants to make confidential of that group then you can protect the group using the password 
#gpasswd –a <username> <group name> = we can give a particular user permission in the group to add and modify the other users in that group. This user become the administrator of that group
#gpasswd –M <user1> <user2><multipleuser>  <group name> = to add multiple users in the group at a time.

Delete users :- 
#groupadd marvels = it  will create a gropu marvels
#cat /etc/group = to see all the groups which is created
#useradd castle = it will create user
 
#cat /etc/group = see the users details in group, the user group which is created they don’t have permission  to add or remote the users in group
#groupmod –ptest marvels = to pretect the group using the password
#gpasswd –A <username> <gropu name> = use to add the users in group and user become the administrator for that group
#gpasswd –d <usernam> <group name> = to remove the users from the group
#groupmod = use to modify the groups
#groupmod –g 1015 marvels = it will change the group id
#groupmod –n <newname> <old group name> = it will change the group name
#userdel <username> = to delete the user but the data will be remain in drive
#userdel –r <username> = it will delete the normal user including files
#userdel –r –f <username> = it will erase everything of that user including user also, it wil not have any details of the particular user.
#groupdel = it will delete the group

User permissiongs –
d – directory
r – read, w- write, x- execute – permission. 1-execute, 2 – write, 4- read
example – drwxr-xr-x = directory, user permission, group permission then other permission. In this example d represent directory, 
#umask – it will show the permission
#chmod = use to change the permission, for example chmod 770 <filename> = it will have user and group full permission but other having nothing
#chmod ugo = u-user, g –group, o- for other, chmode u+x/r/w <filenam> = it gives permission, + user for add permission and – use for revoke permission 
#chmod ugo –rwx <filename> = it will revoke all the permission from the user, group and others
#chmod u+rwx <filename> = give all permission for user
#chmod –R 770 <directory>/ = it will change the file permission of all files in the directory using recursive method.
#chmod 700 <filename> = to change the file permission 
#chrg <root> <filename> = give root permission to file
The files get the permission using umask value. The default value of umask directory is 777 and for files 666. Umask value get while subtracting the u,g and o value of file permission. For example the file having read permission for u, g and o then umask value will be = 666-444 = 222.
#umask = to see the value, you can assign value for umask to create default file permission, for example #umask 0000 then #ttouch afterumaskvalue, #ls –la = it will show rw permission for u,g and o. 

Special Permission –
Acess control list – ACL  - Advanced level permission
	Access control list is used to provide more flexible/granular permission to files and directories.
	Scenario – Provide read and write permission to test/user1 file and to user2 user
	-You should not add user2 to any group
	-Revoke others permission to particular file.
	-User2 user should able to read and write /test/user1.
#ls –ltr = 
#setfacl –m u:<username>:r <filename> = granting an additional user read access
#setfacl –x u:<username> <filename> = it will remove the user entry from the ACL 
#getfacl <directory name> = it will show the user permission for this directory
#setfacl –m u/g/o:<username>:rwx </directory or file name> = it will give a particular user access for that particular user account.
#getfacl /youtube/= see the permission, now the user can create the file and write into that
#su - <username> = to switch to user from one useraccount to other user account
#setfacl –m g:<groupname>:rwx /<directory>/ = it will given rwx permission to group users.
#chmod o-rx /<directoryname>/ = it will revoke the permission 
#setfacl –m u:spiderman:--- /youtube/ = it will revoke the permission from spiderman to access of the youtube directory.
#getfacl <filename1> | setfacl –set-file=- <filename2> = it will copy the ACL of filename1 to filename2
#getfacl –access <oldpermission directory> | setfacl –d –M- /<new direcotry>/ = it will copy the same or replicate the old directory permission to new directory permission.
#setfacl –b <filename> = it will remove all ACL entries from the file
#getfacl <path of old file> | setfacl –set-file=- /<path of new file> = it will give same old directory permission to new directory which is given on new file path.
#cat /etc/profile = to see the umask value and file

Advanced Permission
In u mask there are 4 digit like – 0007, first digit is having the three number, suppose the first digit 7 then permission will be like – 1 – for sticky, 4 – for Suid, 2 – for SGid. If we assign sticky value then the other cannot delete the file accidentally except the file owner.
SGID (2):-  If we assign SGid then whenever a user create a file then it will be shared with other user also. For example there is a finance directory and there are user F1, F2, F3 they work together and having access of directory , if they create any file by F1 or F2 or F3 then it wil be assisnged or shared by other user also of this directory. The UMASK value will be like 4007 – rw-rw---- this will be the file permission
SUID (4) :- if we chage the SU Id then suppose I am a root user but I will give a access to that file to users while assigning SUID, it will give a root user permission.
 
 
#chmod u+s /<filepath> = to apply setuid permission, #chmod 4755 /filepath= it will apply setuid
#chmod g+s /filepath = to apply setgid permission, for example #chmod 2755 /filepath
#chmod +t /filepath = to assign stickybit, chmod 1755 /filepath- it wil apply stickybit

SUDO = substitute user do or supper user do
#/cat /etc/sudoers = it’s having all the user permission, it can’t be edited by users it can be edited by su only.
#cat /etc/sudoers >> /opt/sudoers = copy the sodoers file content to opt folers
#cat /dev/null > /etc/sudoers = making null of sudoers file
#vi sudoers = add the server names etc, create below file and copy the content to /etc/sudoers

#Host Alias
Host_Alias SERVERS = loalhost,<servername>= it can be assigned to any group or user, iits called host alias

#User alias
User_Alias ADMINS = rk, spiderman, user1 = they will be admin groups, it called user alias

#Command alias
Cmnd_Alias CHMOD = /bin/chmod = it’s a command alias
Cmnd_Alias CHOWN = /bin/chown = it’s a command alias
Cmnd_Alias CUSTOM = /sbin/mount, /sbin/fdisk, /sbin/parted = Its called Command Alias, ther user can access this file only if they assign custom permission
Cmnd_Alias ADMINISTRATORS = /sbin/* = it will be executed by admins

#Defaults –
Defaults syslog=auth, insults, syslog_goodpri=alert = it will show if any wrong password or trying do something then it send alerts
Defaults logfile=/var/log/sudo.log 
Defaults  timestamp_timeout=0, log_year, tty_tickets
Defaults mailto=johnhhack39@gmail.com, mail_always, mail_badpass, mail_backups, mail_no_user = it will send email to email if anything goes wrong or tried tologin with bad password

##Allow Users to run any command 
Root ALL=(ALL) ALL
Spiderman ALL=NOPASSWD:ALL = it will not ask password while running command for the spider man user, add sudo before executing any command it will not ask for password
User1 ALL=NOPASSWD: CUSTOM

##Group Names
%marvels ALL =NOPASSWD: CUSTOM
%admins1 ALL =NOPASSWD: ADMINISTRATORS
%dba ALL =NOPASSWD: ADMINISTRATORS !CHMOD, !CHOWN = dba user will not allow to use chmod and chown command

Save it and close
## if any new user joined then no need to go again and again to sudoer file and add it, we can add directly like below, we can create a user directly and add in to those group which is already specified then the user will get the same permission as group having in sudoer file like marvels, admins1, dba etc it’s a group names which is already added in sudoer group
#gropuadd dba
#useradd –u 10010 –d /home/spideran – g dba –G Wheel kumar = the user kumar will get the dba permission 


## NMCLI – Network manager command line Interface
#nmcli device status = it will show all the device conection satatus
#nmcli connection show = it will show the connection 
 
#nmcli connection add type ethernet con-name Home ifname ens33 = a connection profile will be created. Add this device then you can see it while using #nmcli connection show 
#nmcli general status = it will show general status, it will show the connection status only
#nmcli generate logging = it will show logged in protocol
#nmcli device status = it will show how many devices are connected
#nmcli device show <device_name> = it will show the show the status, why it’s not connected and other details like IP gateway etc
#nmcli connection add type Ethernet con-name spiderman ifname ens33 = to make or add the connection
#nmcli connection delete spiderman = to delete the connection 

 

#nmcli connection modify <Network Name> ipv4.address <IP> ipv4.g <gateway> ipv4.dns <dns> +ipv4.dns <dns2add> connection.autoconnect <yes or no> ipv4.method manual
#nmcli connection modify Home ipv4.address 192.168.2.23/24 ipv4.g 192.168.2.2 ipv4.dns 192.168.2.2 +ipv4.dns 4.4.4.4 connection.audoconnect yes ipv4.method manual =  it will modify the connection 
#cat /ect/sysconfig/network-scripts/ifcfg-<connectionname> = you can see this file here with the details which we have modified
#sudo nmcli connection up Home =  it will try to up the Home connection and other connection will get loss. It will change the connection to Home
#nmcli connection show Home = it will show full profile details of Home network
#sudo nmcli connection delete Home = it will delete the connection but before delete you need to inactive the Home connection.
#nmcli –t 0f RUNNING general = it will show connection status
#nmcli –t –f state general = it will show the status whther connected or not
#nmcli device = it will show devices
#nmcli device status = show the satus
#nmcli device monitor = device related information monitor
#sudo nmcli connection down Home = it will make connection down
#sudo nmcli connection up Home = it will make connection up
#ip add = it will show the ip address details.
#nmcli connection modify Home connection.permission users:spiderman = it will give the permission to down and up the Home the connection by spiderman.
#nmtui  = Text Based UI, it’s a GUI based
#nmtui edit Home = it will open home connection in gui to edit, you can edit from here
#sudo nmtui = it will open gui
#sudo nmtui-hostname = it will open hostname directly
#nmtui-connect = to activate or deactivate the network 

##Configuration of Firewall and how it works.
#firewall-config = it will open the firewall graphical user interface, its two type, runtime configuration and permanent configuration. Runtime configuration means when we made a rule then it will be working and once the machine reboot then it will get vanished. Permanent configuration does not get vanished even after reboot. We can do all the setup using GUI
#yum install firewall-config firewalld-filesystem python3-firewall –y
#firewall-config
Firewall-cmd Commands – 
	-systemctl disable iptables
	- systemctl disable ip6tables
	- systemctl stop ipv6tables
	- systemctl stop iptables
	- systemctl mask ip6tables
	- systemctl mask iptables
	- systemctl status iptables
	- systemctl status ip6tables
	- yum install –y firewalld firewall-config
	- systemctl status firewall
	- systemctl enable firewall.service
	- systemctl start firewall.service
	#firewall-cmd –get-default-zone
	#firewall-cmd –set-default-zone=home
	#firewall-cmd –get-default-zone
	#firewall-cmd –get-active-zone
	#firewall-cmd –version
	#firewall-cmd –zone=public –list-iterface
	#firewall-cmd –add-interface=eth0 –zone=public
	#firewall-cmd –remove-interface=eth0 –zone=public
	#firewall-cmd –get-services
	#firewall-cmd –permanent –get-services
	#firewall-cmd –panic-on [Disable incoming and outgoing packets]
##Masquerding – Multi NAT Rule == its like NAT, network address translation.
#firewall-cmd –help = we can setup or configure firewall using the command line
#systemctl status firewalld = it will show the system firewall status
#firewall-cmd –get-default-zone = it will show the default zone
#firewall-cmd –set-default-zone=public ==== it will make the firewall zone default public
#firewall-cmd –get-active-zone = 
#firewall-cmd –version= version of firewall
#firewall-cmd –zone=public –list-interfaces
#firewall-cmd –zone=home –list-interfaces
#firewall-cmd –add-interface=eth0 –zone=home = to add the interface
#firewall-cmd –remove-interface=eth0 –zone=home = it will remove the firewall zone
#firewall-cmd –get-services = it will show the firewall services
#cat /etc/fire
#cat /etc/firewalld/ = it will 
#cat /etc/firewalld/zones/public.xml = it will show the firewall zone where you can change directly


##SELinux Context == Security Enhanced Linux 
1.	Port Level security
2.	Service Level security
3.	File Level security
SElinux having 3 mode
1.	Enforcing mode = enabled 
2.	Permissive mode = not Disabled
3.	Disabled mode = off
#cat /ect/selinux/config = it will show the selinux config file configutation
Enforcing – the policy which ever you have defined that will be enforced, if any user or files comes which is not matching then it will block directly. you can see it here while going to #cat /etc/selinux/config
Permissive mode – its record only the log and does not do anything if anything comes unmatched
Disabled – No SE linux policy is loaded, means there is no permission, user can access any files it will not do anything
#ls –lZ = it will show the context of the object
#cat /etc/selinux/targeted/setrans.conf = it will show all the policy
#getenforce = current status whether it’s enforcing or permissive
#sestatus = it will show full explained status
#setenforce 0 = it will set the selinux to Permissive mode
#setenfoce 1 = it will set the selinux to enforcing 
#ls –ldz /root/ = it will show the context
#ls –ldz /usr= it will show or have different context
#yum install httpd = install httpd
#systemctl start httpd = it wll start httpd
#ls –ldz /var/www/html/ = it will show how we can run the http service
#firewall-cmd –permanent –add-service=http = http service will be added to firewall
#firewall-cmd –permanent –add-service=https = it will add https service
#rewall-cmd –reload = it will re-load the firewall so that it can be started other services.
#cd /var/www/html = go to html directory then create a index.html file, then open the browser and type the IP address it will show the .html file as default, make folder test and see whether you are accessible using ls –ldz test/
#chcon unconfined_u:object_r:etc_t:s0 index.html
#ls –lz index.html
#chcon unconfined_u:object_r:var_t:s0 index.html
#systemctl restart httpd = after running it then refresh the .index file and check, it will not allow to acces or enforcing to stop accessing test folder
#setenforce 0 = it will enable the permissive mode where only you can get the log file but the file will be accessible, to see thelog file jut run #tail –f /var/log/messages = it will show all the log file then try to access the test directory.
#vi /etc/selinux/config = go there and LELINUX and make it disable, then it will disabled after re-start but in current it will be same as older.
#ps –efz = it will show all the enfoced file level and service level
#systemctl status httpd = it will show the service of httpd


## YUM repository – Echo “AppStream | BaseOS | YUM Repository Setup RHEL 8”
# echo “AppStream | BaseOS | YUM Repository Setup RHEL 8”
#mkdir /rpms = create rpms directory and dump all content of DVD repository to rpms, go to #cd /mnt/ then cp –R BaseOS /rpms = it wil copy the baseos then copy #cp –R AppStream /rpms/
#cd /rpms/ = then run ls to see the copied data
#cd /etc/yum.repos.d/ = go to this directory, then run ls and you will see redhat.rep file then create a file #vi AppStream.repo and type below
 	[AppStream]
name=”App Stream Repo”
	baseurl=file:///rpms/AppStream/
	enabled=1
gpgcheck=0
Then copy this file to  #cp AppStream.repo BaseOS.repo
Then edit the BaseOS.repo and type below content
	[BaseOS]
name=”Base OS Repo”
baseurl=file:///rpms/BaseOS/
enabled=1
gpgcheck=0
#cd /rpms/ then run ls then#cat /etc/yum/repos.d/BaseOS.repo and similarly verify once while opening appstraeamrepo
#yum clean all = it will clean then check repo list, #yum repolist = it will give the repo list
#rpm –import RPM-GPG-KEY-redhat-release = Go to mnt directory and run this command to register the repo


NTP (Network Time Protocol) Configuration = use to synchronise the date and time from the server
 
Commands
##NTP server side ##
#dnf install chrony = install the chrony package
#systemctl status chronyd
#systemctl restart chronyd
#systemctl enable chronyd
#vi /etc/chrony.conf = edit the configuration file the save it, type allow <IP address>, it will allow the synchronization from that server.
#systemctl restart chronyd
#firewall-cmd –permanent –add-services=ntp = allow the firewall port
#firewall-cmd –reload
#ntpupdate <NTP server address>

##NTP client side ##
#dnf install chrony
#systemctl enable chronyd
#server <NTP server address>
#systemctl restart chronyd
#chronyc sources; chronyc clients;

RHCSE – NIC Teaming
 
 
 
 
If system having one nic then what if its failed so the services will be timed if they request because they will not get services from the server in this scenario if we add two nic then both IP will be different and our client know only one IP so it will take time to switch from one IP to other IP. To fix this issue NIC Team comes into the picture, we make both IP virtually as a single IP called virtual configuration so that if one is failed then it does not stop the services. These services are called load balance or fail over mechanism or round drop or broadcast mechanism.
#nmcli device status = it will show the devices which is connected with machine, we need to down those connection which we need to add in team so we can down the connection using below command one by one
#nmcli connection down <connection name>
#nmcli connection add type team con-name team0 ifname team0 config ‘{“runner”: {“name”: “activebackup”}}’ = it will create a team0 connection with team feature then modify it using below command.
#nmcli connection modify team0 ipv4.addressess 192.168.2.156/24 ipv4.gateway 192.168.2.2 ipv4.dns 192.168.2.2 connection.autoconnect yes ipv4.method manual = it will assign all the necessary IP to team0 connection then we will add the different NIC into this using below command
#nmcli connection add type team-slave con-name team0-port0 ifname <devicename ex ens37> master team0 = it will make team0 as a master and it will add the connection in this virtual configured team0 connection, similarly we can add another connection while changing the device name and con name. 
#nmcli connection add type team-slave con-name team0-port1 ifname <connection name ex ens38> master team0 = 
#nmcli connection show = it will show the connection 
#nmcli device status = it will be up now
 
#teamdctl team0 status = it will show the team0 status
#nmcl connection down team0-port1 = down team0-port1 down and check it will get ping the ip because the team0-port0 is up.


iSCSI = Internet Small Computer System Interface
 
 
Creating iSCSI Target = 
#fdisk –l = it will show the iSCSI diesk
#fdisk /dev/sdb = create primary disk and create a lvm t, 8e command
#partprobe /dev/sdb = update the partition table
#pvcreate /dev/sdb1 = create pvpart
#vgcreate vg0 /dev/sdb1 = create vg
#lvcreate –l 100%FREE –n lv0 vg0 = it will create lv
#lvs = to see the volumes
#yum install targetcli* = it will install a required tool to convert your disk into iSCSI 
#targetcli = to see the block of the iscsi then create a block using below command after running it />/backstores/block create LUN /dev/vg0/lv0
/> /iscsi create iqn.2018-03.com.techarkit-server:disk1 = after creating it you need to make acl using below command
/>/iscsi/iqn.2018-03.com.techarkit-server:disk1/tpg1/acls create iqn.2018-03.com.arkit-server:node1 = it will create note 1
/>/iscsi/iqn.2018-03.com.techarkit-server:disk1/tpg1/luns create /backstores/block/LUN = it will create lun the we will make portable access using below command
/>/iscsi/iqn.2018-03.com.techarkit-server:disk1/tpg1/portals create 192.168.2.49 = sometime may get error  because the existing portal will be there, to delete the existing portal use below command. 
/>/iscsi/iqn.2018-03.com.techarkit-server:disk1/tpg1/portals delete 0.0.0.0 ip_port 3260 = it will delete the existing portal then you can run and create new portal using above command.
/>saveconfig = it will save the connection what ever we have made so far then exit it using /> exit command or you can verify while typing ls before exit like />ls = it will show the details then you can exit.
#firewall-cmd –list-all = list all the firewall detail
#frewall-cmd –permanent –add-port=3260/tcp
#firewall-cmd –reload = reload it
#systemctl status target.service = it will show the status
#systemctl enable target.service = enable it if its not enable
#systemctl start target.service = If its not started
#systemctl status target.service= to validate the service
#yum install iscsi* = to install the iscsi initiator, preparing to connect LUN
#systemctl start iscsid.service =
#systemctl status iscsid.service= see the status
#iscsiadm –m discovery –t st –p 192.168.43 = see the conection, it may refuse or failed so edit 
#vi /etc/iscsi/initiatorname.iscsi = edit and type as : - InitiatorName=iqn.2018-03.com.techarkit-server:node1 then save and exit from here.
#iscsiadm –m discovery –t st –p 192.168.2.43 = check the conection, if you run then you will get the disc details which you have created.
#iscsiadm –m node –T iqn.2018-03.com.techarkit-server:disk1 –p 192.168.2.43 –l = it will show the logging details
#cat /proc/partitions = it will show all the partition
 

#yum install httpd* = install the webserver and access from the browser, by default the port number will be 80 and if we use ssl then it will be 443.
#systemctl status httpd = 
#systemctl start httpd
#systemctl status httpd
#firewall-cmd –permanent –add-service=http = add the http service in firewall then reload it using beow command
#firewall-cmd --reload
#cd /var/www/html/ 
#vi index.html = to create index page
#mkdir –p /var/www/html/webserver1/
#mkdir –p /var/www/html/webserver2/
#touch  /var/www/html/webserver1/index.html = edit and write some code
#touch  /var/www/html/webserver2/index.html = edit and write some cod
#chmod –R 755 /var/www/html/* = give permission to the files
#vi /etc/httpd/conf.d/webserver1.conf = edit and add the virtual hosting like below, its called virtual configuration file:-
<VertualHost *:80>
ServerAdmin root@localhost.localdomain
ServerName www.webserver1.com
DocumentRoot /var/www/html/webserver1
DirectoryIndex index.html
</VertualHost>
<Directory “/var/www/html/webserver1”>
AllowOverride none
Require all granted
</Directory>
Save and exit then
#httpd –t = to verify it then copy to weserver using below
#cp /etc/httpd/conf.d/webserver1.conf /etc/httpd/conf.d/webserver2.conf = then edit it using vi editor and make below changes.

<VertualHost *:80>
ServerAdmin root@localhost.localdomain
ServerName www.webserver2.com
DocumentRoot /var/www/html/webserver2
DirectoryIndex index.html
</VertualHost>
<Directory “/var/www/html/webserver2”>
AllowOverride none
Require all granted
</Directory>

Save and exit
#systemctl restart httpd.service
#systemctl status httpd.service = after this go to windos and open Hosts file from the pat of C:\Windows\System32\drivers\etc\Hosts.txt and add below two lines
192.168.2.51	www.webserver1.com
192.168.2.51	www.webserver2.com = save it and close it
Now we can access above webpage on windows host machine using above url

#WSGI (Web Server Gateway Interface) application enabled web server
The Web Server Gateway Interface is a simple calling convention for web servers to forward requests to web applications or frameworks written in the Python programming language. It is used to forward requests from a web server (such as Apache or NGINX) to a backend Python web application or framework. From there, responses are then passed back to the webserver to reply to the requestor.
#yum install mod_wsgi = install the wsgi package from this command
#cd /etc/httpd/conf.d = then ls and delete webserver2.conf and webserver1.conf then make beow files
#vi webapp.conf = create this file and write below screept 

<VertualHost *:80>
ServerAdmin root@localhost
ServerName www.wtecharkit.com
WSGIScriptalias / /var/www/html/webapp.wsgi
</VertualHost>

#cd /var/www/html = then create a file with #vi webapp.wsgi
def application(environ, start_response) :
	status = ‘200 OK’
	output = b ’hellow Word!’
	response_headers = [(‘Content-type’, ‘test/plain’),
                           -(‘Content-Length’, str(len(output)))]
	Start_response(status, response_headers)
	Return [output]

#systemctl restart httpd


#SSL Certificate – it will encrypt the data then transfer, it will be not readable form
Web Server Installation – Generate Self-Signed Certificate 

#yum install http* = install the http package 
#yum install mode_ssl = install ssl  package
#systemctl enable httpd =
#systemctl start httpd
#firewall-cmd –permanent –add-service=http
#firewall-cmd –permanent –add-service=https
#firewall-cmd –reload 
#setenforce 0 = enforce selinux
#cd /var/www/html = then create file #vi  index.html, testing website SSL arkit then save this html file
#you can browser this site and check
#cd /etc/httpd/conf.d  = then copy as below
#cp ssl.conf /opt/ = then generate the csr file as below
#sudo openssl req-new > certificate.csr = then create it while selecting
#sudo openssl rsa –in privkey.pem –out keyfile.key
#sudo openssl x509 –in certificate.csr –out cert.cert –req-signkey keyfile.key –days 365
#ls
#mkdri –p /etc/pki/tls/private/
#sudo cp cert.cert /etc/pki/tls/certs/cert.cert
#sudo cp keyfile.key /etc/pki/tls/private/server.key
#cd /etc/httpd/conf.d = then edit the file vim ssl.conf, search for 

DNS = Domain Name System, convert human readable names to system numbers
The DNS convert the name to IP and IP to names, Primary/Master/Slave: a master server reads its zones file s from files on the system’s disk, forwarding, caching, authoritative servers
Forwarding DNS - forwarding server that simply passes all request to another DNS server with recursive capabilities
Caching Servers - it has the advantage of answering recursive requests from the clients
Server that only concerns itself with answering the queries for the zones that it is responsible for .

There are few records type -
	A = Address record
	PTR = Pointer record, reverse lookup
	NS=Name service/Server, naming server or ns server which sent response if we send any request
	MX=mail exchanger
	SOA = State of Authority, verify author or non-authority records
	CNAME = Canonical Name / Alias Name
#cat dns-config = 
#vi dns-config = edit this configuration file and change DNS as bind* then save it
#yum install bind* = to install the DNS server with bind
#systemctl enable named-chroot.service 
# systemctl enable named-service
# systemctl start named-chroot.service 
# systemctl status named-chroot.service
#systemctl status named-service.
#vim /var/named/chroot/etc/named.conf= edit file and add IP address
##vim /var/named/chroot/etc/named.rfc1912.zones = edit and add the configuration update forward and reverse lookup zones 
#cd /var/named/chroot/var/named/ = you can see the zones files here then copy the file using  #cp named.loopback techarkit.local.for.zone  then also copy the #cp named.loopback techarkit.local.rev.zone
#vim techarkit.local.for.zon = edit the forward lookup zone file and add the name at SOA and NS record, A record will have IP address, then edit revers lookup zone same way , update NS and PTR record
#chown root:named techarkit.local.for.zone = change the permission for forward and revers lookup one by one then run below command
#firewall-cmd –permanent –add-service=dns
#  /usr/sbin/named-checkconf –z /etc/named.conf = it will verify the service 
#systemctl restart named.service = verify the service and check in case of any error then verify revers and forward lookup zone
#systemctl sttaus named.service
#ping server.techarkit.local = it will resolve the IP address
#vi /etc/resolv.conf = then add the name server to resolve it
#nslookup server.techarkit.loca  = 

Slave or secondary DNS configuration:- 
#vim /etc/named.conf = 
#systemctl status named =primary DNS need to restart 
Systemctl restart named = 
#yum install bind* -y = install the bind package
#vim /etc/named.conf = edit and add the slave DNS server here
#vim /etc/named.rfc1912.zones = add forward and reverse lookup zone, no need to do manual it will be recursive from the master server IP address
#vim /etc/resolf.conf = edit and add DNS server entry
#systemctl start named = start and check, in case of any errors then verify using below command
# /usr/sbin/named-checkconf –z /etc/named.conf = it will verify
#ll /var/named/slaves/ = the files will be repacked with slave server 
#dig server.techarkit.local= you can see the details 
#dig slave.techarkit.local= you can see the details of slaves
#nslookup jldskjflksjfjfl

#cat dora = 
DORA = Discover – IP address request, Offer – IP address Offer, Request – IP address Selection, Acknowledgment.
#cat dhcp-config = see the file and other details, port number 67
#yum install dhcp*
#yum install dhcp = to install the DHCP package 
#systemctl enable dhcpd.service
#systemctl start dhcpd.service= it will get failed because no configuration done
#cp /usr/share/doc/dhcp-4.2.5/dhcp.conf.example /etc/dhcp/dhcpd.conf= copy the file 
#vim /etc/dhcp/dhcp.conf = edit this configuration file and go to subnet then change the configuration file, like IP address range, provide domain name server IP, domain name, router IP etc the save and exit then re-start it and check the status.
#systemctl restart dhcp.service
#systemctl status dhcp.service = it will run now and you will not get any error if it’s updated properly
Assign permanent IP address using MAC address for that particular server
#ping <server ip>
#arp –a = check the IP table and find the mac of server then go to configuration file and edit it.
#vim /etc/dhcp/dhcpd.conf = copy host configuration then past it and change the Ethernet address then put the fixed IP address, it will take the same IP address whenever it will get re-started it will not change the IP.

How to install and configure the Samba server.
we use to share the files from one system to other we do use samba server, install the samba* package, port will be 445, smb, nmb, /etc/samba/smb.conf
#yum install samba* = to install the samba package
#mount /dev/sr0 /mnt = mount it
#yum install samba* = it will get installed along with dependencies.
#systemctl enable smb
#systemctl enable nmb
#systemctl start smb
#systemctl start nmb
#system ctl status smb
#systemctl status nmb
#firewall-cmd –permanet –add-service=samba= it will add in firewall and allow the firewall to access it permanently.
#firelewall-cmd –reload = reload the firewall
#mkdir /cifshare = create a share folder
#ls –ldZ /cifshare/ = to see the permission 
#semanage fcontext –a –t samba_share_t “/cifshare(/.*)?” = To access subdirectory of this directory
#ls –ldZ /cifshare/
#restorecon –vRF /cifshare/ = smb share will be we can check while using #ls –ldZ /cifshare.
#useradd cifuser1 –s /sbin/nologin = this user will be a samba user so not required to login to our machine using ssh
#smbpasswd –a cifuser1= convert into samba user then give the password
#chown cifuser1: /cifshare = give user permission to access the samba file
#ls –ld /cifshare = to see the permission or ownership of the directory
#pdbedit –L –v = see all the user permission and its details 
#vi /etc/samba/smb.conf = edit the file and go to down and you can write similar conf, give comment and path of the directory which need to share, valid users = cifuser1, etc
#systemctl restart smb
# systemctl restart nmb

SAMBA client site configuration =
#yum install cifs-utils = if we need to access from the client or from the windows or Linux then we need to install the cifs utils package
#mkdri /localcifs = create directory and mount it using
#mount –t cifs –o username=cifuser1 //<server_ip>/name of the share name = it will get mount, give psssword then you can check using df –h
#touch testing123 = test whether its writable or not = permission denied then we need to  give permission 
#chown cifuser1:  /cifshare1/
#chmod 775 /cifshare1/
#systemctl restart smb and nmb services then go to client machine and check whether its permission is given or not
#you can check in server whether its file is created or not.

How to install and configure FTP server = File Transfer Protocol 
#vsftpd is the service and protocol 20 and 21, /etc/vsftpd/vsftpd.conf is configuration file, /var/pub/ftp is the default path where the files are store
#yum install vsftpd* = to install the ftp service
#systemctl enable vsftpd
# systemctl strat vsftpd
#systemctl status vsftpd
#firewall-cmd –permanent –add-service=ftp
# firewall-cmd –permanent –add-port=21/tcp
# firewall-cmd –permanent –add-port=20/tcp
#firewall-cmd –reload
#cd /var/ftp/pub = then ls and create a file touch ftpfile.txt

Go to client side and install ftp service 
#open browser and enter the IP and you can browser this file using ftp://<IP address>
#yum install ftp = to install the ftp 
#ftp <ip> = to login to ftp, username and password will be default ftp

Take daily backup and archive it in a full back then delete these files after taking the backup
#mkdri –p /fullbackup/dailybackup
#cd /fullbackup/dailybackup
#mkdir <date to crete folder>
#mkdir –p /fullbackup/archive
#mv /fullbackup/dailybackup*  /fullbackup/archive
#mkdir /sripts then got o scripts and create a file #vi morethanxday.sh
	#!/bin/bash
	##Delete the directories older then 2 days based on directory name validation 
	Ls –ltr /fullbackup/archive/ | awk ‘{print $9}’ > /scripts/dirs.
	For I in ‘cat /scripts/dirs’; do
	STARTTIME=$(date +%s –d”$i 00:00:00”)
	ENDTIME=$(date +%s)
	echo $(ENDTIME-STARTTIME) | awk ‘{print int($1/60)}’ > /script/value
	COUNT=’cat /scripts/value’
	if [ $COUNT –gt 2880 ]; then
	echo “Directories are oler than 2 days $i” > /scripts/joblog
	rm –rf /fullbackup/archive$i
	fi
Save above file and exit 
#ls –ltr /fullbackup/srchive/ | awk ‘{print $9}’ = it will print all the directory which is older then 2 days
#chmode +x morethanxday.sh
#sh /scripts/morethanxdays.sh
#it will delete all the directory     

#cat userlist= this list has multiple username, you need to create a screep which create al the users, as below = #vim userscript.sh
	#!/bin/bash
	##How to create Multiple Userts
	If [ “$#” = 0  ]; then
	echo “Usage : sh /$PWD/userscript.sh filename”
	else if [ -f “$1” ]; then
		for I in ‘cat $1’; do
		useradd –s /bin/false $i;
		done
	else echo “File $1 not found”
	fi
	fi



MariaDB installation  My SQL                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                   
#yum install mariadb mariadb-client = it will install mariadb or mysql
#systemctl enable mariadb.service
#yum install mariadb* = to install all the MariaDB dependencies along with mariadb
# systemctl enable mariadb.service
# systemctl start mariadb.service
#firewall-cmd –permanent –add-service=mysql
#firewall-cmd –reload
#ss tulnp | grep “mysql” = you can see the mysql
#mysql_secure_installation = set password and remove anonymous user, don’t = do the setting then it will be done and good to go
#mysql –u root –p = login with root
#show databases = it will 
#create database TechArkit = to create data base and exit from there 
#mysql –u root – p = to loging into mysql
#show database then 
#use TechArkit
#show tables = 
#create table Employee (id int(10), name varchar(40), Emp_Id varchar(20), number int(10), mail_id varchar(30)); = it will create a table of employee
#describe table employee = it will show the table with details of variable
#insert into Employee values (“1”, “Raj”, “1234567890”, rk@marvel.local”); = insert data into table
#select * from Employee = to see the data from the table
#update Employee set id=2 where name = “Raj” = it will update the id = 2 

Create user in Mariadb & Grant Permissions = Process to create user
#create user raj@’%’ Identified by ‘password’; = % show the local user, it will create a user for mariadb
#grant select, update, delete, insert on TechArkit. * to raj@’%’= it will give permission to raj user 

To restrict the user using below, you need to install squid package, squid, 3128-port, /etc/squid/squid.conf 
#yum  install squid* = it will install thhe package
#systemctl enable squid
#systemctl status squid
#firewall-cmd –permanent –add-port=3128/tcp = allow the firewall
#firewall-cmd –reload
#vim /etc/squid/squid.conf = edit the file and give permission or restrict it, add the bad sites then make a new file of bad sites which you wants to block using below command
#vim /etc/squid/badsites = add the bad site and enter the url like .facebook.com, .youtube.com, then save and exit it
#systemctl restart squid = re-start the service then go to client and set the proxy on browser of server ip so that it can be access only un_restricted site
#tail –f /var/log/squid/access.log = it will generate the log of the user what they are browsing
#vim /etc/squid/blockfiles.acl = create a blockfiles and it will block the .extension files like .mp4, .mp3 .exe etc, you can enable the work hrs of Internet acess using acl work hours 09:00 – 19:00

To install the same configuration of OS for many systems 100 of system so if we do manually then its configuration will vary and it will take a lot of time so we can configure on server and define the packages which package should install and we can give the permission according to that. To enable this service we need to install httpd*
#yum install httpd*
#yum install system-config-kickstart = install this package also where we will define the rule for installation of packages
#system-config-kickstart = it will start the kickstart gui where you need to select all the option for the machine configuration, need to select standard partition not lvm. Partition type should be ext4 then give size etc, the size will be in mb then save this file in default root as ks.cfg it’s called kickstart file. The default configuration file will be generated then you need to dump this file to the default httpd service
#systemctl start httpd
# systemctl status httpd
#sestatus = 
#disable the se linux 
#firewall-cmd –permanent –add-service=httpd
#firewall-cmd –permanent –add-service=https
#firewall-cmd –reload
#cp –Rv /mnt/* /var/www/html/dvd = it will copy entire content of the drive 
#cp ks.cfg /var/www/html/dvd/ = copy the cfg gile

Now create new virtual machine and do default configuration then map the ISO file  then start the machine but don’t install the OS, please press esc at place of installation and type linux http://<IP of Server>/dvd/ks.cfg = give this path so that the machine can access and install the OS with given configuration then hit enter it will load the ks.cfg file it will install the same configuration as we saved in the file, no need to do anything it will install automatically from the file.

Shell Scripting Language –
 
#cat /etc/shells – we can see all the shell command
There are six types of sheel
	-sh
	-csh
	-ksh
	-bash
	-tcsh – use by developer to develop the apps using C language
	-zsh - use by developer to develop the apps using C language
First program in scripting language –
#!/bin/bash
##first program in sheel
mkdir scriptestdirecotry
touch /scriptestdirecotry/test1.txt
echo “I am writing from the shell scrip into the test1.txt file”
save and exit it then execute on terminal.
 
#!/bin/bash
echo “enter the number below ten : \c”
read –r value = it will read the value which is given and store in value variable
if [ $value –le 10 ]; then = -le use for less than 
echo “You provided value is $value” = it will print the provided value

##Greater Then 

#!/bin/bash
Var=16
If [ $var –gt 10 ]
then
	echo “Value is greater than 10”
fi


##Less Then
#!/bin/bash
Var=5
If [ $var –lt 10 ]
Then
	Echo “Value is less then 10”
Fi


## Logical AND in Conditional Statement
#!/bin/bash
Var=5
If [[ $var -gt 4 ]] && [[ $var –lt 10 ]];
	Echo “the Value is greater then 4 and less then 10’
Fi



## Logical OR in Conditional Statement
#!/bin/bash
Var=5
If [[ $var -gt 4 ]] || [[ $var –lt 10 ]];
	Echo “The value is less then 10 or greater then 4 or both condition tru”
Fi


## if Elif else Conditional Statement
#!/bin/bash
Marks=65
If [ $marks –ge 90 ]
Then
	Echo “Them arks is greater then 90, its execelent”
Elif [$marks –ge 60 ]
then
	Echo “its greater then 60 and lower then 90, its good”
Elif [ $marks –ge 50 ]
then
	Echo “Just satisfactor”
Else 
	Echo “you are failed”
Fi

## Nesting if condition
#!/bin/bash
Var=6
If [ “$var”  -gt 1]
Then
	If [ “$var” –lt 10 ]
	Then 
		Echo “the number lies between 1 to 10”
	Fi
fi	

## Equal(=) and double equal(==) operator
#!/bin/bash
Var1=”Hello”
Var2=’World’
If [ $var1 = $var2]
Then
	If [ $var1 = $var2]
	Then
		Echo “both equal and double equal operator are same”
	Fi
Else
Echo “both equal and double equal operator are not same”
Fi

## Test Not Equal To (!=)
#!/bin/bash
If [ $var != 10 ]
Then
	Echo “the value is not equal to 10”

Fi

## Test Two string Before or After Alphabetically
#!/bin/bash
Var1=’World’
Var2=’World’
If [ $var1 == $var2]
Then
	Echo “Both string are same alphabetically”
Else
Echo “Both string are not same alphabetically”
Fi

##Test String is Null
Var=’ ’
If [ $var = ‘ ’ ]
Then
	Echo “the string is null”
Fi

##Test String is not Null
Var=’Hello ’
If [ $var = ‘ ’ ]
Then
	Echo “the string is null”
Else
	Echo “the string is not null”
Fi

## Test Numerical Compare greater then, less then
Same use && or || to compare with –gt, -lt
&& - And operator
|| - Or Operator
-gt – greater then
-lt – less then
<= - less then or equal to
>= - greater then or equal to
= - to assign value
== - compare value

## Test File Exists
#!/bin/bsh
FILE=file.txt
If [-f  “$FILE” ]
Then
	Echo “$file exists”
Else
	Echo “file does not exists”
fi

##Test File is Not Zero Size
If [ -s “$FILE” ]
Then
	Echo “file is not a zero size”
Else
	Echo “File is zero size”


## Test File is a directory or not
PATH=dir
If [[ -d $PATH ]]
Then
	Echo “$PATH is a directory not a file”
Else
	Echo “it’s not valid”
Fi

-L = use for symbolic link
-d = use for Directory
-s = use for file size
-r = check read permission of file
-w = check write permission of the file
-x = to check execute permission

## Case Conditional Statement with Numbers
#!/bin/bash
Var=10
Case $var in
	10)
		Echo “its 10”
		;;
	20)
		Echo “its 20”
		;;
	*)
		Echo “number is something else or undefined”
		;;
esac

## Case Conditional Statement with Strings
#!/bin/bash
Car=”BMW”
Case $Car in
	TOyota)
		Echo “its toyota”
		;;
	BMW)
		Echo “its BMW
		;;
	*)
		Echo “hmm, seems like some other kar”
		;;
esac

## Case Conditional Statement with Wild card
#!/bin/bash
Var=80
Case $var in
	10)
		Echo “its 10”
		;;
	20)
		Echo “its 20”
		;;
	*)
		Echo “number is something else or undefined”
		;;
esac


## Execute a Command With Backticks
#!/bin/bash
Chown linuxhint \dir  ##linuxhint is a file or directory owner or user

## Open the file content
Var=$(cat file.txt)
Echo  “$var”

Echo “$var” > output.txt ## it will create a output.txt file and save the output in that. Its called capture the standard output
Echo “$var” > stderror.txt ## standard error

## Return code
#!/bin/bash
Var=$(cat file.txt)
Echo “$var”
Echo $? > returncode.txt 

##eval command
#!/bin/bas
Eval echo “Hellow World” 

For Loop concept –
for server in ‘cat /script/servers’
do  = opening the far loop
	ping –c 1 $server > /temp/pingress.txt
valid=’echo $?’ = $? Represent share the exit code of the program, if exit code 0 then the program executed properly or its up and if its 1 then it’s not executed or its down.
if [ $valid –eq 0 ]; then
	echo “$server IP UP”
else
	echo “$server is down”
fi
done = closing the for loop


## For loop
For I in 1 2 3 4 5 6 7 8; do
	Echo “This is the value: $i”
Done


## For loop on range or number
For I in { 10..20 }; do ## It wil pring 10-20
If (( $i<=5 )); then
	Echo “$i”
Else
	Break
Fi
done

## Continue in For loop
For I in {1..10}; do
If (( $i==5 )); then
	Continue
Else
	Echo $i
Fi
done


##while loop
While(( ++I <= 5 )); do
	Echo “counter is at $i”
Done

## Until Loop based on File size
## Array 
Car=(‘BMW’ ‘Toyota’ ‘Mercedes’ ‘Honda’)
For I in “${car[@]}”; do
Echo “$i”
Done

## Print lines on file
File=’file.txt’
N=1
While read line; do
	Echo “Line $n : $line”
	N=$((n+1))
Done < $FILE

## Take Input from User
echo “Please enter 3 words followed by Enter :”
read first middle final
echo “Hellow $first $middle $final”

## Take input into array and print it
echo “Give input to enter into aray :”
read –a arrayvar
echo “the given input array member are as follows : ”
for I in ${arrayvar[@]}; do
	Echo “$i”
done

## Print word of the line
line = “Hi This is a Linux shell scripting language”
for word in $line; do
	Echo “$word”
done


Chronetabs = use to execute the command on specific date and time, its organized as below ss

 
#chrontab –e = -e for edit the chrontab and type one * for every minute, two * for hour, three * for day of the month etc then write the command which you wants to execute
 
Save this file and exit it

RPM vs YUM
RPM – Re Hat Package Manager. Developed in 1997.
YUM – Yellowdog Updater Module. Developed in 2000
Bash-completion-2.7-5.el8.noarch
 
 
 

Container – 
A container is a form of OS virtualization. A single container might be used to run anything from a small micro service of software process to a larger application 
RHEL 8 provides tools (Podman, Buildah, Skopeo and Runc) to work with containers within single-server.
Containers run daemon-less and rootless.
Core Technologies of Container –
Control Groups (cgroups) for resource management
Namespaces for process isolation
SELinux for security
Secure multi-tenancy 
Podman – it is a daemonless container engine for developing, managing and running OCI containers on your Linux system. Containers can either be run as root or in rootless mode.
Buildah – For building, pushin and singning container images
Skopeo – for copying, inspecting, deleting and signing images
Runc -  for providing container run and build features to Podman and Buildah.

Installation, Find and Retrieve Containers Images – 
yum module install container-tools
yum install slirp4netns podman podman-docker –y
podman searc centos
podman pull centos:latest
podman images
podman inspect a268rhgkeubd
podman run centos-working
podman run –it centos-workinng /bin/bash

#yum module install container-tools  -y = install the container module
#yum install slirp4netns podman podman-docker –y = install docker
#useradd <username> = create user
#ssh <username> 
#podman search centos = you can see the centos and docker images, you can pull that images.
#podman pull centos:latest = it will pull the centos latest version of centos images
#podman images= you can see that pulled iimage details
#podman inspect <latest image id > = you can find the id using podman images, then you can see the image 
#podman images
#podman run <image id> = to run the image
#podman images = you can see the details
#podman run –rm centos:lstest cat /etc/redhat-release = run the command in redhat-releas then remove the program. It’s another method to run and exit it
#podman run –name=techarkit –it Ubuntu:latest /bin/bash = it will pull the Ubuntu image and run the bin/bash
#cat /etc/os-release= you can see the image details 
#podman ps = it will show the process but its daemonless so you can not see the any process running here 
#ssh ravi@localhost = login 
#podman ps=
#podman run –d httpd = to run the httpd service
#podman images = it will show all the images which you have pulled as of now

Buildah – building, pushing and signing container images
The buildah package provides a command line tool that can be used to
	Create a working container, either from the scratch or using an image as a starting point
	Create an image, either from a working container or via the instructions in a Docker file
	Images can be built in either the OCI image format or the traditional upstream Docker image format 
	Mount a working container’s root file system for manipulation
	Unmount a working container’s root file system for manipulation
	Unmount a working container’s root file system
	Use the updated contents of a container’s root file system as a file system layer to create a new image
	Delete a working container or an image
	Rename a local container 
Building container image using Buildah – 
	buildah from centos
	buildah images
	buildah containers
	curl –sSL https://ftp.gnu.org/gnu/hello/hello-2.10.tar.gz -o hello-2.10.tar.gz
	buildah copy centos-working-container hello-2.10.tar.gz /tmp/
	buildah copy centos-working-container yum install –y tar gcc make
	buildah copy centos-working-container yum clean all
	buildah copy centos-working-container tar xvzf /tmp/hello-2.10.tar.gz –C /opt
	buildah copy centos-working-container /opt/hello-2.10 centos-working-container
	buildah copy centos-working-container ./configure
	buildah copy centos-working-container make
	buildah copy centos-working-container make install
	buildah copy centos-working-container hello –v
	buildah config –entrypoint /usr/local/bin/hello centos-working-container
	buildah comit –format docker centos-working-container firstbuildah:latest
	buildah image
	podman save –o mybuild1.tar localhost/hello2latest
	podman imi 638d3f915ea2 –f
	podman load –I mybuild1.tar
#buildah from centos = it will copy and build the iage
#buildah imags= to see the images
#buildah container = see the container 
#curl –sSL ,,,,,…. = download the hellow application then see using ls
#buildah copy <container name> <hellowfile name> /tmp = copy the hello application
#buildah run <container name> yum install –y tar gcc make= install the images of hello application
#buildah <container name> yum clean all = it will remove the mkh files 
#buildah run <container name>  tar  xvzf /tmp/hello-2.10.tar.gz –c /opt = hello application extracted 
#buildah config –workingdir /opt/hello-2.10 centos-working-container = set the working path 
#buildah run centos-working-container ./configure = compel the package and install other there
#buildah run centos-working-container make =  it will make
#buildah run centos-working-container make install = it will install
#buildah run centos-working-container hello –v = to test whether its working or not
#buildah config –entypoint /usr/local/bin/hello <container> = set entry point for container
#buildah commit –format docker centos-working-conntainer myfirstbuild:latest = latest on local server
#buildah images= we can see all the images here
#podman save –o <image name> <repository name> = it will set the image, you can see using ls
#podman rmi <image id> -f= delete all the images
#buildah images = we can see the image
#podman load –i <image name> = to load the images 
#buildah images
#buildah containers 

Second method to building a buildah image using Dockerfile
#vi Dockerfile = to create a docker file
FROM centos:latest
LABEL Author Raj Kumar
RUN yum install –y tar gcc gzip make && yum clean all
ADD https://ftp.gnu.org/gnu/hello/hello-2.10.tar.gz /tmp/hello-1.10.tar.gz
RUN tar xvzf /tmp/hellow-2.10.tar.gz –c /opt
WORKDIR /opt/hello-2.10
RUN ./configure
RUN ./configure
RUN make
RUN make install
RUN hello –v
ENTRYPOINT “/usr/local/bin/hello”
Save it then exit from here
#buildah bud –t dockerhello .= run the Docker file and create a image
#buildah images = you can see the images will be added dockerhello
#buildah from dockerhello = 
#buildah containers 
#podman volume create volume1 = to create volume
#podman volume ls = to see the volume
#podman volume inspect volume1 = to see in details 
#podman run –it –v volume1:/newvol –name newcontainer centos:latest = attache the volume to container 
#df –h
#cd /newvol
#mkdir testing
#touch test
#echo “container” >> test
#exit = exit from the container
#ls 
#podman cp hellow-2.10.tar.gz newcontainer:/newvol = copy the file to new volue
#podman exec <container name> ls –l /newvol = execute and see wheter we have the file at that location or not
#padman restart <container name> = to restart the container
#podman exec <container name> ls –l /newvol 
#podman ps = to see the container is running or not
#podman stop <container name> = to stop
#podman rm <container name> = to remove it

AWK command in Unix/Linux with examples
•	Difficulty Level : Easy
•	Last Updated : 07 Sep, 2021
Awk is a scripting language used for manipulating data and generating reports. The awk command programming language requires no compiling and allows the user to use variables, numeric functions, string functions, and logical operators. 
Awk is a utility that enables a programmer to write tiny but effective programs in the form of statements that define text patterns that are to be searched for in each line of a document and the action that is to be taken when a match is found within a line. Awk is mostly used for pattern scanning and processing. It searches one or more files to see if they contain lines that matches with the specified patterns and then perform the associated actions. 
Awk is abbreviated from the names of the developers – Aho, Weinberger, and Kernighan. 
WHAT CAN WE DO WITH AWK? 
1. AWK Operations: 
(a) Scans a file line by line 
(b) Splits each input line into fields 
(c) Compares input line/fields to pattern 
(d) Performs action(s) on matched lines 



2. Useful For: 
(a) Transform data files 
(b) Produce formatted reports 
3. Programming Constructs: 
(a) Format output lines 
(b) Arithmetic and string operations 
(c) Conditionals and loops 
Syntax:
awk options 'selection _criteria {action }' input-file > output-file
Options:  
-f program-file : Reads the AWK program source from the file 
                  program-file, instead of from the 
                  first command line argument.
-F fs            : Use fs for the input field separator
Sample Commands 
Example: 
Consider the following text file as the input file for all cases below: 
$cat > employee.txt 
ajay manager account 45000
sunil clerk account 25000
varun manager sales 50000
amit manager account 47000
tarun peon sales 15000
deepak clerk sales 23000
sunil peon sales 13000
satvik director purchase 80000 
1. Default behavior of Awk: By default Awk prints every line of data from the specified file.  



$ awk '{print}' employee.txt
Output:  
ajay manager account 45000
sunil clerk account 25000
varun manager sales 50000
amit manager account 47000
tarun peon sales 15000
deepak clerk sales 23000
sunil peon sales 13000
satvik director purchase 80000 
In the above example, no pattern is given. So the actions are applicable to all the lines. Action print without any argument prints the whole line by default, so it prints all the lines of the file without failure. 
2. Print the lines which match the given pattern. 
$ awk '/manager/ {print}' employee.txt 
Output:  
ajay manager account 45000
varun manager sales 50000
amit manager account 47000 
In the above example, the awk command prints all the line which matches with the ‘manager’. 
3. Splitting a Line Into Fields : For each record i.e line, the awk command splits the record delimited by whitespace character by default and stores it in the $n variables. If the line has 4 words, it will be stored in $1, $2, $3 and $4 respectively. Also, $0 represents the whole line.  
$ awk '{print $1,$4}' employee.txt 
Output:  
ajay 45000
sunil 25000
varun 50000
amit 47000
tarun 15000
deepak 23000
sunil 13000
satvik 80000 
In the above example, $1 and $4 represents Name and Salary fields respectively. 
Built-In Variables In Awk
Awk’s built-in variables include the field variables—$1, $2, $3, and so on ($0 is the entire line) — that break a line of text into individual words or pieces called fields. 



•	NR: NR command keeps a current count of the number of input records. Remember that records are usually lines. Awk command performs the pattern/action statements once for each record in a file. 
•	NF: NF command keeps a count of the number of fields within the current input record. 
•	FS: FS command contains the field separator character which is used to divide fields on the input line. The default is “white space”, meaning space and tab characters. FS can be reassigned to another character (typically in BEGIN) to change the field separator. 
•	RS: RS command stores the current record separator character. Since, by default, an input line is the input record, the default record separator character is a newline. 
•	OFS: OFS command stores the output field separator, which separates the fields when Awk prints them. The default is a blank space. Whenever print has several parameters separated with commas, it will print the value of OFS in between each parameter. 
•	ORS: ORS command stores the output record separator, which separates the output lines when Awk prints them. The default is a newline character. print automatically outputs the contents of ORS at the end of whatever it is given to print. 
Examples: 
Use of NR built-in variables (Display Line Number)  
$ awk '{print NR,$0}' employee.txt 
Output:  
1 ajay manager account 45000
2 sunil clerk account 25000
3 varun manager sales 50000
4 amit manager account 47000
5 tarun peon sales 15000
6 deepak clerk sales 23000
7 sunil peon sales 13000
8 satvik director purchase 80000 
In the above example, the awk command with NR prints all the lines along with the line number. 
Use of NF built-in variables (Display Last Field)  
$ awk '{print $1,$NF}' employee.txt 
Output:  
ajay 45000
sunil 25000
varun 50000
amit 47000
tarun 15000
deepak 23000
sunil 13000
satvik 80000 
In the above example $1 represents Name and $NF represents Salary. We can get the Salary using $NF , where $NF represents last field. 
Another use of NR built-in variables (Display Line From 3 to 6)  
$ awk 'NR==3, NR==6 {print NR,$0}' employee.txt 
Output:  
3 varun manager sales 50000
4 amit manager account 47000
5 tarun peon sales 15000
6 deepak clerk sales 23000 
More Examples



For the given text file:  
$cat > geeksforgeeks.txt

A    B    C
Tarun    A12    1
Man    B6    2
Praveen    M42    3
1) To print the first item along with the row number(NR) separated with ” – “ from each line in geeksforgeeks.txt:  
$ awk '{print NR "- " $1 }' geeksforgeeks.txt 
1 - A
2 - Tarun
3 – Manav    
4 - Praveen
2) To return the second row/item from geeksforgeeks.txt: 
The question should be:- To return the second column/item from geeksforgeeks.txt:
$ awk '{print $2}' geeksforgeeks.txt 
A12
B6
M42
3) To print any non empty line if present  
$ awk 'NF < 0' geeksforgeeks.txt
here NF should be 0 not less than and the user have to print the line number also:
correct answer : awk ‘NF == 0 {print NR}’  geeksforgeeks.txt
OR 
awk ‘NF <= 0 {print NR}’  geeksforgeeks.txt
0
4) To find the length of the longest line present in the file:  
$ awk '{ if (length($0) > max) max = length($0) } END { print max }' geeksforgeeks.txt
13
5) To count the lines in a file:  
$ awk 'END { print NR }' geeksforgeeks.txt 
3
6) Printing lines with more than 10 characters:  
$ awk 'length($0) > 10' geeksforgeeks.txt 
Tarun    A12    1
Praveen    M42    3
7) To find/check for any string in any specific column:  
$ awk '{ if($3 == "B6") print $0;}' geeksforgeeks.txt
8) To print the squares of first numbers from 1 to n say 6:  
$ awk 'BEGIN { for(i=1;i<=6;i++) print "square of", i, "is",i*i; }' 
square of 1 is 1
square of 2 is 4
square of 3 is 9
square of 4 is 16
square of 5 is 25
square of 6 is 36
This article is contributed by Anshika Goyal and Praveen Negi. If you like GeeksforGeeks and would like to contribute, you can also write an article using write.geeksforgeeks.org or mail your article to review-team@geeksforgeeks.org. See your article appearing on the GeeksforGeeks main page and help other Geeks. 
Please write comments if you find anything incorrect, or you want to share more information about the topic discussed above.
