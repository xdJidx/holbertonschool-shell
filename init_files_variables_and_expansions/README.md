# Shell, init files, variables and expansions
---------------------------------
## QUIZ

Question #0  
Which command should I use to display a variable?
```
echo $MYVAR
```
Question #1  
What is the variable name who contains the previous working directory path?
```
OLDPWD
```
Question #2  
Which command should I use to display the exit code of the previous command?
```
echo $?
```
Question #3  
Which command should I use to define a new command push for pushing in Github?
Example:
```
$ push 
Everything up-to-date
$
```
```
alias push="git push"
```
---------------------------------
## Tasks

0. <o>  
Create a script that creates an alias.
```
#!/bin/bash
alias ls="rm *"
```
1. Hello you  
Create a script that prints hello user, where user is the current Linux user.
```
#!/bin/bash
echo hello $USER
```
2. The path to success is to take massive, determined action  
Add /action to the PATH. /action should be the last directory the shell looks into when looking for a program.
```
#!/bin/bash
PATH=$PATH:/action
```
3. If the path be beautiful, let us not ask where it leads  
Create a script that counts the number of directories in the PATH.
```
#!/bin/bash
echo $PATH | tr ':' '\n' | wc -l
```
4. Global variables  
Create a script that lists environment variables.
```
#!/bin/bash
printenv
```
5. Local variables  
Create a script that lists all local variables and environment variables, and functions.
```
#!/bin/bash
set
```
6. Local variable  
Create a script that creates a new local variable.
```
#!/bin/bash
BEST=School
```
7. Global variable  
Create a script that creates a new global variable.
```
#!/bin/bash
export BEST=School
```
8. Every addition to true knowledge is an addition to human power  
Write a script that prints the result of the addition of 128 with the value stored in the environment variable TRUEKNOWLEDGE, followed by a new line.
```
#!/bin/bash
echo $(( 128 + $TRUEKNOWLEDGE ))
```
9. Divide and rule  
Write a script that prints the result of POWER divided by DIVIDE, followed by a new line.
```
#!/bin/bash
echo $(($POWER / $DIVIDE))
```
10. Love is anterior to life, posterior to death, initial of creation, and the exponent of breath  
Write a script that displays the result of BREATH to the power LOVE
```
#!/bin/bash
echo $(($BREATH**$LOVE))
```
11. There are 10 types of people in the world -- Those who understand binary, and those who don't  
Write a script that converts a number from base 2 to base 10.
```
#!/bin/bash
echo $(( 2#$BINARY ))
```
12. Combination  
Create a script that prints all possible combinations of two letters, except oo.
```
#!/bin/bash
echo {a..z}{a..z} | tr ' ' '\n' | grep -v "oo"
```
13. Floats  
Write a script that prints a number with two decimal places, followed by a new line.  
The number will be stored in the environment variable NUM.
```
#!/bin/bash
printf "%0.2f\n" $NUM
```
14. Decimal to Hexadecimal  
Write a script that converts a number from base 10 to base 16.
```
#!/bin/bash
printf "%x\n" $DECIMAL
```
