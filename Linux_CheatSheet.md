Linux/Unix:

	#List files and Directories.
		ls
			#Options include.
				-l = List
				-h = Human readable file/directory size
				-a = Show hidden files/directories
	
	#Change Directory
	    cd <pathname>

	#List running processes
		ps
	
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


*###Basic Linux commands###*


'''**Command        -       Description**''' 



*ls* 	  **Lists all files and directories in the present working directory**  

*ls -R*   **Lists files in sub-directories as well**  

*ls -a* 	**Lists hidden files as well**  

*ls -al* 	**Lists files and directories with detailed information like permissions,size, owner, etc.**

*cd or cd ~* 	**Navigate to HOME directory**

*cd ..* 	**Move one level up**

*cd* 	**To change to a particular directory** 

*cd /* 	**Move to the root directory**

*cat > filename* 	**Creates a new file**

*cat filename* 	**Displays the file content**

*cat file1 file2 > file3* 	**Joins two files (file1, file2) and stores the output in a new file (file3)**

*mv file "new file path"* 	**Moves the files to the new location**

*mv filename new_file_name* 	**Renames the file to a new filename**

*sudo* 	**Allows regular users to run programs with the security privileges of the superuser or root**

*rm filename* 	**Deletes a file**

*man* 	**Gives help information on a command**

*history* 	**Gives a list of all past commands typed in the current terminal session**

*clear* 	**Clears the terminal**

*mkdir directoryname* 	**Creates a new directory in the present working directory or a at the specified path**

*rmdir* 	**Deletes a directory**

*mv* 	**Renames a directory**

*pr -x* 	**Divides the file into x columns**

*pr -h* 	**Assigns a header to the file**

*pr -n* 	**Denotes the file with Line Numbersv**

*vlp -nc , lpr c*	**Prints “c” copies of the File**

 *lp-d lp-P*         **Specifies name of the printer**
 
*apt-get*        **Command used to install and update packages**

*mail -s 'subject'*
*-c 'cc-address'*
*-b 'bcc-address'*
*'to-address'*
	**Command to send email**
	
*mail -s "Subject"
*to-address < Filename*
	**Command to send email with attachment**
	
	
*###File Permission commands###*


'''**Command        -       Description**''' 




*ls -l* 	**to show file typ*e and access permission**

*r* 	**read permission**

*w* 	**write permission**

*x* 	**execute permission**

*-=* 	**no permission**

*Chown user* 	**For changing the ownership of a file/directory**

*Chown user:group filename* 	**change the user as well as group for a file or directory**


*###Environment Variables command###*


'''**Command        -       Description**''' 




*echo $VARIABLE* 	**To display value of a variable**

*env* 	**Displays all environment variables**

*VARIABLE_NAME= variable_value* 	**Create a new variable**

*Unset* 	**Remove a variable**

*export Variable=value* 	**To set value of an environment variable**


*###User management commands of linux###*


'''**Command        -       Description**''' 




*sudo adduser username* 	  **To add a new user**

*sudo passwd -l 'username'*    	**To change the password of a user**

*sudo userdel -r 'username'* 	**To remove a newly created user**

*sudo usermod -a -G GROUPNAME USERNAME* 	**To add a user to a group**

*sudo deluser USER GROUPNAME* 	**To remove a user from a group**

*finger* 	**Shows information of all the users logged in**

*finger username* 	**Gives information of a particular user**


*###Networking command###*


'''**Command        -       Description**''' 




*SSH username@ip-address or hostname* 	**login into a remote Linux machine using SSH**

*Ping hostname="" or =""* 	**To ping and Analyzing network and host connections**

*dir* 	**Display files in the current directory of a remote computer**

*cd "dirname"* 	**change directory to “dirname” on a remote computer**

*put file* 	**upload ‘file’ from local to remote computer**

*get file* 	**Download ‘file’ from remote to local computer**

*quit* 	**Logout**


*###Process command###*


'''**Command        -       Description**''' 




*bg* 	**To send a process to the background**

*fg* 	**To run a stopped process in the foreground**

*top* 	**Details on all Active Processes**

*ps* 	**Give the status of processes running for a user**

*ps PID* 	**Gives the status of a particular process**

*pidof* 	**Gives the Process ID (PID) of a process**

*kill PID* 	**Kills a process**

*nice* 	**Starts a process with a given priority**

*renice* 	**Changes priority of an already running process**

*df* 	**Gives free hard disk space on your system**

*free* 	**Gives free RAM on your system**


*###VI Editing Commands###*


'''**Command        -       Description**''' 




*i* 	**Insert at cursor (goes into insert mode)**

*a* 	**Write after cursor (goes into insert mode)**

*A* 	**Write at the end of line (goes into insert mode)**

*ESC* 	**Terminate insert mode**

*u* 	**Undo last change**

*U* 	**Undo all changes to the entire line**

*o* 	**Open a new line (goes into insert mode)**

*dd* 	**Delete line**

*3dd* 	**Delete 3 lines**

*D* 	**Delete contents of line after the cursor**

*C* 	**Delete contents of a line after the cursor and insert new text. Press ESC key to end insertion.**

*dw* 	**Delete word**

*4dw* 	**Delete 4 words**

*cw* 	**Change word**

*x* 	**Delete character at the cursor**

*r* 	**Replace character**

*R* 	**Overwrite characters from cursor onward**

*s* 	**Substitute one character under cursor continue to insert**

*S* 	**Substitute entire line and begin to insert at the beginning of the line**

*~* 	**Change case of individual character**


**Hope this Linux reference guide helps you**	
