
	
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

	#Install the requirments listed in requirments.txt.
		pip3 install -r requirments.txt
