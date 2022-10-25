Linux/Unix:

* #### List files and Directories.
    
```bash
$ls
```
#### 
```text
Options include.
-l = List
-h = Human readable file/directory size
-a = Show hidden files/directories
```

* #### Change Directory.
```shell
$cd <pathname>
```

* #### Print ASCII character strings in large letters.
```shell
$banner <text>
```

* #### List running processes.
```shell
$ps
```

* #### Create a new directory.
```shell
$mkdir <directory name>
```

* #### Print the working directory
```shell
$pwd
```

* #### Recursively search for a file or directory.
```shell
$find <directory> -name <filename>
```
	    
* #### Print the contents of a file.
```shell
$cat <filename>
```

* #### Print the contents of a file with line numbers.
```shell
$cat -n <filename>
```

* #### Print the contents of a file with line numbers and non-printing characters.
```shell
$cat -v <filename>
```

* #### Copy a file.
```shell
$cp <source> <destination>
```

* #### Copy a file and preserve the file attributes.
```shell
$cp -p <source> <destination>
```

* #### Move or rename a file.
```shell
$mv <original file> <new location or name>
```

* #### Remove a file.
```shell
$rm <filename>
```

* #### Remove a directory.
```shell
$rmdir <directory name>
```

* #### Remove a directory and all of its contents.
```shell
$rm -r <directory name>
```

* #### Remove a file without prompting for confirmation.
```shell
$rm -f <filename>
```

* #### Remove a directory without prompting for confirmation.
```shell
$rmdir -f <directory name>
```

* #### Remove a directory and all of its contents without prompting for confirmation.
```shell
$rm -rf <directory name>
```

* #### Move or rename a file.
```shell
$mv <original file> <new location or name>
```

* #### Create a symbolic link.
```shell
$ln -s <source> <destination>
```

* #### Create a hard link.
```shell
$ln <source> <destination>
```

* #### Create a file.
```shell
$touch <filename>
```

* #### Create a file and set the file permissions.
```shell
$touch -m <filename>
```

* #### Run previous command as sudo.
```shell
$sudo !!
```

* #### Run previous command as sudo and edit it.
```shell
$sudo !:e
```

* #### Display history file in terminal.
```shell
$history
```

* #### Display history file in terminal with line numbers.
```shell
$history -n
```

* #### Run command with history ID <id>.
```shell
$!<id>
```

* #### Run command with history ID <id> as sudo.
```shell
$sudo !<id>
```

* #### Run last command via command name.
```shell
$!<command name>
```

* #### Run last command via command name as sudo.
```shell
$sudo !<command name>
```

* #### Search man pages with given keyword.
```shell
$apropos <keyword>
```

* #### Use stdout as an argument.
```shell
$xargs <command>
```

* #### Show information of file.
```shell
$file <filename>
```

* #### Reverse search of history.
```shell
$Ctrl + R <command>
```

```text
Tip: Press ctrl + r to cycle to the next command etc
```

* #### Search for a string in a file.
```shell
$grep <string> <filename>
```

* #### Show current user.
```shell
$whoami
```

* #### Show current user and group.
```shell
$groups
```

* #### Pause current session.
```shell
$Ctrl + Z
```

* #### Resume current session.
```shell
$fg
```

* #### Resume current session in background.
```shell
$bg
```

* #### Show current session.
```shell
$jobs
```

* #### Show network interface information.
```shell
$ifconfig
```

* #### Show drive usage information.
```shell
$df
```

* #### Show drive usage information in human readable format.
```shell
$df -h
```

* #### Show memory usage information.
```shell
$free
```

* #### Show memory usage information in human readable format.
```shell
$free -h
```

* #### Ping a given IP or domain.
```shell
$ping <ip or domain>
```

* #### Open an SSH session with a given user and machine.
```shell
$ssh <user>@<machine>
```

* #### Open an SSH session with a given user and machine and port.
```shell
$ssh <user>@<machine> -p <port>
```

