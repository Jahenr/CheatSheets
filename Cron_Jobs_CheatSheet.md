Cron Jobs:

`The crontab utility is the program used to install, deinstall or list the tables
used to drive the cron(8) daemon in Vixie Cron.  Each user can have their own
crontab, and they are not intended to be edited directly.`


	#Command
		crontab
			#Options include.
            -u = Specify the name of the user whose crontab is to be tweaked
            -l = Display the current crontab on standard output
            -r = Remove the current crontab
            -e = Edit the current crontab using the editor.
	
	#Open crontab editor to add or edit a cron
	    crontab -e
	    
	#Remove current crontab
		crontab -r

	#Display current crontab
		crontab -l

	#Open crontab editor to add or edit a cron with user
		crontab -u [user] -e
	

    #Format

    Min  Hour Day  Mon  Weekday
    *    *    *    *    *  command to be executed
    ┬    ┬    ┬    ┬    ┬
    │    │    │    │    └─  Weekday  (0=Sun .. 6=Sat)
    │    │    │    └──────  Month    (1..12)
    │    │    └───────────  Day      (1..31)
    │    └────────────────  Hour     (0..23)
    └─────────────────────  Minute   (0..59)

    #Operators

    * =	all values
    , =	separate individual values
    - =	a range of values
    / =	divide a value into steps

    #Examples

    0 * * * * =	every hour

    */15 * * * * =	every 15 mins

    0 */2 * * * = every 2 hours

    0 18 * * 0-6 = every week Mon-Sat at 6pm

    10 2 * * 6,7 = every Sat and Sun on 2:10am

    0 0 * * 0 = every Sunday midnight

    @reboot	= every reboot