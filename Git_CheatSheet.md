
	#Show what files are changed, staged etc
		git status

	#Add files that are new, updated etc
		git add <filenames>
			Tip: git add . adds all files in the current directory.

	#Commits files added with a message ready to be pushed.
		git commit -m "add message here"

	#Display record of commits made
		git log

	#List branches.
		git branch

	#Create a new branch.
		git branch <branch name>

	#Creates branch and changes to it.
		git switch -c <branch name>
		or
		git checkout -b <branch name>

	#Change to specified branch.
		git switch <branch name>
		or
		git checkout <branch name>

	#Change to last branch used.
		git switch -

	#Show tracked repos.
		git remote -v

	#Push changes to the default remote repo.
		git push
			Tip: you can specify the name of another tracked repo after "push".

	#Pull changes from default remote repo and merges them into local.
		git pull

	#Pull changes from default remote repo but do not merg into local.
		git fetch

	#Roll back and reset the last staged commit.
		git reset HEAD~1
			Tip: The number specifies how much commits to reset by, git reset HEAD~2 rolls back 2 commits etc.
    
	#Squash multiple commits into one commit.
		squash last 4 commits:
			git rebase -i HEAD~4
				Note: This command will open up default editor then replace "pick" on the second and subsequent commits with "squash".
		Squash all commits:
			git rebase --root -i
				Note: This command will open up default editor then replace "pick" on the second and subsequent commits with "squash".

	#Stash the current state of the working directory
		git stash

	#Remove the stashed code and apply it in the current working directory
		git stash pop

	#Remove all stashed entries
		git stash clear
  
  	#Remove new/existing files from staged files
		git restore --staged <file_name>