* #### Close an active SSH session or exit the terminal.
```shell
$exit
```

* #### Show the current date and time.
```shell
$date
```

* #### Show logs of specified service.
```shell
$journalctl -u <service>
```

* #### Show logs of specified service and follow.
```shell
$journalctl -u <service> -f
```

* #### Show logs of specified process ID.
```shell
$journalctl _PID=<pid>
```

* #### Show all installed services.
```shell
$systemctl list-unit-files --type=service
```

* #### Show all running services.
```shell
$systemctl list-units
```

* #### Show all running services and follow.
```shell
$systemctl list-units -f
```

* #### Terminate process.
```shell
$kill <pid>
```

* #### Terminate process and all of its children.
```shell
$kill -9 <pid>
```

* #### Print the first 10 lines of a file to standard output.
```shell
$head <filename>
```

```text
Options include
-n [NUM] = Print the first NUM lines instead of 10
-n -[NUM] = Print all but the last NUM lines of a file
```

* #### Print the last 10 lines of a file to standard output.
```shell
$tail <filename>
```

```text
Options include
-n [NUM] = Print the last [NUM] lines instead of 10
-n +[NUM] = Print all lines starting with [NUM] until EOF
```

* #### Check the current system clock time.
```shell
$timedatectl
```

```text
Options include
set-time "yyyy-MM-dd hh:mm:ss" = Set the local time of the system clock directly
list-timezones = available timezones
set-timezone timezone = Set the system timezone
set-ntp on = Enable Network Time Protocol (NTP) synchronization
```

* #### Show the current system clock time.
```shell
$timedatectl status
```

* #### Change the permissions granted.
```shell
$chmod <permissions> <filename>
```

* #### Change the owner of a file.
```shell
$chown <user> <filename>
```

* #### Change the apparent root directory for the current running process and its children.
```shell
$chroot <directory>
```

* #### Create (if not exist) or Edit file using vi.
```shell
$vi <filename>
```

* #### Create (if not exist) or Edit file using nano.
```shell
$nano <filename>
```

* #### Displays active TCP connections, ports.
```shell
$netstat -tulpn
```

* #### Displays active TCP connections, ports, and process ID.
```shell
$netstat -tulpn | grep <port>
```

* #### Download from terminal.
```shell
$wget <url>
```

* #### Download from terminal and set output filename.
```shell
$wget -O <filename> <url>
```

* #### Unzip a file.
```shell
$unzip <filename>
```

* #### Unzip a file to a specific directory.
```shell
$unzip <filename> -d <directory>
```

* #### Mount a drive.
```shell
$mount <drive> <directory>
```

* #### Unmount a drive.
```shell
$umount <drive>
```

* #### Switch to users.
```shell
$su <user>
```

* #### Switch to root
```shell
$su root
```

* #### Find the location of source/binary file.
```shell
$which <filename>
```

* #### Install, build, remove and manage packages
* ###### Debian/Ubuntu
```shell
$dpkg
$apt-get install <package>
$apt-get build-dep <package>
$apt-get remove <package>
$apt-get update
$apt-get upgrade
```

* ###### Redhat/CentOS
```shell
$rpm
$yum install <package>
$yum builddep <package>
$yum remove <package>
$yum update
$yum upgrade
```

* ###### Arch
```shell
$pacman
$pacman -S <package>
$pacman -Ss <package>
$pacman -R <package>
$pacman -Syu
```

* ###### Gentoo
```shell
$emerge
$emerge <package>
$emerge -av <package>
$emerge -C <package>
$emerge -uDN world
```

* ###### Slackware
```shell
$installpkg
$installpkg <package>
$installpkg -l <package>
$installpkg -r <package>
$upgradepkg
$upgradepkg --install-new
```

* ###### FreeBSD
```shell
$pkg
$pkg install <package>
$pkg search <package>
$pkg delete <package>
$pkg update
$pkg upgrade
```

