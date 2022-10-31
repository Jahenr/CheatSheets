	#Enter insert mode at current cursor position
		i

	#Enter insert mode at the start of the current line
		I

	#Enter insert mode after cursor (Append)
       		a

	#Enter insert mode at the end of the current line
        	A

	#Create blank line below cursor & and enter insert mode
        	o

	#Create blank line above cursor & and enter insert mode
        	O

	#Exit any other mode and enter Normal mode
		<esc> key

    	#Search for text in buffer
        	/<search-pattern>

    	#Jump to the beginning of the line 
		0

    	#Jump to the end of the line 
		$

    	#Jump to next search match
		n

    	#Jump to previous search match
		N

	#Write changes
		:w

	#Quit without saving changes
		:q!

	#Quit all open buffers without saving changes
		:qa!

	#Write and quit
		:wq
   
	#Enter visual mode to select characters
		v

	#Enter visual mode and select entire line
		V

	#Cut(Delete) selected text
		d

	#Delete next word selected text
		dw

	#Delete previous word selected text
		db

	#Cut current line
		dd

	#Copy(Yank) highlighted text in visual mode
		y

	#Copy beginning from the cursor position until the end of the line in Normal mode
		y$

	#Paste the line below the cursor
		p

	#Paste the line above the cursor
		P

	#Undo vim action
		u

    	#Jump to the first character of the next word in the line
       		w

    	#Jump to the last character of the next word in the line
        	e

    	#Jump to the previous word in the line
        	b

    	#Jump to the top of the buffer
        	gg

    	#Jump to the bottom of the buffer
        	G

	#Redo vim action
		ctrl + r

	#Open a bash session from Vim
		:! bash

	#Exit a bash session to go back to Vim
		exit

	#Turn word-wrap on/off
        	:set wrap
        	:set nowrap	

	#Turn line numbers on/off
        	:set number
        	:set nonumber

	#Turn relative line numbers on/off
        	:set relativenumber
        	:set norelativenumber

	#Open multiple files in new tabs (from bash prompt)
        	vim -p <file1> <file2> ...

	#Quick switch to next tab
        	gt

	#Quick switch to previous tab
        	gT

	#Save tab session to file
        	:mksession <session_filename.vim>

	#Load saved tab session (from bash prompt)
        	vim -S <session_filename.vim>

	#Search and replace all patterns found in file
		:%s/<pattern match>/<replace with>/g

	#Search and replace all patterns found in file with confirmation
		:%s/<pattern match>/<replace with>/gci
	
