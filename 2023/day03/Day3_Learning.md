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
    
## F. ```find``` Command (```find``` to search the files and directories within a hierarchical structure)
#### 1. To find a ```file/directory_name``` in the home directory
    find ~ -name <file/directory_name>
#### 2. It seeks a ```file/directory_name``` within the ```directory_name``` directory. (like searching from the pwd and then search for file/directory throughout that directory)
    find ./<directory_name> -name <file/directory_name>
#### 3. It seeks a ```file/directory_name``` having the specific pattern of file (like .txt, .md etc) type within the ```directory_name``` directory. (like searching from the pwd and then search for file/directory throughout that directory)
    find ./<directory_name> -name *.txt 
#### 4. It lists the empty files and directories within a specified directory ```directory_name```.
    find ./<directory_name> -empty

#### Options Available in Find Command in Linux
#### Here are the `find` command options along with brief descriptions of their purposes.
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

## G. ```chmod``` Command (```chmod``` stands for ```change mode``` and used for change file permissions. In this the permissions have three categories: read, write, and execute simultaneously represented by `r`, `w` and `x`. )
#### 1. To find a ```file/directory_name``` in the home directory
    find ~ -name <file/directory_name>
#### Options Available in chmod Command Linux
| Options  | Description |
| ------------- | ------------- |
| ```-R```| Apply the permission change recursively to all the files and directories within the specified directory.|
| ```-v```| It will display a message for each file that is processed. while indicating the permission change that was made.|
| ```-c```| It works same as `-v` but in this case it only displays messages for files whose permission is changed.|
| ```-f```| It helps in avoiding display of error messages.|
| ```-h```| Change the permissions of symbolic links instead of the files they point to.|

### Modes in chmod Command in Linux
#### The “mode” helps in setting new permissions that have to be applied to files or directories.
#### This mode can be specified in several ways, we will discuss two modes: Symbolic and Octal mode. 

#### 1. Symbolic mode
##### If we talk about symbolic mode, we can say that it is the most common method used for specifying fir permissions. In this we have to make a combination of letters and operators to set or tell what to do with permissions.

##### The following operators can be used with the symbolic mode:
| Operators  | Definition |
| ------------- | ------------- |
| ```+```| Add permissions|
| ```-```| Remove permissions|
| ```=```| Set the permissions to the specified values|

##### The following letters that can be used in symbolic mode:
| Letters  | Definition |
| ------------- | ------------- |
| ```r```| Read permission|
| ```w```| Write permission|
| ```x```| Execute permission|

##### The following Reference that are used:
| Reference  | Class |
| ------------- | ------------- |
| ```u```| Owner|
| ```g```| Group|
| ```o```| Others|
| ```a```| All (owner,groups,others)|

#### Examples of Using the Symbolic mode:
#### Read, write and execute permissions to the file owner:
    chmod u+rwx [file_name]

#### Remove write permission for the group and others:
    chmod go-w [file_name]

#### Read and write for Owner, and Read-only for the group and other:
    chmod u+rw,go+r [file_name]

#### 2. Octal mode
##### It is also a method for specifying permissions. In this method we specify permission using three-digit number. Where..

##### - First digit specify the permission for Owner.
##### - Second digit specify the permission for Group. 
##### - Third digit specify the permission for Others. The digits 
###### NOTE: The digits are calculated by adding the values of the individual permissions.
| Value  | Permission |
| ------------- | ------------- |
| ```4```| Read Permission|
| ```2```| Write Permission|
| ```1```| Execute Permission|

#### Examples of Using the Octal mode:
#### Suppose if we to give read and write permission to the file Owner. Read, write and executable permission to the Group. Read-only permission to the Other. They our command would be.
    chmod 674 [file_name]

#### Here.
#### 6 represent permission of file Owner which are (rw).
#### 7 represent permission of Group which are (rwx).
#### 4 represent permission of Other which is (r).
![image](https://github.com/PraveenReddy2510/90DaysOfDevOps/assets/127923130/f2d24389-f2c5-412a-9f40-0245bfd1be34)

![image](https://github.com/PraveenReddy2510/90DaysOfDevOps/assets/127923130/20145e99-3826-4d6b-8d4a-f009255a16fb)


