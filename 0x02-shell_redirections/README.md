
Week 12: Shell—I/O Redirections, and Filters

    Weight: 1280
    Project will start Jun 15, 2025 7:00 PM, must end by Jun 29, 2025 7:00 PM
    Checker was released at Jun 15, 2025 7:00 PM
    An auto review will be launched at the deadline

Important!
This is a graded project assignment that will contribute 12.5% to your overall grade. You must complete all the tasks provided after the quiz to ensure that you’re completing this assignment project. Each task contains its own set of instructions, so review them carefully.


This project introduces learners to input and output redirections and essential text-processing commands in Linux. Through hands-on tasks, students will gain practical experience in redirecting command output, reading from files, and using common filters like cat, head, tail, sort, and uniq. By the end of this project, learners will be able to control where output goes, manage errors, and combine commands with pipes for efficient data processing.
Instructions

    Start by completing the quiz you see below. Once you complete the quiz, you can see the activity tasks mentioned in these instructions.
    Complete the tasks one by one and follow the submission instructions below to submit your solution to the tasks.

How to Submit

    Repository and Directory Setup
        Ensure you have a GitHub account set up. If you are new to GitHub, use the GitHub website (https://github.com) to create your repository and upload files.
        Create a new repository named system_engineering-devops.
        Inside this repository, create a directory called 0x02-shell_redirections where all your script files for this project will be stored.

    Adding Files for Each Task
        Each task requires a unique script file. Create each script in the 0x02-shell_redirections directory, using the exact file names provided in each task description (e.g., 0-helloworld, 1-confusedsmiley).

    Submitting Your Project
        Once all files are uploaded to the GitHub repository, verify that your directory structure and filenames match the requirements.

    Using GitHub UI (Preferred Method)
        You can easily upload files through GitHub’s web interface by clicking “Add file” > “Upload files” in your project directory.
        For learners comfortable with the command line, feel free to use git commands to interact with GitHub.

Auto-Checking Process

At the end of the submission deadline, the auto-checker will review the tasks for correctness and award points. Ensure each script functions as expected and follows the naming conventions.

Important!
All your files must have this as the first line. This will enable the checker to execute your files.

#!/bin/bash


Quiz questions
Great! You've completed the quiz successfully! Keep going! (Show quiz)
Tasks
0. Hello World
mandatory

Write a script that prints “Hello, World”, followed by a new line to the standard output.

Example:

julien@ubuntu:/tmp/h$ ./0-hello_world 
Hello, World
julien@ubuntu:/tmp/h$ ./0-hello_world | cat -e
Hello, World$
julien@ubuntu:/tmp/h$ 

Repo:

    GitHub repository: system_engineering-devops
    Directory: 0x02-shell_redirections
    File: 0-hello_world

1. Confused Smiley
mandatory

Write a script that displays a confused smiley "(Ôo)'.

Example:

julien@ubuntu:/tmp/h$ ./1-confused_smiley 
"(Ôo)'
julien@ubuntu:/tmp/h$ 

Repo:

    GitHub repository: system_engineering-devops
    Directory: 0x02-shell_redirections
    File: 1-confused_smiley

2. Let's Display a File
mandatory

Display the content of the /etc/passwd file.

Example:

$ ./2-hellofile
##
# User Database
#
# Note that this file is consulted directly only when the system is running
# in single-user mode. At other times this information is provided by
# Open Directory.
#
# See the opendirectoryd(8) man page for additional information about
# Open Directory.
##
nobody:*:-2:-2:Unprivileged User:/var/empty:/usr/bin/false
root:*:0:0:System Administrator:/var/root:/bin/sh
daemon:*:1:1:System Services:/var/root:/usr/bin/false
_uucp:*:4:4:Unix to Unix Copy Protocol:/var/spool/uucp:/usr/sbin/uucico
_taskgated:*:13:13:Task Gate Daemon:/var/empty:/usr/bin/false
_networkd:*:24:24:Network Services:/var/networkd:/usr/bin/false
_installassistant:*:25:25:Install Assistant:/var/empty:/usr/bin/false
_lp:*:26:26:Printing Services:/var/spool/cups:/usr/bin/false
_postfix:*:27:27:Postfix Mail Server:/var/spool/postfix:/usr/bin/false
_scsd:*:31:31:Service Configuration Service:/var/empty:/usr/bin/false
_ces:*:32:32:Certificate Enrollment Service:/var/empty:/usr/bin/false
_mcxalr:*:54:54:MCX AppLaunch:/var/empty:/usr/bin/false
_krbfast:*:246:-2:Kerberos FAST Account:/var/empty:/usr/bin/false
$

Repo:

    GitHub repository: system_engineering-devops
    Directory: 0x02-shell_redirections
    File: 2-hellofile

3. What About 2?
mandatory

Display the content of /etc/passwd and /etc/hosts.

Example:

$ ./3-twofiles
##
# User Database
#
# Note that this file is consulted directly only when the system is running
# in single-user mode. At other times this information is provided by
# Open Directory.
#
# See the opendirectoryd(8) man page for additional information about
# Open Directory.
##
nobody:*:-2:-2:Unprivileged User:/var/empty:/usr/bin/false
root:*:0:0:System Administrator:/var/root:/bin/sh
daemon:*:1:1:System Services:/var/root:/usr/bin/false
##
# Host Database
#
# localhost is used to configure the loopback interface
# when the system is booting. Do not change this entry.
##
127.0.0.1   localhost
255.255.255.255 broadcasthost
::1 localhost
$

Repo:

    GitHub repository: system_engineering-devops
    Directory: 0x02-shell_redirections
    File: 3-twofiles

4. Last Lines of a File
mandatory

Display the last 10 lines of /etc/passwd.

Example:

$ ./4-lastlines
_assetcache:*:235:235:Asset Cache Service:/var/empty:/usr/bin/false
_coremediaiod:*:236:236:Core Media IO Daemon:/var/empty:/usr/bin/false
_launchservicesd:*:239:239:_launchservicesd:/var/empty:/usr/bin/false
_iconservices:*:240:240:IconServices:/var/empty:/usr/bin/false
_distnote:*:241:241:DistNote:/var/empty:/usr/bin/false
_nsurlsessiond:*:242:242:NSURLSession Daemon:/var/db/nsurlsessiond:/usr/bin/false
_nsurlstoraged:*:243:243:NSURLStorage Daemon:/var/empty:/usr/bin/false
_displaypolicyd:*:244:244:Display Policy Daemon:/var/empty:/usr/bin/false
_astris:*:245:245:Astris Services:/var/db/astris:/usr/bin/false
_krbfast:*:246:-2:Kerberos FAST Account:/var/empty:/usr/bin/false

Tips: “Think of it as a cat, what is at the end of it?”

Repo:

    GitHub repository: system_engineering-devops
    Directory: 0x02-shell_redirections
    File: 4-lastlines

5. I'd Prefer the First Ones, Actually
mandatory

Display the first 10 lines of /etc/passwd.

Example:

$ ./5-firstlines
##
# User Database
#
# Note that this file is consulted directly only when the system is running
# in single-user mode. At other times this information is provided by
# Open Directory.
#
# See the opendirectoryd(8) man page for additional information about
# Open Directory.
##
$

Repo:

    GitHub repository: system_engineering-devops
    Directory: 0x02-shell_redirections
    File: 5-firstlines

6. Line #2
mandatory

Write a script that displays the third line of the /file iacta.

The file iacta will be in the working directory.

Important! You’re not allowed to use sed!

Example:

julien@ubuntu:/tmp/h$ cat iacta 
Alea iacta est

Alea iacta est ("The die is cast") is a Latin phrase attributed by Suetonius
(as iacta alea est) to Julius Caesar on January 10, 49 BC
as he led his army across the Rubicon river in Northern Italy. With this step,
he entered Italy at the head of his army in defiance of the Senate and began
his long civil war against Pompey and the Optimates. The phrase has been
adopted in Italian (Il dado è tratto), Romanian (Zarurile au fost aruncate),
Spanish (La suerte está echada), French (Les dés sont jetés), Portuguese (A
sorte está lançada), Dutch (De teerling is geworpen),
German (Der Würfel ist gefallen), Hungarian (A kocka el van vetve) and many other languages to
indicate that events have passed a point of no return.

Read more: https://en.wikipedia.org/wiki/Alea_iacta_est
julien@ubuntu:/tmp/h$ ./6-third_line 
Alea iacta est ("The die is cast") is a Latin phrase attributed by Suetonius
julien@ubuntu:/tmp/h$ 

Take note! The output will differ, depending on the content of the file iacta.

Repo:

    GitHub repository: system_engineering-devops
    Directory: 0x02-shell_redirections
    File: 6-third_line

7. It's a Good File That Cuts Iron Without Making a Noise
mandatory

Write a shell script that creates a file named exactly *\'"Best School"\'\*$\?*****:), containing the text Best School, and ending with a new line.

Example:

julien@ubuntu:~/shell$ ls && ./7-file && ls -l && cat -e \\*
0-mac_and_cheese 7-file 7-file~ Makefile
total 20
-rwxrw-r-- 1 julien julien 79 Jan 20 06:24 0-mac_and_cheese
-rwxrw-r-- 1 julien julien 90 Jan 20 06:40 7-file
-rwxrw-r-- 1 julien julien 69 Jan 20 06:37 7-file~
-rw-rw-r-- 1 julien julien 14 Jan 20 06:38 Makefile
-rw-rw-r-- 1 julien julien 17 Jan 20 06:40 '\*\\'"Best School"\'\\*$\?\*\*\*\*\*:)'
Best School$
julien@ubuntu:~/shell$

Repo:

    GitHub repository: system_engineering-devops
    Directory: 0x02-shell_redirections
    File: 7-file

8. Save Current State of Directory
mandatory

Write a script that writes into the file lscwdcontent the result of the command ls -la. If the file lscwdcontent already exists, it should be overwritten. If the file lscwdcontent does not exist, create it.

Example:

julien@ubuntu:/tmp/h$ ls -la
total 20
drwxrwxr-x  2 julien julien 4096 Sep 20 18:18 .
drwxrwxrwt 13 root   root   4096 Sep 20 18:18 ..
-rwxrw-r--  1 julien julien   36 Sep 20 18:18 8-cwd_state
-rw-rw-r--  1 betty  julien   23 Sep 20 14:25 hello
-rw-rw-r--  1 julien julien  926 Sep 20 17:52 iacta
julien@ubuntu:/tmp/h$ ./8-cwd_state 
julien@ubuntu:/tmp/h$ ls -la
total 24
drwxrwxr-x  2 julien julien 4096 Sep 20 18:18 .
drwxrwxrwt 13 root   root   4096 Sep 20 18:18 ..
-rwxrw-r--  1 julien julien   36 Sep 20 18:18 8-cwd_state
-rw-rw-r--  1 betty  julien   23 Sep 20 14:25 hello
-rw-rw-r--  1 julien julien  926 Sep 20 17:52 iacta
-rw-rw-r--  1 julien julien  329 Sep 20 18:18 ls_cwd_content
julien@ubuntu:/tmp/h$ cat ls_cwd_content 
total 20
drwxrwxr-x  2 julien julien 4096 Sep 20 18:18 .
drwxrwxrwt 13 root   root   4096 Sep 20 18:18 ..
-rwxrw-r--  1 julien julien   36 Sep 20 18:18 8-cwd_state
-rw-rw-r--  1 betty  julien   23 Sep 20 14:25 hello
-rw-rw-r--  1 julien julien  926 Sep 20 17:52 iacta
-rw-rw-r--  1 julien julien    0 Sep 20 18:18 ls_cwd_content
julien@ubuntu:/tmp/h$ 

Repo:

    GitHub repository: system_engineering-devops
    Directory: 0x02-shell_redirections
    File: 8-cwd_state

9. Duplicate the Last Line
mandatory

Write a script that duplicates the last line of the file iacta.

    The file iacta will be in the working directory.

Example:

julien@ubuntu:/tmp/h$ cat iacta 
Alea iacta est

Alea iacta est ("The die is cast") is a Latin phrase attributed by Suetonius
(as iacta alea est) to Julius Caesar on January 10, 49 BC
as he led his army across the Rubicon river in Northern Italy. With this step,
he entered Italy at the head of his army in defiance of the Senate and began
his long civil war against Pompey and the Optimates. The phrase has been
adopted in Italian (Il dado è tratto), Romanian (Zarurile au fost aruncate),
Spanish (La suerte está echada), French (Les dés sont jetés), Portuguese (A
sorte está lançada), Dutch (De teerling is geworpen),
German (Der Würfel ist gefallen), Hungarian (A kocka el van vetve) and many other languages to
indicate that events have passed a point of no return.

Read more: https://en.wikipedia.org/wiki/Alea_iacta_est
julien@ubuntu:/tmp/h$ ./9-duplicate_last_line 
julien@ubuntu:/tmp/h$ cat iacta 
Alea iacta est

Alea iacta est ("The die is cast") is a Latin phrase attributed by Suetonius
(as iacta alea est) to Julius Caesar on January 10, 49 BC
as he led his army across the Rubicon river in Northern Italy. With this step,
he entered Italy at the head of his army in defiance of the Senate and began
his long civil war against Pompey and the Optimates. The phrase has been
adopted in Italian (Il dado è tratto), Romanian (Zarurile au fost aruncate),
Spanish (La suerte está echada), French (Les dés sont jetés), Portuguese (A
sorte está lançada), Dutch (De teerling is geworpen),
German (Der Würfel ist gefallen), Hungarian (A kocka el van vetve) and many other languages to
indicate that events have passed a point of no return.

Read more: https://en.wikipedia.org/wiki/Alea_iacta_est
Read more: https://en.wikipedia.org/wiki/Alea_iacta_est
julien@ubuntu:/tmp/h$ 

Repo:

    GitHub repository: system_engineering-devops
    Directory: 0x02-shell_redirections
    File: 9-duplicate_last_line

10. No More Javascript
mandatory

Write a script that deletes all the regular files (not the directories) with a .js extension that are present in the current directory and all its sub-folders.

Example:

julien@ubuntu:/tmp/h$ ls -lR
.:
total 24
-rwxrw-r-- 1 julien julien   49 Sep 20 18:29 10-no_more_js
drwxrwxr-x 2 julien julien 4096 Sep 20 18:23 dir1
drwxrwxr-x 2 julien julien 4096 Sep 20 18:24 dir.js
-rw-rw-r-- 1 betty  julien   23 Sep 20 14:25 hello
-rw-rw-r-- 1 julien julien  982 Sep 20 18:21 iacta
-rw-rw-r-- 1 julien julien  329 Sep 20 18:18 ls_cwd_content
-rw-rw-r-- 1 julien julien    0 Sep 20 18:23 main.js

./dir1:
total 0
-rw-rw-r-- 1 julien julien 0 Sep 20 18:23 code.js

./dir.js:
total 0
julien@ubuntu:/tmp/h$ ./10-no_more_js 
julien@ubuntu:/tmp/h$ ls -lR
.:
total 24
-rwxrw-r-- 1 julien julien   49 Sep 20 18:29 10-no_more_js
drwxrwxr-x 2 julien julien 4096 Sep 20 18:29 dir1
drwxrwxr-x 2 julien julien 4096 Sep 20 18:24 dir.js
-rw-rw-r-- 1 betty  julien   23 Sep 20 14:25 hello
-rw-rw-r-- 1 julien julien  982 Sep 20 18:21 iacta
-rw-rw-r-- 1 julien julien  329 Sep 20 18:18 ls_cwd_content

./dir1:
total 0

./dir.js:
total 0
julien@ubuntu:/tmp/h$ 

Repo:

    GitHub repository: system_engineering-devops
    Directory: 0x02-shell_redirections
    File: 10-no_more_js

