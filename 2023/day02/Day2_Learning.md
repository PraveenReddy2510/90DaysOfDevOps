# Day-2 Learning
Blog's referred:
- https://medium.com/cloud-native-daily/mastering-linux-for-devops-engineers-essential-commands-and-practices-for-success-a608a718069f
- https://medium.com/cloud-native-daily/mastering-linux-advanced-skills-for-devops-engineers-1a0c00fad159
- https://www.geeksforgeeks.org/cp-command-linux-examples/?ref=lbp

# File and Directory Management
## A. Basic linux commands
#### 1. The ls command is used to list files or directories in Linux and other Unix-based operating systems.
    ls
#### 2. Type the ls -l command to list the contents of the directory in a table format with columns including.
###### content permissions
###### number of links to the content
###### owner of the content
###### group owner of the content
###### size of the content in bytes
###### last modified date / time of the content
###### file or directory name
    ls -l
#### 3. Type the ls -a command to list files or directories including hidden files or directories. In Linux, anything that begins with a . is considered a hidden file.
    ls -a
#### 4. Type the ls *.txt (*extension type) command to list all files with same extension, in this case all .txt file will be listed in the directory.
    ls *.txt
#### 5. List the files and directories with index numbers in oders
    ls -i
#### 6. Type the ls -d */ command to list only directories.
    ls -d */
## B. Directoy commands
#### 1. Print work directory. Gives the present working directory.
    pwd
#### 2. Change directory to the provided path.
    cd <path-to-directory>
#### 3. Change directory to the home directory. ```cd ~ ``` or just  ```cd ``` 
    cd ~
    
    cd
#### 4. Go to the last working directory.
    cd -
#### 5. Change directory to one step back.
    cd ..
#### 6. Use ls ../.. to reach the root linux file directory
    cd ../..
#### 7. Use ls ../.. for contents two levels above.
    cd <path-to-directory>/<path-to-directory>
#### 8. Use to make a directory in a specific location
    mkdir  <directory-Name>
#### 9. Use to make a hidden directory (also . before a file to make it hidden)
    mkdir <.NewFolder>
#### 10. Use to make multiple directories at the same time.
    mkdir <directory-Name1> <directory-Name2> <directory-Name3> <directory-Name4>
#### 11. Use to make a new folder in a specific location
    mkdir /home/user/<My-directory>
#### 12. Use to make a nested directory
    mkdir -p  <directory-Name1>/<directory-Name2>/<directory-Name3>/<directory-Name4>
## C. Removing commands
#### 1. Used to remove the file from the directory
    rm <file-name>
#### 2. Used to remove the empty or non empty directories
    rm -r <file-name>
#### 3. Used to remove the empty directories
    rmdir <file-name>
#### 4. Used to remove all similar kind of extension files in one go. As below removes all .txt file in a directory.
    rm *.txt
## D. Copying commands
#### 1. Used to copy the file form one directory to another directory
    cp <source-file> <destination>
#### 2. Used to copy all similar kind of extension files in one go. As below copies all .txt file into a destination directory.
    cp *.txt <destination_directory>
#### 3. It copies the contents of the Source file to the Destination file.
###### If `Dest_file` does not exist, it is created.
###### If `Dest_file` already exists, it is overwritten without any warning.
    cp <Src-file> <Dest-file>
#### 4. It copies the contents of the Source file to the Destination file.
###### If `Dest_file` does not exist, it is created.
###### If `Dest_file` already exists, prompts for a response, if you press y or yes then it overwrites the file and with any other option leaves it uncopied.
    cp -i <Source_file> <Destination_file>
#### 5. It copies multiple files to a destination directory.
###### If the destination directory does not exist, it is created.
###### If it already exists, the files are overwritten without warning.
    cp <Src-file1> <Src-file2> <Src-file3> <Dest-directory>
#### 6. It copies all files from the source directory to the destination directory. `-r` or `-R` Option can be used
    cp -R <Src_directory> <Dest_directory>
#### 7. If the system is unable to open destination file for writing operation because the user doesn’t have writing permission for this file then by using -f option with cp command, destination file is deleted first and then copying of content is done from source to destination file.
    cp -f <Source_file> <Destination_file>
#### 8. With -p option cp preserves the following characteristics of each source file in the corresponding destination file: the time of the last data modification and the time of the last access, the ownership (only if it has permissions to do this), and the file permission-bits. 
##### Note: For the preservation of characteristics, you must be the root user of the system, otherwise characteristics change.
    cp -p <Source_file> <Destination_file>
## E. Moving commands






