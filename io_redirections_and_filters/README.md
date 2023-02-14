Shell, I/O Redirections and filters

---------------------------------
QUIZ

Question #0
Which symbol should I use to redirect the standard output to a file (overwrite the file)?
>

Question #1
Which symbol should I use to redirect the standard output to a file (appending to the file)?
>>

Question #2
Which symbol should I use to redirect the error output to the standard output?
2>&1

Question #3
Which symbol should I use to start a comment?
#

Question #4
Which command should I use to display the entire file content?
cat

Question #5
Which command should I use to display the last 11 lines of a file?
tail-n 11 my_file

Question #6
Which symbol should I use to escape a special character?
\

---------------------------------
Tasks

0. Hello World
Write a script that prints “Hello, World”, followed by a new line to the standard output.
#bin/bash
echo "Hello, World"

1. Confused smiley
Write a script that displays a confused smiley "(Ôo)'.
#bin/bash
echo "\"(Ôo)'

2. Let's display a file
Display the content of the /etc/passwd file.
#bin/bash
cat /etc/passwd

3. What about 2?
Display the content of /etc/passwd and /etc/hosts
#bin/bash
echo /etc/passwd /etc/hosts

4. Last lines of a file
Display the last 10 lines of /etc/passwd
#bin/bash
tail -n 10 /etc/passwd

5. I'd prefer the first ones actually
Display the first 10 lines of /etc/passwd
#bin/bash
head -n 10 /etc/passwd

6. Line #2
Write a script that displays the third line of the file iacta.
#!/bin/bash
head -n 3 iacta | tail -n 1

7. It is a good file that cuts iron without making a noise
Write a shell script that creates a file named exactly \*\\'"Best School"\'\\*$\?\*\*\*\*\*:) containing the text Best School ending by a new line.
#bin/bash
echo -e Best School >> "\\*\\\\'\"Best School\"\\'\\\\*$\\?\\*\\*\\*\\*\\*:)"

8. Save current state of directory
Save current state of directory. Write a script that writes into the file ls_cwd_content the result of the command ls -la. If the file ls_cwd_content already exists, it should be overwritten. If the file ls_cwd_content does not exist, create it.
#bin/bash
ls -la >> ls_cwd_content

9. Duplicate last line
Write a script that duplicates the last line of the file iacta
The file iacta will be in the working directory
#bin/bash
tail -n 1 >> iacta
