
	#Show what files are changed, staged etc
		git status

	#Add files that are new, updated etc
		git add <filenames>
			Tip: git add . adds all files in the current directory.

	#Commits files added with a message ready to be pushed.
		git commit -m "add message here"

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
			Tip: you can specify the name of another tracked repo after "push"

	#Pull changes from default remote repo and merges them into local.
		git pull

	#Update remote repo

