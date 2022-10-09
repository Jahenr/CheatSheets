Linux/Unix:

	#List files and Directories.
		ls
			#Options include.
				-l = List
				-h = Human readable file/directory size
				-a = Show hidden files/directories
	
	#Change Directory
	    cd <pathname>
	    
	#Print ASCII character strings in large letters
		banner <text>

	#List running processes
		ps

	#Create a new directory
		mkdir <directory name to be created>
	
	#Print the working directory
		pwd
		
	#Recursively search for a file or directory
		find <file or directory name>
	
	#View full contents of file in terminal
		cat <filename>
		
	#Copy a file
		cp <original filename> <copy filename>
		
	#Move or rename a file
		mv <original file> <new location or name>

	#Run previous command as sudo.
		sudo !!

	#Display history file in terminal
		history

	#Run command with history ID <id>
		!<id>

	#Run last command via command name
		!<command name>

	#Search man pages with given keyword
		apropos <keyword>

	#Use stdout as an argument
		xargs

	#Show information of file
		file <filename>

	#Reverse search of history
		ctrl + r <command>
			Tip: Press ctrl + r to cycle to the next command etc

	#Show current user
		whoami

	#Show logged in user with  what process they are running etc
		w

	#Show logged in user
		who

	#Pause current session
		ctrl + z

	#Show current paused sessions
		jobs

	#Resume paused session
		fg

	#Send paused session to background
		bg
		
	#Show network interface information
		ifconfig
		
	#Show drive usage information
		df
		
	#Show memory usage information
		free
		
	#Ping a given IP or domain
		ping <ip or domain>
		
	#Open an SSH session with a given user and machine
		ssh <user>@<machine IP or domain>
		
	#Close an active SSH session or exit the terminal
		exit
		
	#Show logs of specified service
		journalctl -u <service name>

	#Show logs of specified process ID
		journalctl _PID=<process id>
		
	#Show all installed services
		systemctl list-unit-files --type=service
    
	#Terminate process 
		kill <process id>

	#Create a file
		touch <filename>

	#Print the first 10 lines of a file to standard output
		head <filename>
			#Options include
				-n [NUM] = Print the first NUM lines instead of 10
				-n -[NUM] = Print all but the last NUM lines of a file
        
	#Print the last 10 lines of a file to standard output
		tail <filename>

			#Options include
				-n [NUM] = Print the last [NUM] lines instead of 10
				-n +[NUM] = Print all lines starting with [NUM] until EOF
				
	#Check the current system clock time
		timedatectl
	        	#Options include
				set-time "yyyy-MM-dd hh:mm:ss" = Set the local time of the system clock directly
	  		        list-timezones = available timezones
				set-timezone timezone = Set the system timezone
				set-ntp on = Enable Network Time Protocol (NTP) synchronization
       
	#View Date on terminal 
		date

	#Change the permissions granted
		chmod

	#change a file's ownership
		chown
	
	#change the apparent root directory for the current running process and its children
		chroot

	#Edit file using vi
		vi <file name>
	
	#Edit file using nano
		nano <file name>
	
	#Displays active TCP connections, ports
		netstat -tulpn
	
	#Download from terminal
		wget <url>

	#unzip a file
		unzip <filename>
	
	#mount a drive
		mount <drive name> <mount point>

	#unmount a drive
		umount <drive name>
	
	#Switch to users
		su <username>
	
	#Switch to root
		sudo su
	
	#Find the location of source/binary file
		whereis <file name>

	#Manipulation of partition tables
		fdisk 
	
	#Install, build, remove and manage Debian packages
		dpkg

	#Install, build, remove and manage Debian packages
		apt-get
	
	#Creates a new user account
		adduser
	
	#Creates a new group
		groupadd 

	#Adds a user to a group
		usermod
	
	#Remove a user from a group
		userdel

	#Change password of user
		passwd
	
	#Check md5sum of file
		md5sum <filename>

	#Check sha1sum of file
		sha1sum <filename>

	#Prints the name of the terminal
		tty

	#Ftp on a remote host
		ftp <host>

	#Dns lookup 
		nslookup <host>

	#Show domain information
		host <host>

	#Show detailed domain information
		dig <host>
	
	#View sttrings in a file
		strings <filename>

	#View file type
		file <filename>

	#Details on all Active Processes
		top
    
  	#Determine system boot-up performance statistics
    		systemd-analyze

  	#find the files by name
		locate <filename>



**Basics Linux Commands**

#Lists all files and directories in the present working directory
             ls 

