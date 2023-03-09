#Shell, permissions#

##Quiz##

Question #0  
Which command should I use for changing a file permission?  
```
chmod  
```
Question #1  
Which command should I use for changing a file owner?
```
chown  
```
Question #2
What is the permission value for a file without any restriction?
```
777
```
Question #3  
What is the permission value for a file read only for the group owner?
```
040
```
Question #4
What is the numerical value for the rwx------ permission?
```
700
```
Question #5
What is the numerical value for the r-xr--r-- permission?
```
544
```
Question #6
What is the numerical value for the ----w---x permission?
```
021
```
##Task##  

0. My name is Betty  
Create a script that switches the current user to the user betty.
```
#!/bin/bash
su betty
```
  
1. Who am I  
Write a script that prints the effective username of the current user.
```
#!/bin/bash
whoami
```

2. Groups  
Write a script that prints all the groups the current user is part of.
```
#!/bin/bash
groups
```

3. New owner  
Write a script that changes the owner of the file hello to the user betty.
```
#!/bin/bash
chown betty: hello
```

4. Empty!  
Write a script that creates an empty file called hello.
```
#!/bin/bash
touch hello
```

5. Execute  
Write a script that adds execute permission to the owner of the file hello.
```
#!/bin/bash
chmod +100 hello
```

6. Multiple permissions  
Write a script that adds execute permission to the owner and the group owner, and read permission to other users, to the file hello.
```
#!/bin/bash
chmod +114 hello
```

7. Everybody!  
Write a script that adds execution permission to the owner, the group owner and the other users, to the file hello
```
#!/bin/bash
chmod a+x hello
```

8. James Bond  
Write a script that sets the permission to the file hello as follows:
```
#!/bin/bash
chmod 007 hello
```

9. John Doe  
Write a script that sets the mode of the file hello to this:
```
#!/bin/bash
chmod 753 hello
```

10. Look in the mirror  
Write a script that sets the mode of the file hello the same as olleh’s mode.
```
#!/bin/bash
chmod 354 olleh hello
```

11. Directories  
Create a script that adds execute permission to all subdirectories of the current directory for the owner, the group owner and all other users. Regular files should not be changed.
```
#!/bin/bash
chmod -R a+x */
```

12. More directories  
Create a script that creates a directory called my_dir with permissions 751 in the working directory.
```
#!/bin/bash
mkdir -m 751 my_dir
```

13. Change group  
Write a script that changes the group owner to school for the file hello
```
#!/bin/bash
chgrp school hello
```

14. Owner and group  
Write a script that changes the owner to vincent and the group owner to staff for all the files and directories in the working directory.
```
#!/bin/bash
chown -R vincent:staff *
```

15. Symbolic links  
Write a script that changes the owner and the group owner of _hello to vincent and staff respectively.
```
#!/bin/bash
chown -h vincent:staff _hello
```

16. If only  
Write a script that changes the owner of the file hello to vincent only if it is owned by the user guillaume.
```
#!/bin/bash
chown --from=guillaume vincent hello
```
