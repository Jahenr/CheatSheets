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
    
	#Terminate process 
	    kill <process id>

	#Create a file
	    touch <filename>

	
