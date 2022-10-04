Powershell:

cmdlets:

# This command allows you to get support with PowerShell
        Get-Help 

# This command offers you a list of available PSDrives, such as c, env, hklm, hkcu, alias, etc.
        Get-PSdrive

# In any registry, children are the subkeys of the current key. To get the required details, you can use the following command.
        Get-ChildItem

# Run this command to list all the children recursively of the current PSdrive, folder, or registry key.
        Get-ChildItem -recurse

# Use this command To include the hidden folders (directories).
        Get-ChildItem -rec -force

# Run any of these commands to get the list file and directory names in the current folder.
        (Get-ChildItem).name or Get-ChildItem -name        

# Use this command to get the number of entries in the collection of objects returned by the Get-Children.
        (Get-ChildItem).count 

PSdrives:         

# The prompt character will change to the “ENV:\>”. Set-Location env by running the following command:Set-Location env-
        Switching to env-

# This command will get you all the environment variables.
        Env:\> Get-Childitem        

# Use this command to get the environment variables of “userprofile.”
        Env:\> Get-Childitem userprofile

# Run the following command to change the prompt character to “Alias.”
        Env:\> Set-Location alias:

# Run this command to get all the children of all aliases.
        Alias:\> Get-Childitem

# Use this command to get the “C:/>” prompt again, back to the default drive.
        Alias:\> Set-Location C:\

# Run this command to find what alias “ls” stands for.
        C:\Users\user_name>$alias:ls

Pipelines:

# The pipeline consists of the following three stages.
        Get-ChildItem *.txt | Where-Object length -lt 1000 | Sort-Object length

# Easily sets the value of the ‘lastwritetime.year’ property to the present date and time without affecting the file’s content.
        (Get-Item /Users/praashibansal/Desktop).lastwritetime.year

# Provides an empty result
        (Get-ChildItem data.txt.rtf -name).name # -> null    

# Changes the old file names and file extensions to the new ones
        "data.txt.rtf" | Rename-Item -NewName "data_new.txt.rtf"

# A trivial renaming command that invokes an automatic variable
        Get-ChildItem data.txt | Rename-Item -new {$_.name}

# If the piped object $_ doesn't have the member property (name), you will receive an error, as parameter $_.name is null
        Get-ChildItem data.txt.rtf -name | Rename-Item -new {$_.name} 

# Displays the list of the names of all the files that are present in the current folder sorted in alphabetical order.
        Get-ChildItem | Select-Object basename | Sort-Object *

# Moves all the files to the folder subdirectory
        Move-Item *.txt subdirectory

# Gives the error message that Move-Item lacks input
        Get-ChildItem *.txt | Move-Item ..\

Alias:         

# Appends value to a file
        Add-Content

# Finds file content in an array
        Get-Content

# Changes folder, key, or PS drive
        Set-Location

# Clears console
        Clear-Host

# Delete files
        Remove-Item

# Lists Folder, Key, or PSDrive Children
        Get-ChildItem -Path .\

# Sends the array to the console, pipeline, or redirect it to the file
        Write-Output

# Traverses each object in a pipeline
        Foreach-Object

# Formats the table with selected properties for each object in each column
        Format-Table 

# Formats the process properties by name
        Format-List

# Provides Cmdlet Alias
        Get-Alias

# Provides you with commands from the current session only
        Get-Command 

# Retrieves all the object members
        Get-Member

# Provides the specified item’s properties
        Get-ItemProperty .\data.txt | Format-List

# Gives the current value for a specified property while using the name parameter
        Get-ItemPropertyValue -Path '.\data.txt' -Name LastWriteTime 

# Finds session variable names and sessions
        Get-Variable m*

# Creates a new file, directory, symbolic link, registry key, or registry entry
        New-Item -Path .\ -Name "testfile1.txt" -ItemType "file" -Value "This is a text string."

# Gives the entire list of all the running processes
        Get-Process 

# Provides the current directory’s or registry key’s location
        Get-Location

# Renames the old item name with the new name
        Rename-Item -Path “old_name” -NewName “new_name”

# Removes the specified directory, files, or registry keys
        Remove-Item .\testfile1.txt 

# Removes the specified variable
        Remove-Variable 

# Suspends an activity for a specified period of time
        Start-Sleep              