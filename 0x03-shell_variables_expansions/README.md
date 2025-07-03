Week 13: Shell, init Files, Variables and Expansions
 Weight: 1280
 Project will start Jun 29, 2025 7:00 PM, must end by Jul 6, 2025 7:00 PM
 Checker was released at Jun 29, 2025 7:00 PM
 An auto review will be launched at the deadline




Important!
This is a graded project assignment that will contribute 12.5% to your overall grade. You must complete all the tasks provided after the quiz to ensure that you’re completing this assignment project. Each task contains its own set of instructions, so review them carefully.
 

This project explores environment variables, shell initialization files, and expansions in Linux. Learners will gain practical experience in creating and managing environment and local variables, configuring initialization files for custom settings, and using expansions to perform dynamic operations within the shell. By completing these tasks, learners will understand how to customize the shell environment and enhance their scripts with variables and expansions.

Instructions
Start by completing the quiz you see below. Once you complete the quiz, you can see the activity tasks mentioned in these instructions.
Complete the tasks one by one and follow the submission instructions below to submit your solution to the tasks.
How to Submit
Repository and Directory Setup

Ensure you have a GitHub account set up. If you are new to GitHub, use the GitHub website (https://github.com) to create your repository and upload files.
Create a new repository named system_engineering-devops.
Inside this repository, create a directory called 0x03-shell_variables_expansions where all your script files for this project will be stored.
Adding Files for Each Task

Each task requires a unique script file. Create each script in the 0x03-shell_variables_expansions directory, using the exact file names provided in each task description (e.g., 0-alias, 1-hello_you).
Submitting Your Project

Once all files are uploaded/created to the GitHub repository, verify that your directory structure and filenames match the requirements.
Using GitHub UI (Preferred Method)

You can easily upload files through GitHub’s web interface by clicking “Add file” > “Upload files” in your project directory.
For learners comfortable with the command line, feel free to use git commands to interact with GitHub.
Auto-Checking Process
At the end of the submission deadline, the auto-checker will review the tasks for correctness and award points. Ensure each script functions as expected and follows the naming conventions.


Important!
All scripts must be exactly two lines long.
Scripts should end with a new line.
All your files must have this as the first line. This will enable the checker to execute your files.
#!/bin/bash
 



Quiz questions
Great! You've completed the quiz successfully! Keep going! (Show quiz)
Tasks
0. <o>
mandatory

The objective of this task is to ensure that you understand what aliases are and how to create them.

Create a script that creates an alias.

Name: ls
Value: rm *
Here is an example illustrating how you will use the script you create and how it will behave when you execute it.

julien@ubuntu:/tmp/0x03$ ls
0-alias  file1  file2
julien@ubuntu:/tmp/0x03$ source ./0-alias 
julien@ubuntu:/tmp/0x03$ ls
julien@ubuntu:/tmp/0x03$ \ls
julien@ubuntu:/tmp/0x03$ 
If you know how to create an alias, then all the task is asking of you is to write a simple bash script which when executed will create a new alias.

The example shown above illustrates how you will use the script that you create. Before adding your alias, the ls comand will list all files in the current directory. But as soon as the you create the alias for ls, executing it will remove all files in the directory.

NB: If any of the checks are failing, try the following:

Review the output of the checker and try to understand what is not working
Confirm that you have the right repository name on GitHub
Confirm that you have the right directory name (remember the naming is case sensitive)
Confirm that you have a README.md file in root of the repository and another one in the root of the directory and more importantly these files should not be empty.
Repo:

GitHub repository: system_engineering-devops
Directory: 0x03-shell_variables_expansions
File: 0-alias
1. Hello you
mandatory

The objective of this task is to ensure that you know how to find the current Linux user. If you know the command for checking the current user then you just need to create a simple bash script that when executed, will show a greeting to the current user.
Create a script that prints hello user, where user is the current Linux user.

Here is an example illustrating how your script should behave when executed.

julien@ubuntu:/tmp/0x03$ id
uid=1000(julien) gid=1000(julien) groups=1000(julien),4(adm),24(cdrom),27(sudo),30(dip),46(plugdev),113(lpadmin),128(sambashare)
julien@ubuntu:/tmp/0x03$ chmod +x ./1-hello_you 
julien@ubuntu:/tmp/0x03$ ./1-hello_you 
hello julien
julien@ubuntu:/tmp/0x03$ 
Repo:

GitHub repository: system_engineering-devops
Directory: 0x03-shell_variables_expansions
File: 1-hello_you
2. The path to success is to take massive, determined action
mandatory

Add /action to the PATH. /action should be the last directory the shell looks into when looking for a program.
julien@ubuntu:/tmp/0x03$ echo $PATH
/home/julien/bin:/home/julien/.local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/games:/usr/local/games:/snap/bin
julien@ubuntu:/tmp/0x03$ source ./2-path 
julien@ubuntu:/tmp/0x03$ echo $PATH
/home/julien/bin:/home/julien/.local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/games:/usr/local/games:/snap/bin:/action
julien@ubuntu:/tmp/0x03$ 
Repo:

GitHub repository: system_engineering-devops
Directory: 0x03-shell_variables_expansions
File: 2-path
3. If the path be beautiful, let us not ask where it leads
mandatory

Create a script that counts the number of directories in the PATH.
julien@ubuntu:/tmp/0x03$ echo $PATH
/home/julien/bin:/home/julien/.local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/games:/usr/local/games:/snap/bin
julien@ubuntu:/tmp/0x03$ . ./3-paths 
11
julien@ubuntu:/tmp/0x03$ PATH=/home/julien/bin:/home/julien/.local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/games:/usr/local/games:/snap/bin:::::/hello
julien@ubuntu:/tmp/0x03$ . ./3-paths 
12
julien@ubuntu:/tmp/0x03$ 
Repo:

GitHub repository: system_engineering-devops
Directory: 0x03-shell_variables_expansions
File: 3-paths
4. Global variables
mandatory

Create a script that lists environment variables.
julien@ubuntu:/tmp/0x03$ source ./4-global_variables
CC=gcc
CDPATH=.:~:/usr/local:/usr:/
CFLAGS=-O2 -fomit-frame-pointer
COLORTERM=gnome-terminal
CXXFLAGS=-O2 -fomit-frame-pointer
DISPLAY=:0
DOMAIN=hq.garrels.be
e=
TOR=vi
FCEDIT=vi
FIGNORE=.o:~
G_BROKEN_FILENAMES=1
GDK_USE_XFT=1
GDMSESSION=Default
GNOME_DESKTOP_SESSION_ID=Default
GTK_RC_FILES=/etc/gtk/gtkrc:/nethome/franky/.gtkrc-1.2-gnome2
GWMCOLOR=darkgreen
GWMTERM=xterm
HISTFILESIZE=5000
history_control=ignoredups
HISTSIZE=2000
HOME=/nethome/franky
HOSTNAME=octarine.hq.garrels.be
INPUTRC=/etc/inputrc
IRCNAME=franky
JAVA_HOME=/usr/java/j2sdk1.4.0
LANG=en_US
LDFLAGS=-s
LD_LIBRARY_PATH=/usr/lib/mozilla:/usr/lib/mozilla/plugins
LESSCHARSET=latin1
LESS=-edfMQ
LESSOPEN=|/usr/bin/lesspipe.sh %s
LEX=flex
LOCAL_MACHINE=octarine
LOGNAME=franky
[...]
julien@ubuntu:/tmp/0x03$ 
Repo:

GitHub repository: system_engineering-devops
Directory: 0x03-shell_variables_expansions
File: 4-global_variables
5. Local variables
mandatory

Create a script that lists all local variables and environment variables, and functions.
julien@ubuntu:/tmp/0x03$ . ./5-local_variables
BASH=/bin/bash
BASHOPTS=checkwinsize:cmdhist:complete_fullquote:expand_aliases:extglob:extquote:force_fignore:histappend:interactive_comments:progcomp:promptvars:sourcepath
BASH_ALIASES=()
BASH_ARGC=()
BASH_ARGV=()
BASH_CMDS=()
BASH_COMPLETION_COMPAT_DIR=/etc/bash_completion.d
BASH_LINENO=()
BASH_REMATCH=()
BASH_SOURCE=()
BASH_VERSINFO=([0]="4" [1]="3" [2]="46" [3]="1" [4]="release" [5]="x86_64-pc-linux-gnu")
BASH_VERSION='4.3.46(1)-release'
CLUTTER_IM_MODULE=xim
COLUMNS=133
COMPIZ_CONFIG_PROFILE=ubuntu
COMP_WORDBREAKS=$' \t\n"\'><=;|&(:'
DBUS_SESSION_BUS_ADDRESS=unix:abstract=/tmp/dbus-Fg27Lr20bq
DEFAULTS_PATH=/usr/share/gconf/ubuntu.default.path
DESKTOP_SESSION=ubuntu
[...]
julien@ubuntu:/tmp/0x03$ 
Repo:

GitHub repository: system_engineering-devops
Directory: 0x03-shell_variables_expansions
File: 5-local_variables
6. Local variable
mandatory

Create a script that creates a new local variable.
Name: BEST
Value: School
Repo:

GitHub repository: system_engineering-devops
Directory: 0x03-shell_variables_expansions
File: 6-create_local_variable
7. Global variable
mandatory

Create a script that creates a new global variable.
Name: BEST
Value: School
Repo:

GitHub repository: system_engineering-devops
Directory: 0x03-shell_variables_expansions
File: 7-create_global_variable
8. Every addition to true knowledge is an addition to human power
mandatory

Write a script that prints the result of the addition of 128 with the value stored in the environment variable TRUEKNOWLEDGE, followed by a new line.
julien@production-503e7013:~$ export TRUEKNOWLEDGE=1209
julien@production-503e7013:~$ ./8-true_knowledge | cat -e
1337$
julien@production-503e7013:~$
Repo:

GitHub repository: system_engineering-devops
Directory: 0x03-shell_variables_expansions
File: 8-true_knowledge
9. Divide and rule
mandatory

Write a script that prints the result of POWER divided by DIVIDE, followed by a new line.
POWER and DIVIDE are environment variables
julien@production-503e7013:~$ export POWER=42784
julien@production-503e7013:~$ export DIVIDE=32
julien@production-503e7013:~$ ./9-divide_and_rule | cat -e
1337$
julien@production-503e7013:~$
Repo:

GitHub repository: system_engineering-devops
Directory: 0x03-shell_variables_expansions
File: 9-divide_and_rule
10. Love is anterior to life, posterior to death, initial of creation, and the exponent of breath
mandatory

Write a script that displays the result of BREATH to the power LOVE
BREATH and LOVE are environment variables
The script should display the result, followed by a new line
julien@production-503e7013:~/$ export BREATH=4
julien@production-503e7013:~/$ export LOVE=3
julien@production-503e7013:~/$ ./10-love_exponent_breath
64
julien@production-503e7013:~/$
Repo:

GitHub repository: system_engineering-devops
Directory: 0x03-shell_variables_expansions
File: 10-love_exponent_breath