* ###### OpenBSD
```shell
$pkg_add
$pkg_add <package>
$pkg_info
$pkg_info <package>
$pkg_delete
$pkg_delete <package>
$pkg_info -u
$pkg_info -a
```

* ###### NetBSD
```shell
$pkgin
$pkgin install <package>
$pkgin search <package>
$pkgin remove <package>
$pkgin update
$pkgin upgrade
```

* ###### DragonFlyBSD
```shell
$pkg
$pkg install <package>
$pkg search <package>
$pkg delete <package>
$pkg update
$pkg upgrade
```

* ###### Solaris
```shell
$pkg
$pkg install <package>
$pkg search <package>
$pkg uninstall <package>
$pkg update
$pkg upgrade
```

* ##### Creates a new user account.
```shell
$useradd <username>
```

* ##### Creates a new user account with a specific user ID.
```shell
$useradd -u <uid> <username>
```

* ##### Creates a new user account with a specific group ID.
```shell
$useradd -g <gid> <username>
```

* ##### Creates a new group.
```shell
$groupadd <groupname>
```

* ##### Adds a user to a group.
```shell
$usermod -a -G <groupname> <username>
```

* ##### Removes a user from a group.
```shell
$gpasswd -d <username> <groupname>
```

* ##### Removes a user from a group.
```shell
$userdel
```

* ##### Change password of user.
```shell
$passwd <username>
```

* ##### Check md5sum of file.
```shell
$md5sum <filename>
```

* ##### Check sha1sum of file.
```shell
$sha1sum <filename>
```

* ##### Check sha256sum of file.
```shell
$sha256sum <filename>
```

* ##### Check sha512sum of file.
```shell
$sha512sum <filename>
```

* ##### Prints the name of the terminal.
```shell
$echo $TERM
$tty
```

* ##### Ftp on a remote host.
```shell
$ftp <host>
```

* ##### Ftp on a remote host with a specific port.
```shell
$ftp -p <port> <host>
```

* ##### Ftp on a remote host with a specific username.
```shell
$ftp -u <username> <host>
```

* ##### Ftp on a remote host with a specific username and password.
```shell
$ftp -u <username> -p <password> <host>
```

* ##### DNS lookup.
```shell
$dig <domain>
```

* ##### DNS lookup with a specific nameserver.
```shell
$dig @<nameserver> <domain>
```

* ##### DNS lookup with a specific nameserver and port.
```shell
$dig @<nameserver> -p <port> <domain>
```

* ##### View strings in a file.
```shell
$strings <filename>
```

* ##### View file type.
```shell
$file <filename>
```

* ##### Details on all Active Processes.
```shell
$ps -aux
$top
```

* ##### Details on all Active Processes with a specific user.
```shell
$ps -u <username>
```

* ##### Determine system boot-up performance statistics.
```shell
$uptime
$systemd-analyze
```

* ##### Determine system boot-up performance statistics with a specific user.
```shell
$systemd-analyze blame
```

* ##### Find the files by name.
```shell
$find <directory> -name <filename>
$locate <filename>
```

* ##### TCPdump filter HTTP Request (GET).
```shell
$sudo tcpdump -s 0 -A 'tcp[((tcp[12:1] & 0xf0) >> 2):4] = 0x47455420'
```

* ##### TCPdump filter for HTTP Request(POST).
```shell
$sudo tcpdump -s 0 -A 'tcp dst port 80 and (tcp[((tcp[12:1] & 0xf0) >> 2):4] = 0x504f5354)'
```

* ##### TCPdump filter for HTTP traffic including request and response header and message body.
```shell
$tcpdump -A -s 0 'tcp port 80 and (((ip[2:2] - ((ip[0]&0xf)<<2)) - ((tcp[12]&0xf0)>>2)) != 0)'
$tcpdump -X -s 0 'tcp port 80 and (((ip[2:2] - ((ip[0]&0xf)<<2)) - ((tcp[12]&0xf0)>>2)) != 0)'
```
