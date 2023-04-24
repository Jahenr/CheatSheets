# CheatSheets, Common Command Line Commands 
## Welcome
CheatSheets is a project that contains the common commands used for a variety of systems. For a list of command systems that are already added, [click here](#list-of-commands). 


### Why command lines 
Command lines allows new starters to contribute to projects on Github and get used to Git tools and commands. It also allows user to perform a specific task that may be issued via command line interfance. 

You don't really need any coding experience as this is more of a documentation project, so no stress. Please feel free to contribute anytime you can, its appreciated. Directions on [how to contribute](#contributing) are provided below.  

I am still learning about Github and Git myself and want to get involved more within the open source community, so please feel free to give any advice or recommendations via an issue request.


---

## List of commands
NOTE this is a list of CLI that are already added and is here for your convience. Feel free to add more commands, edit existing, or add another CLI. 
* [Byobu](https://github.com/Jahenr/CheatSheets/blob/master/Byobu_CheatSheet.md)
* [Django](https://github.com/Jahenr/CheatSheets/blob/master/Django_Cheatsheet.pdf)
* [Elasticsearch](https://github.com/Jahenr/CheatSheets/blob/master/Elasticsearch_CheatSheet.md)
* [Flexbox](https://github.com/Jahenr/CheatSheets/blob/master/Flexbox_CheatSheet.md)
* [Flutter](https://github.com/Jahenr/CheatSheets/blob/master/Flutter_cheatsheet.md)
* [Git](https://github.com/Jahenr/CheatSheets/blob/master/Git_CheatSheet.md)
* [K8s](https://github.com/Jahenr/CheatSheets/blob/master/K8s_CheatSheet.md)
* [Linux](https://github.com/Jahenr/CheatSheets/blob/master/Linux_CheatSheet.md)
* [MYSQL](https://github.com/Jahenr/CheatSheets/blob/master/MYSQL_Cheatsheet.md)
* [NPM](https://github.com/Jahenr/CheatSheets/blob/master/NPM_CheatSheet.md)
* [Nano](https://github.com/Jahenr/CheatSheets/blob/master/Nano_Editor_CheatSheet.md)
* [Powershell](https://github.com/Jahenr/CheatSheets/blob/master/Powershell_CheatSheet.md)
* [Python](https://github.com/Jahenr/CheatSheets/blob/master/Python_CheatSheet.md)
* [Redis](https://github.com/Jahenr/CheatSheets/blob/master/Redis_CheatSheet.md)
* [SQL](https://github.com/Jahenr/CheatSheets/blob/master/SQL_CheatSheet.md)
* [Tmux](https://github.com/Jahenr/CheatSheets/blob/master/Tmux_CheatSheet.md)
* [VIM](https://github.com/Jahenr/CheatSheets/blob/master/VIM_CheatSheet.md)
* [VSCode](https://github.com/Jahenr/CheatSheets/blob/master/VSCode_CheatSheet.md)
* [Windows](https://github.com/Jahenr/CheatSheets/blob/master/Windows_CheatSheet.md)
* [aws](https://github.com/Jahenr/CheatSheets/blob/master/aws_CheatSheet.md)
* [Mongob](https://github.com/Jahenr/CheatSheets/blob/master/mongodb_cheatsheet.md)


---


## Contributing
1. Fork this repo (upper right hand corner) 
2. Get the link of the forked repo and `git clone` link of forked repo 
3. Create a new branch using `git checkout -b` newbranchname OR to edit an existing branch use `git checkout` branchname.
4. Push your changes to your fork and open a PR! 
5. Don't forget to update the ReadMe [List of Commands](#list-of-commands) in your forked repository if you created a new branch before opening the PR!



Adddtionally, links are provided below for the steps above! 
1. [Fork the repo and git clone your fork](https://docs.github.com/en/get-started/quickstart/contributing-to-projects)
2. [Create your branch](https://www.atlassian.com/git/tutorials/using-branches)
3. [Make your changes and commit them with a quick message of what was added](https://www.atlassian.com/git/tutorials/saving-changes/git-commit)
4. Push your changes and branch to your forked repo
5. [Open a PR so your changes can be reviewed and merged into the main project](https://docs.github.com/en/pull-requests/collaborating-with-pull-requests/proposing-changes-to-your-work-with-pull-requests/creating-a-pull-request)

The changes will be reviewed and if all is well, merged into master.

**Tip**: Remember to add the main project as upstream and do a `git pull` or `fetch` to keep your local fork up to date with the main project, before you commit and push any changes to your forked version ready for a PR.

Here is [a handy guide with more detail for clarity](https://stefanbauer.me/articles/how-to-keep-your-git-fork-up-to-date)

## NOTE before contributing 

Please have a search (`ctrl + f`) to see if the categories/commands or options have already been added, please do not duplicate already added entries. If possible try to group similar bundles of commands with each other.

The structure should be as followed.

Category or sub category:

```bash
    # Quick explanation of command
    	Command
```

e.g

Linux:

```bash
    # List files and Directories.
    	ls
    		#Options include.
    			-l = List
    			-h = Human readable file/directory size
    			etc


    # List files in a list, shows file size in human readable format and shows hidden files.
    	ls -lha
```

Looking at the example above the category/sub category name ends in a colon, then the command description is indented 1 tab (_8 Spaces_) below. The command itself is then indented 2 tabs (_16 Spaces_), the options title if applicable is indented 3 tabs (_24 Spaces_) and the options themselves indented 4 tabs (_32 Spaces_).

This is how the layout should be for the listed commands etc., **please follow the same structure throughout each cheat sheet.**

Thank you and have fun 😉
