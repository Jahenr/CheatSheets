
	#Install Github for Windows
		https://windows.github.com
		
	#Install Github for Mac
		https://mac.github.com
	
	#Install Github for all platforms
		https://git-scm.com
	
	#Creates a new local repo.
	       	git init
	       
	#Shows changes not yet staged 
	       	git diff

	#Show what files are changed, staged etc
		git status

	#Add files that are new, updated etc
		git add <filenames>
			Tip: git add . adds all files in the current directory.
			Tip: git add fil* adds all files starting with "fil" in the current directory.
	
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
			Tip: git log -p shows the commit's history including all files and their changes

	#List branches.
		git branch
		
	#List git branch with last commit info.
		git branch -v
		
	#List git branch with last commit and remote branch info.
		git branch -vv
		
	#Create a new branch.
		git branch <branch_name>
    
	#Creates branch and changes to it.
		git switch -c <branch_name>
		or
		git checkout -b <branch_name>

	#Change to specified branch.
		git switch <branch_name>
		or
		git checkout <branch_name>

	#Change to last branch used.
		git switch -

	#Show tracked repos.
		git remote -v	
		
	#Add new origin
		git remote add origin git@github.com:User/UserRepo.git
		
	#Change url of existing repo
		git remote set-url origin git@github.com:User/UserRepo.git

	#Push changes to the default remote repo.
		git push
		
	#Push local branch code to the remote master branch of the repository
		git push -u origin master
	
	#Push changes a specified branch.
		git push <branch_name>
			Tip: You can add a '+' before the branch name to force push the changes.

	#Pull changes from default remote repo and merges them into local.
		git pull

	#Pull changes from default remote repo but do not merge into local.
		git fetch
		
	#Remove Files from Working Directory
		git rm
		Tip: use rm -rf to remove all files forcefully
		
	#Clone or download a repo that already exists on github, including all of the files, branches and commits
		git clone <github_repo_url>

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
		git merge <branch_name>

	#To resolve merge conflict manually open the merge tool
		git mergetool

	#To remove untracked files from the working directory
		git clean 

	#Command to configure your username
		git config --global user.name "your name"
		
	#Command to configure your email-id
		git config --global user.email "your email address"

	#Command to enable helpful colorization of command line output
		git config --global color.ui auto

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

	#Command to delete specified branch
		git branch -d <branch_name>
	
	#Delete remote branch
		git push origin --delete <remote branch name>
	
  	#Reapply previously stashed changes and keep the stash
		git stash apply
    
	#Dropping changes in the stash
		git stash drop
    
	#Stashing everything (including ignored files)
		git stash --all
