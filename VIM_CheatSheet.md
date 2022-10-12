
	
	#Insert mode
		i
	
	#Insert after cursor
        	a
		
	#Insert at the beginning of the line
		I
	
	#Insert at the end of the line
        	A
	
	#Create blank line below & insert
        	o
	
	#Create blank line above & insert
        	O

	#Normal mode
		esc key
	
	#Down
		j
	
	#Up
		k
	
	#Left
		h
	
	#Right
		l
	
	#Hop forward by a word
		w
	
	#Hop backward by a word
		b
	
	#Move to end of current word
		e

	#Write changes
		:w

	#Quit without saving changes
		:q!

	#Write and quit
		:wq

	#Enter visual mode to select characters
		v

	#Enter visual mode to select line
		V

	#Cut(Delete) selected text
		d

	#Cut current line
		dd
	
	#Cut current word
		diw
	
	#Cut current character
		x
	
	#Cut current character and insert (Substitute)
		s

	#Copy(Yank) selected text
		y

	#Copy current line
		y$

	#Paste after cursor
		p

	#Paste before cursor
		P

	#Undo vim action
		u

	#Redo vim action
		ctrl + r
	
	#Page up
		ctrl + u
	
	#Page down
		ctrl + d
	
	#Jump to beginning of file
		gg
	
	#Jump to bottom of file
		G

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
	
