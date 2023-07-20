	
	#To Run file/s enter in terminal
		gcc file.c -o anyname

	#To exit the program
		exit(return code);
			#Return Code Options
				EXIT_SUCCESS = executed successfully without error
				EXIT_FALIURE or 0 = Indicates presence of an error in the code
				Can be any number from 0 - 255

	#Show output on the screen
		printf("Hello world");

	#Show output on the screen with a format specifier/s
		printf("format_specifier", variables);
			#Format Specifiers
				%d = Signed Integer
				%c = Charcter
				%e or %E = Scientific notation of Floats
				%f = Float Values
				%hi = signed integer (short)
				%hu = Unsigned Integer(short)
				%i = Unsigned Integer
				%l or %ld or %li = Long
				%lf = Double
				%Lf = Long double
				%lu = Unsigned int or unsigned ong
				%o = Octal representation
				%p = pointer
				%s = string
				%u = Unsigned int
				%x or %X = Hexidecimal representation

	#To take input from user
		scanf("format_specifier", &variables);

	#Single line comment
		// It is a single line comment

	#Multi-line comment
		/* Its a 
		multi-line
		comment
		*/

	#Skips the rest of current iteration of the loop and returns to the strating point of the loop
		continue;

	#Breaks the loop
		break

	#Returns a value from a function/method
		return val;

	#Conditional statements used perform operation based on condition
		if (condition)
		{
		code goes here
		}else if(condition)
		{
		code goes here
		}else{
		code goes here
		}

	#Loops based on if it meets the condition
		while(condition)
		{
		code goes here
		}

		