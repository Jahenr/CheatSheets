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
