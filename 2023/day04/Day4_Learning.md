# Day-4 Learning
Blog's referred:
- https://medium.com/cloud-native-daily/mastering-linux-for-devops-engineers-essential-commands-and-practices-for-success-a608a718069f
- https://medium.com/cloud-native-daily/mastering-linux-advanced-skills-for-devops-engineers-1a0c00fad159
- https://www.geeksforgeeks.org/cat-command-in-linux-with-examples/
- https://www.geeksforgeeks.org/introduction-linux-shell-shell-scripting/
- https://www.youtube.com/watch?v=zsajhz2_50g&list=PLdpzxOOAlwvIZ7u-gtpX_bozrspUbTQ1S&pp=iAQB

# 2. Text Manipulation and Viewing
## A. ```cat``` Command (it is used for various file-related operations, allowing users to view, concatenate, create, copy, merge, and manipulate file contents.
#### 1. To View the Content of a Single File ```file_name```
    cat <file_name>
<img width="319" alt="image" src="https://github.com/PraveenReddy2510/90DaysOfDevOps/assets/127923130/766bc09c-a7f0-43a1-9dcb-d4f3a732aaa8">

#### 2. To View the Content of a multiple files ```file_name1``` & ```file_name2```
    cat <file_name1> <file_name2>
![image](https://github.com/PraveenReddy2510/90DaysOfDevOps/assets/127923130/655f1cc0-4c2c-49f1-8ace-2d2a03b11f42)

#### 3. To View the Content of a single/multiple files with line numbers ```file_name1``` & ```file_name2```
    cat -n <file_name1>

    cat -n <file_name1> <file_name2>
![image](https://github.com/PraveenReddy2510/90DaysOfDevOps/assets/127923130/6ff5c1dc-8546-43e7-a3c6-2ec44a2d500f)
#### 4. To create a new file or overwrite an existing file with new content.
    cat > <new_file_name1>
![image](https://github.com/PraveenReddy2510/90DaysOfDevOps/assets/127923130/6631802f-076d-4e1b-9536-30b40c1a1ba2)

    cat > <existing_file_name1>
![image](https://github.com/PraveenReddy2510/90DaysOfDevOps/assets/127923130/3c69ceca-b4ed-4c84-80ad-c14e414d54d5)

#### 5. To concatenate multiple files content into a single file.
    cat <existing_file_name1> <existing_file_name2> > <new_file_name1>
![image](https://github.com/PraveenReddy2510/90DaysOfDevOps/assets/127923130/d41327b8-1c2c-42ad-87e5-3b5e61d3c04b)

#### 6. To Append the Contents of One File to the End of Another File.
    cat <one_file_name> >> <another_file_name1>
![image](https://github.com/PraveenReddy2510/90DaysOfDevOps/assets/127923130/1746c658-95a6-4aa2-a574-87fed5ba294f)

#### 7. To Display Content in Reverse Order.
    tac <file_name>
![image](https://github.com/PraveenReddy2510/90DaysOfDevOps/assets/127923130/b4e9fa0a-fe3b-4c65-9d54-4f2c28a4509b)
#### 7. To Highlight the End of Line
    cat -E <file_name>
![image](https://github.com/PraveenReddy2510/90DaysOfDevOps/assets/127923130/fd0b0dce-be13-409a-8fd8-597071efc901)
#### 8. To Open Dashed Files (example: ```-flash```, ```-dashed_file```)
    cat -- <-dashed_file>
![image](https://github.com/PraveenReddy2510/90DaysOfDevOps/assets/127923130/644040eb-78b6-48b5-ba33-1c20a0691e49)
#### 9. To show the content in fit mode of CLI and ```MORE``` option to see next line by clicking enter for each line.
    cat <file_name> | more
![image](https://github.com/PraveenReddy2510/90DaysOfDevOps/assets/127923130/b80ba52a-a0a6-4ae2-941b-0d2247691853)
#### 10. To Append the content to the last line of exiting file
    cat >> <file_name>
![image](https://github.com/PraveenReddy2510/90DaysOfDevOps/assets/127923130/fbc85b47-dc51-4440-b172-07f05a47e5b7)

# Shell Scripting
## Shell Scripting used for automate the linux commands.
### We will discuss Linux shells and shell scripting so before understanding shell scripting we have to get familiar with the following terminologies:
- Kernel
- Shell
- Terminal
### What is Kernel?
#### The kernel is a computer program that is the core of a computer’s operating system, with complete control over everything in the system. It manages the following resources of the Linux system –
* File management
* Process management
* I/O management
* Memory management
* Device management etc.
#### It is often mistaken that Linus Torvalds has developed Linux OS, but actually, he is only responsible for the development of the Linux kernel.
#### Complete ```Linux system``` ```=``` ```Kernel``` ```+``` ```GNU system utilities and libraries``` ```+``` ```other management scripts``` ```+``` ```installation scripts```
![image](https://github.com/PraveenReddy2510/90DaysOfDevOps/assets/127923130/0a13f8fa-b28c-4004-a7ab-1b116de03eff)

