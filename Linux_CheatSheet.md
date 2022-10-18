Linux/Unix:

	#List files and Directories.
		ls
			#Options include.
				-l = List
				-h = Human readable file/directory size
				-a = Show hidden files/directories

	#Colorize the output of the ls command 
		ls --color=auto
	
	#Change Directory
	    cd <pathname>
	        
			#Options
				cd .. = Moves to the previous parent directory
				cd ~  = Moves to the home directory of current user
				cd -  = Moves to the previous directory
	    
	#Home Directory 
	     cd
	
	#Moves to the Parent Directory of current Directory
	      cd..
	
	#To find the content of the file
		grep <"content to find"> <file name
	    Ex: grep "Google" companies.txt
	
	#To see previously ran commands
		history
	
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
	
	#Overwriting a file
		cat > <filename>

	#Appending text to a file from the terminal
		cat >> <file name>

			#Option include
				>> = Redirection operator
		
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

	#Create multiple files
		touch <filename1> <filename2> <filename3>

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
	
	#View strings in a file
		strings <filename>

	#View file type
		file <filename>

	#Details on all Active Processes
		top
		
  	#Determine system boot-up performance statistics
	   systemd-analyze
     
  	#Determine system boot-up performance statistics
    		systemd-analyze

	#Request system information / software version
		uname -a
    
	#Clear all previous commands from the history
		cat /dev/null > ~/.bash_history && history -c

  	#find the files by name
		locate <filename>
    
    	#List Block Devices mounted on the system
		lsblk

	#Delete a regular file
		rm <filename>
	
	#Delete an empty directory
		rm -r <directory>/

	#Delete a directory with content inside
		rm -rf <directory>/

	#Get the active username
		whoami

	#Find the difference between two files
		diff <file 1> <file 2>

	#Clear the terminal display
		clear
    
	#Look for the path of the file
		find <filename>

			#Option include
				f = file
				. = current directory

			#Query optimisation
				-type = type of file
				-name = matching with a filename	

	#Look for a file with a giving name using query optimisation
		find . -type f -name <filename>

	#Remove Directory if it is empty
		rmdir <directory name>

	#Remove Directory
		rm <option> <directory name>

			#Options include
				-r = recursive/content	

	#Check OS Details
		uname <option>

			#Options include
				-a = Information about the Operating System, Kernel version and hardware
				-s = Kernel name

	#Get information from a command and it's options
		help <command>

	#Display free disc space
		df <option>

			#Option include
				-h = Disc space in human readable format

	#Number of lines in a file
		nl <filename>

	#Content in alphabetical order
		sort <filename>

			#Option include
				-o = Write the output to a new file
				-r = Reverse Order

	#Content in a reverse order from a file
		sort -r <filename>

	#Write the output to a new file
		sort -o <current filename> <new filename>
	
  	#List Block Devices mounted on the system
		lsblk

	#Download files from the internet
	        wget <option> <url>

	#Open the calendar of the current month
		cal

	#Displays the file content in reverse order
		tac <file name>  

	#Displays screenful contents of a file at a time
		more <file name> 

	#Command line calculator
		bc

	#Replace old text with new text
		sed '-s/myOldText/myNewText' theFileBeingEdited.txt

