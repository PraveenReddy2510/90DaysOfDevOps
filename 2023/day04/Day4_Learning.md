# Day-4 Learning
Blog's referred:
- https://medium.com/cloud-native-daily/mastering-linux-for-devops-engineers-essential-commands-and-practices-for-success-a608a718069f
- https://medium.com/cloud-native-daily/mastering-linux-advanced-skills-for-devops-engineers-1a0c00fad159
- https://www.geeksforgeeks.org/cat-command-in-linux-with-examples/

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







