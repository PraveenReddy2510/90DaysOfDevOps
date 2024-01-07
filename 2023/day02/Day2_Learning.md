# Day-2 Learning
Blog's referred:
- https://medium.com/cloud-native-daily/mastering-linux-for-devops-engineers-essential-commands-and-practices-for-success-a608a718069f
- https://medium.com/cloud-native-daily/mastering-linux-advanced-skills-for-devops-engineers-1a0c00fad159

# File and Directory Management
## Basic linux commands
#### The ls command is used to list files or directories in Linux and other Unix-based operating systems.
    ls
#### Type the ls -l command to list the contents of the directory in a table format with columns including.
###### content permissions
###### number of links to the content
###### owner of the content
###### group owner of the content
###### size of the content in bytes
###### last modified date / time of the content
###### file or directory name
    ls -l
#### Type the ls -a command to list files or directories including hidden files or directories. In Linux, anything that begins with a . is considered a hidden file.
    ls -a
#### Type the ls *.txt (*extension type) command to list all files with same extension, in this case all .txt file will be listed in the directory.
    ls *.txt
#### List the files and directories with index numbers in oders
    ls -i
#### Type the ls -d */ command to list only directories.
    ls -d
## Directoy commands
#### Print work directory. Gives the present working directory.
    pwd
#### Change directory to the provided path.
    cd <path-to-directory>
#### Change directory to the home directory. ```cd ~ ``` or just  ```cd ``` 
    cd ~
    
    cd
#### Go to the last working directory.
    cd -
#### Change directory to one step back.
    cd ..
#### Use ls ../.. to reach the root linux file directory
    cd ../..
#### Use ls ../.. for contents two levels above.
    cd <path-to-directory>/<path-to-directory>
#### Use to make a directory in a specific location
    mkdir  <directory-Name>
#### Use to make a hidden directory (also . before a file to make it hidden)
    mkdir <.NewFolder>
#### Use to make multiple directories at the same time.
    mkdir <directory-Name1> <directory-Name2> <directory-Name3> <directory-Name4>
#### Use to make a new folder in a specific location
    mkdir /home/user/<My-directory>
#### Use to make a nested directory
    mkdir -p  <directory-Name1>/<directory-Name2>/<directory-Name3>/<directory-Name4>
#### Used to remove the file from the directory
    rm <file-name>
#### Used to remove the empty or non empty directories
    rm -r <file-name>
#### Used to remove the empty directories
    rmdir <file-name>
#### Used to copy the file form one directory to another directory
    cp <source-file> <destination>
#### It copies the contents of the Source file to the Destination file.
###### If `Dest_file` does not exist, it is created.
###### If `Dest_file` already exists, it is overwritten without any warning.
    cp <Src-file> <Dest-file>
#### It copies multiple files to a destination directory.
###### If the destination directory does not exist, it is created.
###### If it already exists, the files are overwritten without warning.
    cp <Src-file1> <Src-file2> <Src-file3> <Dest-directory>






