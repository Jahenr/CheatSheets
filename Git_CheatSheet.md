         #creates a new local repo.
	       git init
	       
	 #shows changes not yet staged 
	       git diff

	#Show what files are changed, staged etc
		git status

	#Add files that are new, updated etc
		git add <filenames>
			Tip: git add . adds all files in the current directory.
	
	#Add patches of a file
		git add <filename> -p  #this command adds a specific file
		git add . -p  #this command adds patches from all files within directory

	#Commits files added with a message ready to be pushed.
		git commit -m "add message here"
	
	#Commit files to the last commit and edit commit message.
		git commit --amend
	
	#Commit files to the last commit and keep the original commit message.
		git commit --amend --no-edit

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
	
	#Push changes a specified branch.
		git push <branch_name>
			Tip: You can add a '+' before the branch name to force push the changes.

	#Pull changes from default remote repo and merges them into local.
		git pull

	#Pull changes from default remote repo but do not merg into local.
		git fetch

	#Roll back and reset the last staged commit.
		git reset HEAD~1
			Tip: The number specifies how much commits to reset by, git reset HEAD~2 rolls back 2 commits etc.
	
	#Perform interactive rebase.
		git rebase -i
	
	#Peform interactive rebase on the last 'N' commits.
		git rebase -i HEAD~<N>
    
	#Squash multiple commits into one commit.
		squash last 4 commits:
			git rebase -i HEAD~4
				Note: This command will open up default editor then replace "pick" on the second and subsequent commits with "squash".
        
	#Squash all commits:
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
		
	#Cherry Pick enables arbitrary Git commits to be picked by reference and appended to the current working HEAD.  
               cherry pick a commit on to main branch:
                        git cherry-pick commitSHA
  
	#Command to merge a specific branch into the current branch
		git merge <branch name>

	#To resolve merge conflict manually open the merge tool
		git mergetool

	#To remove untracked files from the working directory
		git clean 

	#Command to configure your username
		git config --global user.name "your name"

	#To see all configurations
		git config --list
    
	#Add origin/upstream remote
		git add origin/upstream <git_url>
			Note: Upstream refers to the original repo that you have forked. Origin refers to your fork on the original repo.
	
	#Fetch changes from upstream of all the branches.
		git fetch upstream
			Note: You first need to add the upstream remote.
	
	#Sync local branch with the upstream branch.
		git rebase upstream/<branch_name>
			Note: Use this command only after fetching the changes from the upstream.
      