#Lists files in sub-directories as well  
 ls -R

#Lists hidden files as well    
ls -a 

#Lists files and directories with detailed information like permissions,size, owner, etc.  
ls -al 

#Navigate to HOME directory  
 cd or cd ~ 

#Move one level #  
cd ..

#To change to a particular directory   
  cd*

#Move to the root directory  
 cd /

#Creates a new file  
  cat > filename

#Displays the file content  
 cat filename

#Joins two files (file1, file2) and stores the output in a new file (file3)  
cat file1 file2 > file3

#Moves the files to the new location  
 mv file "new file path"

#Renames the file to a new filename  
mv filename new_file_name

#Allows regular users to run programs with the security privileges of the superuser or root  
sudo

#Deletes a file  
  rm filename

#Gives help information on a command  
man

#Gives a list of all past commands typed in the current terminal session  
 history 

#Clears the terminal 
clear

#Creates a new directory in the present working directory or a at the specified path 
	mkdir directoryname

#Deletes a directory 
rmdir

#Renames a directory 
 mv

#Divides the file into x columns 
pr -x 

#Assigns a header to the file 
pr -h 

#Denotes the file with Line Numbers 
pr -n 

#Prints “c” copies of the File 
vlp -nc , lpr c

#Specifies name of the printer 
  lp-d lp-P 
 
#Command used to install and update packages 
 apt-get 

#Command to send email
   mail -s 'subject'
          -c 'cc-address'
          -b 'bcc-address'
          'to-address'
	
#Command to send email with attachment 
    mail -s "Subject"
                to-address < Filename
	
	
	
**File Permission commands**


#to show file typ*e and access permission 
  ls -l 

#read permission 
    r 

#write permission 
  w 

#execute permission 
  x 

#no permission 
   -=

#For changing the ownership of a file/directory 
  Chown user

#change the user as well as group for a file or directory 
     Chown user:group filename 


**Environment Variables command**


#To display value of a variable 
echo $VARIABLE 

#Displays all environment variables 
env 

#Create a new variable 
VARIABLE_NAME= variable_value 

#Remove a variable 
Unset

#To set value of an environment variable#export Variable=value 
 export Variable=value

**User management commands of linux**
 
#To add a new user 
sudo adduser username

#To change the password of a user 
 sudo passwd -l 'username'

#To remove a newly created user 
 sudo userdel -r 'username'

#To add a user to a group 
sudo usermod -a -G GROUPNAME USERNAME

#To remove a user from a group 
 sudo deluser USER GROUPNAME 

#hows information of all the users logged in 
  finger 

#Gives information of a particular user 
 finger username


**Networking command**

#login into a remote Linux machine using SSH 
 SSH username@ip-address or hostname 

#To ping and Analyzing network and host connections 
Ping hostname="" or ="" 

#Display files in the current directory of a remote compute 
 dir

#change directory to “dirname” on a remote computer 
 cd "dirname" 

#upload ‘file’ from local to remote computer 
 put file 

#Download ‘file’ from remote to local computer 
 get file 

#Logout 
quit 	

**Process command**

#To send a process to the background# 
bg

#To run a stopped process in the foreground# 
fg

#Details on all Active Processes# 
top 

#Give the status of processes running for a user# 
 ps 	

#Gives the status of a particular process# 
 ps PID 

#Gives the Process ID (PID) of a process# 
pidof

#Kills a process# 
kill PID 

#Starts a process with a given priority# 
nice

#Changes priority of an already running process# 
renice

#Gives free hard disk space on your system# 
 df 

#Gives free RAM on your system# 
 free

**VI Editing Commands**

#Insert at cursor (goes into insert mode) 
 i

#Write after cursor (goes into insert mode) 
 a 

#Write at the end of line (goes into insert mode) 
A 

#Terminate insert mode 
ESC 

#Undo last change 
u

#Undo all changes to the entire line 
 U

#Open a new line (goes into insert mode) 
o
 
#Delete line 
dd 

#Delete 3 lines 
 3dd 

#Delete contents of line after the cursor 
D 

#Delete contents of a line after the cursor and insert new text. Press ESC key to end insertion. 
 C 

#Delete word 
dw 

#Delete 4 words 
4dw 

#Change word 
cw 

#Delete character at the cursor 
  x

#Replace character 
 r 

#Overwrite characters from cursor onward 
R 

#Substitute one character under cursor continue to insert 
 s 

#Substitute entire line and begin to insert at the beginning of the line 
 S 

#Change case of individual character 
  ~ 


**Hope this Linux reference guide helps you**
