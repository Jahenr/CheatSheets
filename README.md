# CheatSheets

This repo is small project that is a central place for the most common commands used for systems we may use in work/projects.

It can allow new starters to contribute to projects on Github and get used to Git tools and commands. 

You dont really need any coding experience as this is more of a documentation project, so no stress. Please feel free to contribute anytime you can, its appreciated.

I am still learning about Github and Git myself and want to get involved more within the opensource community, so please feel free to give any advice or reccomendations via an issue request.

--------------------------------------------------

To add stuff to this repo it best to fork this repo, git clone your fork of the repo, create a branch and make changes, push them to your fork and then open a PR

High level Steps include:

1. Fork the repo and git clone your fork - https://docs.github.com/en/get-started/quickstart/contributing-to-projects 
2. Create your branch - https://www.atlassian.com/git/tutorials/using-branches
3. Make your changes and commit them with a quick message of what was added - https://www.atlassian.com/git/tutorials/saving-changes/git-commit
5. Push your changes and branch to your forked repo.
6. Open a PR so your changes can be reviewed and merged into the main project.

The changes will be reviewed and if all is well, merged into master.

Tip: Remember to do a git pull or fetch to keep your local up to date with the main project before you commit and push any changes, this ensures your local is up to date with remote main project. - https://stefanbauer.me/articles/how-to-keep-your-git-fork-up-to-date

--------------------------------------------------

Please have a search (ctrl + f) to see if the categories/commands or options have already been added, please do not duplicate already added entries. If possible try to group simmilar bundles of commands with each other.

The structure should be as followed.

Sub category:

    #Quick explanation of command
        Command

e.g

Linux/Unix:

    #List files and Directories.
        ls
            #Options include.
                -l = List
                -h = Human readable file/directory size
                etc
                
        
    #List files in a list, shows file size in human readable format and shows hidden files.
        ls -lha


Looking at the example above the category/sub category name ends in a colon, then the command description is indented 1 tab (8 Spaces) below. The command itself is then indented 2 tabs (16 Spaces), the options title if applicable is idented 3 tabs (24 Spaces) and the options themselves idented 4 tabs (32 Spaces).

This is how the layout should be for the listed commands etc, please follow the same structure throughout each cheat sheet.

Thank you and have fun ;)
