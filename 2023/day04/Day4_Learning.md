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

### What is Shell?
#### A shell is a special user program that provides an interface for the user to use operating system services. Shell accepts human-readable commands from users and converts them into something which the kernel can understand. It is a command language interpreter that executes commands read from input devices such as keyboards or from files. The shell gets started when the user ```logs in``` or ```starts the terminal```.
![image](https://github.com/PraveenReddy2510/90DaysOfDevOps/assets/127923130/4d65b90c-e011-4677-8fc9-1b11a7751264)
##### Shell is broadly classified into two categories –
##### 1. Command Line Shell
##### 2. Graphical shell
------------------------------------------------------------------------------------------
#### 1. Command Line Shell
##### Shell can be accessed by users using a command line interface. A special program called Terminal in Linux/macOS, or Command Prompt in Windows OS is provided to type in the human-readable commands such as “cat”, “ls” etc. and then it is being executed. The result is then displayed on the terminal to the user. A terminal in Ubuntu 16.4 system looks like this –
![image](https://github.com/PraveenReddy2510/90DaysOfDevOps/assets/127923130/a162c316-a501-4f27-b6db-9cea956675ff)

###### In the above screenshot ```ls``` command, it will list all the files in the current working directory.
##### Working with a command line shell is a bit difficult for beginners because it’s hard to memorize so many commands. ```It is very powerful```; it allows users to store commands in a file and execute them together. This way any repetitive task can be easily automated. These files are usually called ```batch files in Windows``` and ```Shell Scripts in Linux/macOS systems```.

#### 2. Graphical Shells
##### Graphical shells provide means for manipulating programs based on the graphical user interface (GUI), by allowing for operations such as opening, closing, moving, and resizing windows, as well as switching focus between windows. Window OS or Ubuntu OS can be considered as a good example which provides GUI to the user for interacting with the program. Users do not need to type in commands for every action. A typical GUI in the Ubuntu system –
![image](https://github.com/PraveenReddy2510/90DaysOfDevOps/assets/127923130/387accb4-b74d-4657-94f4-9999e03207fc)

#### There are several shells are available for Linux systems like –
- BASH (Bourne Again SHell) – It is the most widely used shell in Linux systems. It is used as default login shell in Linux systems and in macOS. It can also be installed on Windows OS.
- CSH (C SHell) – The C shell’s syntax and its usage are very similar to the C programming language.
- KSH (Korn SHell) – The Korn Shell was also the base for the POSIX Shell standard specifications etc.
###### ```Note```: Each shell does the same job but understands different commands and provides different built-in functions.
