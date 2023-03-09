# Shell, I/O Redirections and filters
---------------------------------
## QUIZ

### Question #0  
Which symbol should I use to redirect the standard output to a file (overwrite the file)?
```
>
```
### Question #1  
Which symbol should I use to redirect the standard output to a file (appending to the file)?
```
>>
```
### Question #2  
Which symbol should I use to redirect the error output to the standard output?
```
2>&1
```
### Question #3  
Which symbol should I use to start a comment?
```
#
```
### Question #4  
Which command should I use to display the entire file content?
```
cat
```
### Question #5  
Which command should I use to display the last 11 lines of a file?
```
tail-n 11 my_file
```
### Question #6  
Which symbol should I use to escape a special character?
```
\
```
---------------------------------
## Tasks

### 0. Hello World  
Write a script that prints “Hello, World”, followed by a new line to the standard output.
```
#bin/bash
echo "Hello, World"
```
### 1. Confused smiley  
Write a script that displays a confused smiley "(Ôo)'.
```
#bin/bash
echo "\"(Ôo)'
```
### 2. Let's display a file  
Display the content of the /etc/passwd file.
```
#bin/bash
cat /etc/passwd
```
### 3. What about 2?  
Display the content of /etc/passwd and /etc/hosts
```
#bin/bash
echo /etc/passwd /etc/hosts
```
### 4. Last lines of a file  
Display the last 10 lines of /etc/passwd
```
#bin/bash
tail -n 10 /etc/passwd
```
### 5. I'd prefer the first ones actually  
Display the first 10 lines of /etc/passwd
```
#bin/bash
head -n 10 /etc/passwd
```
### 6. Line #2  
Write a script that displays the third line of the file iacta.
```
#!/bin/bash
head -n 3 iacta | tail -n 1
```
### 7. It is a good file that cuts iron without making a noise  
Write a shell script that creates a file named exactly \*\\'"Best School"\'\\*$\?\*\*\*\*\*:) containing the text Best School ending by a new line.
```
#bin/bash
echo -e Best School >> "\\*\\\\'\"Best School\"\\'\\\\*$\\?\\*\\*\\*\\*\\*:)"
```
### 8. Save current state of directory  
Save current state of directory. Write a script that writes into the file ls_cwd_content the result of the command ls -la. If the file ls_cwd_content already exists, it should be overwritten. If the file ls_cwd_content does not exist, create it.
```
#bin/bash
ls -la >> ls_cwd_content
```
### 9. Duplicate last line  
Write a script that duplicates the last line of the file iacta
The file iacta will be in the working directory
```
#bin/bash
tail -n 1 >> iacta
```
### 10. No more javascript  
Write a script that deletes all the regular files (not the directories) with a .js extension that are present in the current directory and all its subfolders.
```
#!/bin/bash
find . -type f -name "*.js" -delete
```
### 11. Don't just count your directories, make your directories count  
Write a script that counts the number of directories and sub-directories in the current directory.
```
#!/bin/bash
echo "\"(Ôo)'"
```
### 12. What’s new  
Create a script that displays the 10 newest files in the current directory.
```
#!/bin/bash
ls -t | head
```
### 13. Being unique is better than being perfect  
Create a script that takes a list of words as input and prints only words that appear exactly once.
```
#!/bin/bash
sort | uniq -u
```
### 14. It must be in that file  
Display lines containing the pattern “root” from the file /etc/passwd
```
#!/bin/bash
grep "root" /etc/passwd
```
### 15. Count that word  
Display the number of lines that contain the pattern “bin” in the file /etc/passwd
```
#!/bin/bash
grep -c "bin" /etc/passwd
```
### 16. What's next?  
Display lines containing the pattern “root” and 3 lines after them in the file /etc/passwd.
```
#!/bin/bash
grep -A3 "root" /etc/passwd
```
### 17. I hate bins  
Display all the lines in the file /etc/passwd that do not contain the pattern “bin”.
```
#!/bin/bash
grep -v "bin" /etc/passwd
```
### 18. Letters only please  
Display all lines of the file /etc/ssh/sshd_config starting with a letter.
```
#!/bin/bash
grep '^[[:alpha:]]' /etc/ssh/sshd_config
```
### 19. A to Z  
Replace all characters A and c from input to Z and e respectively.
```
#!/bin/bash
tr "A" "Z" | tr "c" "e"
```
### 20. Without C, you would live in hiago  
Create a script that removes all letters c and C from input.
```
#!/bin/bash
tr -d c | tr -d C
```
### 21. esreveR  
Write a script that reverse its input.
```
#!/bin/bash
rev
```
### 22. DJ Cut Killer  
Write a script that displays all users and their home directories, sorted by users.
```
#!/bin/bash
cut -d: -f1,6 /etc/passwd | sort
```
