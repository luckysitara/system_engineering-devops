Week 14: Loops, Conditions, and Parsing
 Weight: 1280
 Project will start Jun 29, 2025 7:00 PM, must end by Jul 13, 2025 7:00 PM
 Checker was released at Jun 29, 2025 7:00 PM
 An auto review will be launched at the deadline




Important!
This is a graded project assignment that will contribute 12.5% to your overall grade. You must complete all the tasks provided after the quiz to ensure that you’re completing this assignment project. Each task contains its own set of instructions, so review them carefully.

This project introduces learners to loops, conditional statements, and basic input parsing in Bash scripting. Learners will develop skills in using control flow to automate repetitive tasks and handle decision-making in scripts. Through hands-on tasks, students will practice with for, while, and until loops, create conditional logic with if, elif, else, and use parsing techniques for handling input data. By the end of the project, learners will be able to build more dynamic and responsive shell scripts.

Instructions
You should be able to see below the activity tasks mentioned in these instructions.
Complete the tasks one by one and follow the submission instructions below to submit your solution to the tasks.
How to Submit
Repository and Directory Setup

Ensure you have a GitHub account set up. If you are new to GitHub, use the GitHub website (https://github.com) to create your repository and upload files.
Create a new repository named system_engineering-devops.
Inside this repository, create a directory called 0x04-loopsconditionsand_parsing where all your script files for this project will be stored.
Adding Files for Each Task

Each task requires a unique script file. Create each script in the 0x04-loopsconditionsand_parsing directory, using the exact file names provided in each task description (e.g., 0-RSApublickey.pub, 1-forbestschool).
Submitting Your Project

Once all files are uploaded to the GitHub repository, verify that your directory structure and filenames match the requirements.
Using GitHub UI (Preferred Method)

You can easily upload files through GitHub’s web interface by clicking “Add file” > “Upload files” in your project directory.
For learners comfortable with the command line, feel free to use git commands to interact with GitHub.
Auto-Checking Process
At the end of the submission deadline, the auto-checker will review the tasks for correctness and award points. Ensure each script functions as expected, follows the naming conventions, and includes required permissions.


Important!
All your files must have this as the first line. This will enable the checker to execute your files.
#!/bin/bash



Tasks
0. For Best School Loop
mandatory

In Bash scripting, loops are fundamental constructs that allow you to execute a block of code repeatedly. They are essential for automating repetitive tasks and processing collections of data. There are several types of loops, each suited for different scenarios.
The objective of this task is to ensure you understand and can implement a for loop in Bash to perform a repetitive action.

Task: Write a Bash script that displays the phrase “Best School” exactly 10 times.

Requirement: * You must use the for loop. * The while and until loops are forbidden for this task.

Here is an example illustrating how your script should behave when executed:

sylvain@ubuntu$ head -n 2 1-for_best_school 
#!/usr/bin/env bash
# This script is displaying "Best School" 10 times
sylvain@ubuntu$ ./1-for_best_school 
Best School
Best School
Best School
Best School
Best School
Best School
Best School
Best School
Best School
Best School
sylvain@ubuntu$ 
Take note!

The first line of your Bash script should be #!/usr/bin/env bash.
The second line should be a comment explaining what it’s doing.
Repo:

GitHub repository: system_engineering-devops
Directory: 0x04-loops_conditions_and_parsing
File: 1-for_best_school
1. While Best School Loop
mandatory

Following your work with the for loop, this task introduces another fundamental looping construct in Bash: the while loop. A while loop repeatedly executes a block of code as long as a specified condition remains true.
The objective of this task is to ensure you understand and can implement a while loop in Bash to perform a repetitive action.

Task: Write a Bash script that displays the phrase “Best School” exactly 10 times.

Requirements:

You must use the while loop.
The for and until loops are forbidden for this task.
Here is an example illustrating how your script should behave when executed:

sylvain@ubuntu$ ./2-while_best_school
Best School
Best School
Best School
Best School
Best School
Best School
Best School
Best School
Best School
Best School
sylvain@ubuntu$ 
Take note!

The first line of your Bash script should be #!/usr/bin/env bash.
The second line should be a comment explaining what it’s doing.
Repo:

GitHub repository: system_engineering-devops
Directory: 0x04-loops_conditions_and_parsing
File: 2-while_best_school
2. Until Best School Loop
mandatory

You’ve now worked with for and while loops. This task introduces the third common looping construct in Bash: the until loop. An until loop repeatedly executes a block of code as long as a specified condition remains false. It’s essentially the opposite of a while loop.
The objective of this task is to ensure you understand and can implement an until loop in Bash to perform a repetitive action.

Task: Write a Bash script that displays the phrase “Best School” exactly 10 times.

Requirements:

You must use the until loop.
The for and while loops are forbidden for this task.
Here is an example illustrating how your script should behave when executed:

sylvain@ubuntu$ ./3-until_best_school
Best School
Best School
Best School
Best School
Best School
Best School
Best School
Best School
Best School
Best School
sylvain@ubuntu$ 
Take note!

The first line of your Bash script should be #!/usr/bin/env bash.
The second line should be a comment explaining what it’s doing.
Repo:

GitHub repository: system_engineering-devops
Directory: 0x04-loops_conditions_and_parsing
File: 3-until_best_school
3. If 9, Say Hi!
mandatory

You’ve mastered basic loops. Now, let’s combine looping with conditional statements. An if statement allows your script to make decisions and execute different blocks of code based on whether a condition is true or false. This is crucial for creating dynamic and responsive scripts.
The objective of this task is to ensure you can integrate an if statement within a while loop to alter behavior based on a specific iteration.

Task: Write a Bash script that displays “Best School” 10 times. However, for the 9th iteration, your script should display “Best School” and then, on a new line, display “Hi”.

Requirements:

You must use the while loop.
The for and until loops are forbidden for this task.
You must use the if statement.
Here is an example illustrating how your script should behave when executed:

sylvain@ubuntu$ ./4-if_9_say_hi
Best School
Best School
Best School
Best School
Best School
Best School
Best School
Best School
Best School
Hi
Best School
sylvain@ubuntu$ 
Take note!

The first line of your Bash script should be #!/usr/bin/env bash.
The second line should be a comment explaining what it’s doing.
Repo:

GitHub repository: system_engineering-devops
Directory: 0x04-loops_conditions_and_parsing
File: 4-if_9_say_hi
4. 4 Bad Luck, 8 Is Your Chance
mandatory

Building on your understanding of if statements, this task introduces elif (else if) and else clauses. These allow for more complex conditional branching, enabling your script to handle multiple distinct conditions.
The objective of this task is to ensure you can use a while loop with a full if-elif-else structure to display different messages based on specific loop iterations.

Task: Write a Bash script that loops from 1 to 10 and:

Displays “bad luck” for the 4th loop iteration.
Displays “good luck” for the 8th loop iteration.
Displays “Best School” for all other iterations.
Requirements:

You must use the while loop.
The for and until loops are forbidden for this task.
You must use the if, elif, and else statements.
Here is an example illustrating how your script should behave when executed:

sylvain@ubuntu$ ./5-4_bad_luck_8_is_your_chance
Best School
Best School
Best School
bad luck
Best School
Best School
Best School
good luck
Best School
Best School
sylvain@ubuntu$ 
For the most curious:

8 in Chinese culture
4 in Chinese culture
Take note!

The first line of your Bash script should be #!/usr/bin/env bash.
The second line should be a comment explaining what it’s doing.
Repo:

GitHub repository: system_engineering-devops
Directory: 0x04-loops_conditions_and_parsing
File: 5-4_bad_luck_8_is_your_chance
5. Superstitious Numbers
mandatory

You’ve used if-elif-else for conditional logic. This task introduces another powerful conditional construct: the case statement. A case statement is particularly useful when you need to perform different actions based on the specific value of a single variable or expression. It provides a cleaner and often more readable alternative to a long chain of if-elif statements when dealing with multiple possible values.
The objective of this task is to ensure you understand and can implement a case statement within a while loop to display different messages based on specific loop iteration numbers.

Task: Write a Bash script that displays numbers from 1 to 20. For specific iterations, it should display additional “bad luck” messages:

Displays 4 and then “bad luck from China” for the 4th loop iteration.
Displays 9 and then “bad luck from Japan” for the 9th loop iteration.
Displays 17 and then “bad luck from Italy” for the 17th loop iteration.
For all other iterations, only the number should be displayed.
Requirements:

You must use the while loop.
The for and until loops are forbidden for this task.
You must use the case statement.
Here is an example illustrating how your script should behave when executed:

sylvain@ubuntu$ ./6-superstitious_numbers
1
2
3
4
bad luck from China
5
6
7
8
9
bad luck from Japan
10
11
12
13
14
15
16
17
bad luck from Italy
18
19
20
sylvain@ubuntu$ 
Take note!

The first line of your Bash script should be #!/usr/bin/env bash.
The second line should be a comment explaining what it’s doing.
Repo:

GitHub repository: system_engineering-devops
Directory: 0x04-loops_conditions_and_parsing
File: 6-superstitious_numbers
6. For ls
mandatory

This task combines your knowledge of for loops with file system manipulation and text processing. You’ll need to iterate through files and extract specific parts of their names.
The objective of this task is to ensure you can use a for loop to process items (like filenames) and apply string manipulation to achieve a specific output format.

Task: Write a Bash script that displays:

The content of the current directory.
In a list format (one item per line).
Where only the part of the name after the first dash (-) is displayed (refer to the example for clarity).
Requirements:

You must use the for loop.
The while and until loops are forbidden.
Your script must not display hidden files (files starting with a .).
Here is an example illustrating how your script should behave when executed:

sylvain@ubuntu$ ls
100-read_and_cut              1-for_best_school         6-superstitious_numbers
101-tell_the_story_of_passwd  2-while_best_school       7-clock
102-lets_parse_apache_logs    3-until_best_school       8-for_ls
103-dig_the-data              4-if_9_say_hi                  9-to_file_or_not_to_file
10-fizzbuzz                   5-4_bad_luck_8_is_your_chance
sylvain@ubuntu$  ./8-for_ls
read_and_cut
tell_the_story_of_passwd
lets_parse_apache_logs
dig_the-data
fizzbuzz
for_best_school
while_best_school
until_best_school
if_9_say_hi
4_bad_luck_8_is_your_chance
superstitious_numbers
clock
for_ls
to_file_or_not_to_file
sylvain@ubuntu$ 
Take note!

The first line of your Bash script should be #!/usr/bin/env bash.
The second line should be a comment explaining what it’s doing.
Repo:

GitHub repository: system_engineering-devops
Directory: 0x04-loops_conditions_and_parsing
File: 8-for_ls
7. To file, or not to file
mandatory

In shell scripting, it’s often necessary to check the properties of files or directories before performing operations on them. This ensures your scripts behave correctly and avoid errors. Bash provides various file test operators that allow you to check for existence, type, permissions, and size.
The objective of this task is to ensure you can use conditional statements (if and else) to test different properties of a file and print specific messages based on those tests.

Task: Write a Bash script that provides information about a file named school. Your script should perform the following checks and print the corresponding messages:

Check for existence:
* If the `school` file exists, print: `school file exists`
* If the `school` file does not exist, print: `school file does not exist`
If the file exists, then perform further checks:
* If the `school` file is empty, print: `school file is empty`
* If the `school` file is not empty, print: `school file is not empty`
* If the `school` file is a regular file (not a directory, symbolic link, etc.), print: `school is a regular file`
* If the `school` file is not a regular file (e.g., it's a directory), do not print anything for this specific check.
Requirements:

You must use if and else statements.
The case statement is forbidden for this task.
Here is an example illustrating how your script should behave when executed with different states of the school file:

sylvain@ubuntu$ file school
school: cannot open `school' (No such file or directory)
sylvain@ubuntu$ ./9-to_file_or_not_to_file 
school file does not exist
sylvain@ubuntu$ touch school
sylvain@ubuntu$ ./9-to_file_or_not_to_file 
school file exists
school file is empty
school is a regular file
sylvain@ubuntu$ echo 'betty' > school 
sylvain@ubuntu$ ./9-to_file_or_not_to_file 
school file exists
school file is not empty
school is a regular file
sylvain@ubuntu$ rm school 
sylvain@ubuntu$ mkdir school
sylvain@ubuntu$ ./9-to_file_or_not_to_file 
school file exists
school file is not empty
sylvain@ubuntu$ 
Take note!

The first line of your Bash script should be #!/usr/bin/env bash.
The second line should be a comment explaining what it’s doing.
Repo:

GitHub repository: system_engineering-devops
Directory: 0x04-loops_conditions_and_parsing
File: 9-to_file_or_not_to_file
