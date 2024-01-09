# Day-3 Learning
Blog's referred:
- https://medium.com/cloud-native-daily/mastering-linux-for-devops-engineers-essential-commands-and-practices-for-success-a608a718069f
- https://medium.com/cloud-native-daily/mastering-linux-advanced-skills-for-devops-engineers-1a0c00fad159
- https://www.geeksforgeeks.org/mv-command-linux-examples/
- https://www.geeksforgeeks.org/find-command-in-linux-with-examples/
- https://www.geeksforgeeks.org/chmod-command-linux/

# File and Directory Management
## E. Moving commands (```mv``` - is for renaming a file or directory and moving a file or directory to another location)
#### 1. It renames the source_file_name as Destination_file_name
###### If `Destination_file_name` already exists, in that case, it will be overwritten without prompting for confirmation.
    mv <source_file_name> <Destination_file_name>
#### 2. It moves the source_file_name to the Destination_path.
###### If `Destination_path` directory already exists with `source_file_name`, in that case, it will be overwritten without prompting for confirmation.
    mv <source_file_name> <Destination_path>
#### 3. It moves all the source_file_name to the Destination_path.
###### If `Destination_path` directory already exists with any one of `source_file_name`, in that case, it will be overwritten without prompting for confirmation.
    mv <source_file_name_1> <source_file_name_2> <source_file_name_3> <Destination_path>
#### 4. It renames the source_directory_name as Destination_directory_name
    mv <source_directory_name> <Destination_directory_name>
#### 5. It renames the source_file_name as Destination_file_name and 
###### If `Destination_file_name` does not exist, it is renamed simply.
###### If `Destination_file_name` already exists, prompts for a response, if you press y or yes then it overwrites the file and with any other option leaves it uncopied.
    mv -i <source_file_name> <Destination_file_name>
#### 6. It moves the source_file_name to the Destination_path.
###### If `Destination_path` directory already exists with `source_file_name`, in that case, it prompts for a response, if you press y or yes then it overwrites the file and with any other option leaves it uncopied.
    mv -i <source_file_name> <Destination_file_path>
#### 7. If the system is unable to overwrite the write protected because the user doesn’t have writing permission for this file/directory then by using -f option with mv command, source file/directory is overwritten with destination file.
    mv -f <source_file/directory_name> <Destination_file/directory_name/path>
#### 8. It prevents an existing file from overwritten.  
    mv -n <source_file> <Destination_file/path>
#### 9. It renames the source_file_name as Destination_file_name
###### If `Destination_file_name` already exists, in that case, it will be creating a new file with the tilda at the end of `Destination_file_name` (as `Destination_file_name~`)
    mv -b <source_file_name> <Destination_file_name>
    
## F. Find Command (```find``` to search the files and directories within a hierarchical structure)

Options Available in Find Command in Linux
Here are the `find` command options along with brief descriptions of their purposes.
| Command  | Description |
| ------------- | ------------- |
| ```-name pattern```| Searches for files with a specific name or pattern.|
| ```-type type```| Specifies the type of file to search for (e.g., f for regular files, d for directories).|
| ```-size [+/-]n```| Searches for files based on size. `+n` finds larger files, `-n` finds smaller files. ‘n‘ measures size in characters.|
| ```-mtime n```| Finds files based on modification time. `n` represents the number of days ago.|
| ```-exec command {} \;```| Executes a command on each file found.|
| ```-print```| Displays the path names of files that match the specified criteria.|
| ```-maxdepth levels```| Restricts the search to a specified directory depth.|
| ```-mindepth levels```| Specifies the minimum directory depth for the search.|
| ```-empty```| Finds empty files and directories.|
| ```-delete```| Deletes files that match the specified criteria.|
| ```-execdir command {} \;```| Executes a command on each file found, from the directory containing the matched file.|
| ```-iname pattern```| Case-insensitive version of `-name`. Searches for files with a specific name or pattern, regardless of case.|







#### 1. It renames the source_file_name as Destination_file_name
###### If `Destination_file_name` already exists, in that case, it will be overwritten without prompting for confirmation.
    mv <source_file_name> <Destination_file_name>
#### 1. It renames the source_file_name as Destination_file_name
###### If `Destination_file_name` already exists, in that case, it will be overwritten without prompting for confirmation.
    mv <source_file_name> <Destination_file_name>
