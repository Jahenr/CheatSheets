
	#To print output on the screen
		cout<<"This is a cheat-sheet for C++ language";
	
	#To take input from the user
		cin>>variable_name;

	#To execute the program (windows)
		g++ -o program program.cpp && program.exe
			
			#On Unix(linux and mac)
				CC program.cc
				
				#can use gcc
					gcc -o program program.cpp&&program.exe

	#Data types used
		char, int, float, double, bool, String

			#Example
				char variable_name;
	#Comments
		#Single line comment
			//It is a single line comment

		#multiline comment
			/*It is a
			multiline
			comment*/
	
	#Built-in functions
		#Math functions
			#max function
				cout<<max(100, 19);
			
			#min function
				cout<<min(80, 90);
			
			#sqrt function
				#include <cmath>

				cout<<sqrt(36);
				
			#ceil function
				ceil(X)
				
			#floor function
				floor(X)

	#Escape Sequences
		#Backspace
			\b
			
		#newline
			\n
			
		#carriage return 
			\r

		#tab
			\t

		#backslash
			\\

		#Single quote
			\'

		#Question mark
			\?

	#Pointers
		#Declaration
			data_type *var_name;
			var_name = &var2;

	#User defined functions
		return_type func_name(data_type parameter..){
		 ...
		 }

		 func_name(args);
