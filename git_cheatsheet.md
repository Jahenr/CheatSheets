Git Terminologies
#	Git Command	Description
1	Bare- Repository	Repository without a working directory.
2	Branch-	A branch is an active area of development in Git. The most recent commit shows the tip of the branch.
3	Blame-	Describes the last modification to every line in the file. Shows Revision, Author & Time.
4	Checkout-	This refers to the process in which any given commit is selected from the repository and the state of the associated file and the directory tree is recreated in the working directory.
5	Commit-	This is a single point in Git history which holds the information about a changeset.
6	Diff-	A Diff is the difference in changes between two Commits, or saved changes.
7	Detached -Head	The state in which a specific commit is checked out instead of a branch.
8	Fetch-	Fetching means to get latest changes in the branch and the local/remote repos.
9	Fork-	By Forking the repository, you will be able to add Commits and create Pull Requests.
10	Hash-	A unique SHA1 code for every Commit
11	Head	-A named reference to the Commit at the tip of a Branch
12	Index	-A collection of files with state information.
13	Merge-To bring out the content of another Branch in the current Branch.
14	Master-	The default development Branch in Git
15	Origin-	The default Upstream Repository
16	Pull Request-	Suggests changes into the Master Branch
17	Push-	Pushes new changes after Committing them
18	Repository-	A collection of Commits, Branches and Tags to identify Commits.
19	Working Tree-	The tree of actual checked out files


Git Configuration
#	Git Command	Description
1	git config –global user.name	-Set the username to be used for all actions
2	git config –global user.email-	Set the email to be used for all the actions.
3	git config –global alias.-	Create a shortcut for the Git command.
4	git config –system core.editor	-Set the text editor for all the command actions.
5	git config –global –edit	-Open global configuration file in the text editor for manual editing.
6	git config –global color.ui auto-	Enable helpful colourization of command line outputs.


Set Up a Git Repository
#	Git Command	Description
1	git init-	Initialize an empty Git repo in the current project.
2	git clone (Repo URL)-	Clone the repository from GitHub to the project folder.
3	git clone (Repo URL) (Folder )-	Clone the repository into a specific folder.
4	git remote add origin
https://github.com/username/(repo_name).git	Create a remote repo pointing on your existing GitHub repository.
5	git remote-Shows the name of remote repositories.
6	git remote -v	-Shows the name and the URL of the remote repositories.
7	git remote rm -(remote repo name)-	Removes the remote repository.
8	git remote set-url origin (git URL)	-Changes the URL of the repository.
9	git fetch-	Get the latest changes from the origin but not merge.
10	git pull	-Get the latest changes from the origin and merge them.


Local File Changes
#	Git Command	Description
1	git add (file name)	-Add the current changes to the file to staging.
2	git add .-	Add the whole directory changes to staging (no delete files).
3	git add -A	-Add all new, modified and deleted files to staging.
4	git rm (file_name)-	Removes the file and untracks (stop tracking) it.
5	git rm –cached (file_name)	-Untracks the current file.
6	git mv  (file_name) (new_file_name)	-Changes the filename and prepare it for Commit.
7	git checkout <deleted file name>	-Recovers the deleted file and prepares it for Commit
8	git status	-Shows the status of the modified files.
9	git ls-files –other –ignored –exclude-standard	-Shows the list of all ignored files.
10	git diff	-hows unstaged changes in the index and the working directory.
11	git diff –staged	-Shows file differences between staging and the last file version.
12	git diff (file_name)	-Shows changes in a single file compared to the last Commit.

Declare Commits
#	Git Command	Description
1	git commit -m “(message)”	-Commits the changes with a custom message.
2	git commit -am “(message)”	-Adds all changes to staging and commits them with a custom message.
3	git checkout	S-witch to the provided Commit.
4	git show	-Outputs the metadata and content changes of the specified Commit.
5	git reset –hard-Discard all the history and changes back to a given Commit.
6	git reset –hard Head	-Discards all local changes in the working directory.
7	git log	-Shows the history of changes.
8	git log -p	-Shows the full display of each Commit.
9	git log -oneline	-Shows the list of Commits with a simple message.
10	git log –follow (file_name)	-List the history for the current file.
11	git blame (file_name)	-Shows all changes along with the name of the user.
12	git stash	-emporarily saves all modified tracked files.
13	git stash pop	-Restores the most recently stashed files.
14	git stash -list	List all stash changedsets.
15	git stash apply-	Apply the latest stashed contents.
16	git stash drop	-Discard the most recently stashed files
17	git stash apply (stash id)	-Re-apply a specific stash content by ID.
18	git stash drop (stash_id)	-Drop a specific stash content by ID.
19	git push	-Push changes to the Origin.
16	git push origin (branch_name)	-Push branch to the Origin.
17	Git push -f origin (branch_name)	-Force pushes the changes to the Origin.
18	git tag (tag_name)	-Define a tag for a version.
19	git push	-Push changes to the Origin.


Branching
#	Git Command	Description
1	git branch	-Shows the list of all branches.
2	git branch	-Creates a new branch.
3	git branch -m	-Renames the branch.
4	git branch -a	-List all branches, local and remote.
5	git checkout -b	-Creates a branch and switch to it.
6	git checkout	-Switch to the provided branch.
7	git checkout -b origin/	-Get a remote branch from origin to the local directory.
8	git branch -d	-Delete the specified branch.
9	git merge	-erge the current branch into the master (first checkout to master)
10	git rebase	-Takes all the changes of the branch and restate on others.
11	git rebase	-Rebase the current branch onto the base. Base can be a Commit ID or a branch name.
12	git fetch remote	-Fetches the specified branch from the repository.
13	git diff ..	-Shows the differences between two branches.
14	git pull –rebase	-Fetches the remote copy of the current branch and rebases it into the local copy.
15	git push –all	Push all the local branches to the specified remote repository.
