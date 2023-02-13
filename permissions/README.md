Shell, permissions

0. My name is Betty
#!/bin/bash
su betty

1. Who am I
#!/bin/bash
whoami

2. Groups
#!/bin/bash
groups

3. New owner
#!/bin/bash
chown betty: hello

4. Empty!
#!/bin/bash
touch hello

5. Execute
#!/bin/bash
chmod +100 hello

6.Multiple permissions
#!/bin/bash
chmod +114 hello

7. Everybody!
#!/bin/bash
chmod a+x hello

8. James Bond
#!/bin/bash
chmod 007 hello

9. John Doe
#!/bin/bash
chmod 753 hello

10.Look in the mirror
#!/bin/bash
chmod 354 olleh hello

11.Directories
#!/bin/bash
chmod -R a+x */

12. More directories
#!/bin/bash
mkdir -m 751 my_dir

13. Change group
chgrp school hello



