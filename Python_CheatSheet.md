
	
	#Enter python interpreter.
		python

	#Exit python interpreter.
		exit()

	#Help page on modules or inbuilt functions.
		help()
			Tip: Enter module or function name in the parentheses

	#Create virtual environment in current folder.
		python -m venv ./venv

	#Activate virtual environment in current directory.
		source .venv/bin/activate

	#Exit virtual environment.
		deactivate
	
	#Run python script from IDLE.
		exec(open('path/to/file or filename').read())
	
	#Redirect the modules and dependencies installed to requirements.txt.
		pip3 freeze > requirements.txt

    	#Install modules whose names are listed in a file (requirements.txt)
		pip3 install -r requirements.txt
        
    	#Sort a 2D list (lst) based on any one index (i is the index)
		lst.sort(key = lambda x : x[i])

	#Print command can be used to print any type of object like integer,string, list, tuple, etc.
		print(object)

	#Round is used to round a number to a given precision in decimal digits. 
		round(number, digits)
	

