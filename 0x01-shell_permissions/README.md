
This project focuses on understanding and managing file permissions in Linux, a key component of system security. Learners will explore the basics of file ownership, user roles, and permission settings, including changing permissions for files and directories. Through hands-on tasks, students will practice setting, modifying, and verifying permissions, ensuring they are well-versed in controlling access to files and directories within the Linux command line.
Instructions

    Start by completing the quiz you see below. Once you complete the quiz, you can see the activity tasks mentioned in these instructions.
    Complete the tasks one by one and follow the submission instructions below to submit your solution to the tasks.

How to Submit

    Repository and Directory Setup
        Ensure you have a GitHub account set up. If you are new to GitHub, use the GitHub website (https://github.com) to create your repository and upload files.
        Create a new repository named system_engineering-devops.
        Inside this repository, create a directory called 0x01-shell_permissions where all your script files for this project will be stored.

    Adding Files for Each Task
        Each task requires a unique script file. Create each script in the 0x01-shell_permissions directory, using the exact file names provided in each task description (e.g., 0-iam_betty, 1-who_am_i).
        Make sure each script is executable. You can set file permissions directly on GitHub or, if using the command line, run: bash chmod +x filename

    Submitting Your Project
        Once all files are uploaded to the GitHub repository, verify that your directory structure and filenames match the requirements.

    Using GitHub UI (Preferred Method)
        You can easily create or upload files through GitHub’s web interface by clicking “Add file” > “Upload files” in your project directory.
        For learners comfortable with the command line, feel free to use git commands to interact with GitHub.

Auto-Checking Process

At the end of the submission deadline, the auto-checker will review the tasks for correctness and award points. Ensure each script functions as expected and follows the naming conventions.

Important!
All your files must have this as the first line. This will enable the checker to execute your files.

#!/bin/bash


Quiz questions
Great! You've completed the quiz successfully! Keep going! (Show quiz)
Tasks
0. My Name Is Betty
mandatory
Score: 0.0% (Checks completed: 0.0%)

Create a script that switches the current user to the user betty.

    You should use exactly 8 characters for your command (+1 character for the new line).
    You can assume that the user betty will exist when we will run your script.

Example:

julien@ubuntu:/tmp/h$ tail -1 0-iam_betty | wc -c
9
julien@ubuntu:/tmp/h$

Repo:

    GitHub repository: system_engineering-devops
    Directory: 0x01-shell_permissions
    File: 0-iam_betty

1. Who Am I
mandatory
Score: 0.0% (Checks completed: 0.0%)

Write a script that prints the effective username of the current user.

Example:

julien@ubuntu:/tmp/h$ ./1-who_am_i
julien
julien@ubuntu:/tmp/h$ 

Repo:

    GitHub repository: system_engineering-devops
    Directory: 0x01-shell_permissions
    File: 1-who_am_i

2. Groups
mandatory
Score: 0.0% (Checks completed: 0.0%)

Write a script that prints all the groups the current user is part of.

Example:

julien@ubuntu:/tmp/h$ ./2-groups
julien adm cdrom sudo dip plugdev lpadmin sambashare
julien@ubuntu:/tmp/h$ 

Important note: Depending on the user, you’ll get a different output.

Repo:

    GitHub repository: system_engineering-devops
    Directory: 0x01-shell_permissions
    File: 2-groups

3. New Owner
mandatory
Score: 0.0% (Checks completed: 0.0%)

Write a script that changes the owner of the file hello to the user betty.

Example:

julien@ubuntu:/tmp/h$ ls -l
total 4
-rwxrw-r-- 1 julien julien 30 Sep 20 14:23 3-new_owner
-rw-rw-r-- 1 julien julien  0 Sep 20 14:18 hello
julien@ubuntu:/tmp/h$ sudo ./3-new_owner 
julien@ubuntu:/tmp/h$ ls -l
total 4
-rwxrw-r-- 1 julien julien 30 Sep 20 14:23 3-new_owner
-rw-rw-r-- 1 betty  julien  0 Sep 20 14:18 hello
julien@ubuntu:/tmp/h$

Repo:

    GitHub repository: system_engineering-devops
    Directory: 0x01-shell_permissions
    File: 3-new_owner

4. Empty!
mandatory
Score: 0.0% (Checks completed: 0.0%)

Write a script that creates an empty file called hello.

Repo:

    GitHub repository: system_engineering-devops
    Directory: 0x01-shell_permissions
    File: 4-empty

5. Execute
mandatory
Score: 0.0% (Checks completed: 0.0%)

Write a script that adds execute permission to the owner of the file hello.

    The file hello will be in the working directory.

Example:

julien@ubuntu:/tmp/h$ ls -l
total 8
-rwxrw-r-- 1 julien julien 28 Sep 20 14:26 5-execute
-rw-rw-r-- 1 julien julien 23 Sep 20 14:25 hello
julien@ubuntu:/tmp/h$ ./hello
bash: ./hello: Permission denied
julien@ubuntu:/tmp/h$ ./5-execute 
julien@ubuntu:/tmp/h$ ls -l
total 8
-rwxrw-r-- 1 julien julien 28 Sep 20 14:26 5-execute
-rwxrw-r-- 1 julien julien 23 Sep 20 14:25 hello
julien@ubuntu:/tmp/h$ 

Repo:

    GitHub repository: system_engineering-devops
    Directory: 0x01-shell_permissions
    File: 5-execute

6. James Bond
mandatory
Score: 0.0% (Checks completed: 0.0%)

Write a script that sets the permission to the file hello as follows:

    Owner: no permission at all
    Group: no permission at all
    Other users: all the permissions

The file hello will be in the working directory You are not allowed to use commas for this script

julien@ubuntu:/tmp/h$ ls -l
total 8
-rwxrw-r-- 1 julien julien 28 Sep 20 14:40 8-James_Bond
-rwxr-x--x 1 julien julien 23 Sep 20 14:25 hello
julien@ubuntu:/tmp/h$ ./8-James_Bond 
julien@ubuntu:/tmp/h$ ls -l
total 8
-rwxrw-r-- 1 julien julien 28 Sep 20 14:40 8-James_Bond
-------rwx 1 julien julien 23 Sep 20 14:25 hello
julien@ubuntu:/tmp/h$ 

Repo:

    GitHub repository: system_engineering-devops
    Directory: 0x01-shell_permissions
    File: 8-James_Bond

7. John Doe
mandatory
Score: 0.0% (Checks completed: 0.0%)

Write a script that sets the mode of the file hello to this:

-rwxr-x-wx 1 julien julien 23 Sep 20 14:25 hello

    The file hello will be in the working directory
    You are not allowed to use commas for this script

Repo:

    GitHub repository: system_engineering-devops
    Directory: 0x01-shell_permissions
    File: 9-John_Doe

8. Directories
mandatory
Score: 0.0% (Checks completed: 0.0%)

Create a script that adds execute permission to all subdirectories of the current directory for the owner, the group owner and all other users.

Regular files should not be changed.

julien@ubuntu:/tmp/h$ ls -l
total 20
-rwxrwxr-x 1 julien julien   24 Sep 20 14:53 11-directories_permissions
drwx------ 2 julien julien 4096 Sep 20 14:49 dir0
drwx------ 2 julien julien 4096 Sep 20 14:49 dir1
drwx------ 2 julien julien 4096 Sep 20 14:49 dir2
-rw-rw-r-- 1 julien julien   23 Sep 20 14:25 hello
julien@ubuntu:/tmp/h$ ./11-directories_permissions 
julien@ubuntu:/tmp/h$ ls -l
total 20
-rwxrwxr-x 1 julien julien   24 Sep 20 14:53 11-directories_permissions
drwx--x--x 2 julien julien 4096 Sep 20 14:49 dir0
drwx--x--x 2 julien julien 4096 Sep 20 14:49 dir1
drwx--x--x 2 julien julien 4096 Sep 20 14:49 dir2
-rw-rw-r-- 1 julien julien   23 Sep 20 14:25 hello
julien@ubuntu:/tmp/h$ 

Repo:

    GitHub repository: system_engineering-devops
    Directory: 0x01-shell_permissions
    File: 11-directories_permissions

9. More directories
mandatory
Score: 0.0% (Checks completed: 0.0%)

Create a script that creates a directory called my_dir with permissions 751 in the working directory.

julien@ubuntu:/tmp/h$ ls -l
total 20
-rwxrwxr-x 1 julien julien   39 Sep 20 14:59 12-directory_permissions
drwx--x--x 2 julien julien 4096 Sep 20 14:49 dir0
drwx--x--x 2 julien julien 4096 Sep 20 14:49 dir1
drwx--x--x 2 julien julien 4096 Sep 20 14:49 dir2
-rw-rw-r-- 1 julien julien   23 Sep 20 14:25 hello
julien@ubuntu:/tmp/h$ ./12-directory_permission s
julien@ubuntu:/tmp/h$ ls -l
total 24
-rwxrwxr-x 1 julien julien   39 Sep 20 14:59 12-directory_permissions
drwx--x--x 2 julien julien 4096 Sep 20 14:49 dir0
drwx--x--x 2 julien julien 4096 Sep 20 14:49 dir1
drwx--x--x 2 julien julien 4096 Sep 20 14:49 dir2
drwxr-x--x 2 julien julien 4096 Sep 20 14:59 my_dir
-rw-rw-r-- 1 julien julien   23 Sep 20 14:25 hello
julien@ubuntu:/tmp/h$ 

Repo:

    GitHub repository: system_engineering-devops
    Directory: 0x01-shell_permissions
    File: 12-directory_permissions

10. Change group
mandatory
Score: 0.0% (Checks completed: 0.0%)

Write a script that changes the group owner to school for the file hello

    The file hello will be in the working directory

julien@ubuntu:/tmp/h$ ls -l
total 24
-rwxrwxr-x 1 julien julien   34 Sep 20 15:03 13-change_group
drwx--x--x 2 julien julien 4096 Sep 20 14:49 dir0
drwx--x--x 2 julien julien 4096 Sep 20 14:49 dir1
drwx--x--x 2 julien julien 4096 Sep 20 14:49 dir2
drwxr-x--x 2 julien julien 4096 Sep 20 14:59 my_dir
-rw-rw-r-- 1 julien julien   23 Sep 20 14:25 hello
julien@ubuntu:/tmp/h$ sudo ./13-change_group 
julien@ubuntu:/tmp/h$ ls -l
total 24
-rwxrwxr-x 1 julien julien      34 Sep 20 15:03 13-change_group
drwx--x--x 2 julien julien    4096 Sep 20 14:49 dir0
drwx--x--x 2 julien julien    4096 Sep 20 14:49 dir1
drwx--x--x 2 julien julien    4096 Sep 20 14:49 dir2
drwxr-x--x 2 julien julien    4096 Sep 20 14:59 my_dir
-rw-rw-r-- 1 julien school   23 Sep 20 14:25 hello
julien@ubuntu:/tmp/h$ 

Repo:

    GitHub repository: system_engineering-devops
    Directory: 0x01-shell_permissions
    File: 13-change_grou
