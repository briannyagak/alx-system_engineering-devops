#!/bin/bash
su betty > switches the current user to the user betty.
id -un > prints the effective username of the current user.
groups > prints all the groups the current user is part of.
chown betty hello > changes the owner of the file hello to the user betty.
touch hello > creates an empty file called hello. 
chmod u+x hello > adds execute permission to the owner of the file hello.
chmod u+x,g+x,o+r hello > adds execute permission to the owner and the group owner, and read permission to other users, to the file hello.
chmod ugo+x hello > adds execution permission to the owner, the group owner and the other users, to the file hello
chmod 007 hello > script that sets the permission to the file hello as follows:
Owner: no permission at all
Group: no permission at all
Other users: all the permissions

chmod 753 hello > script that sets the mode of the file hello to this:
-rwxr-x-wx 1 julien julien 23 Sep 20 14:25 hello

chmod --reference=olleh hello > script that sets the mode of the file hello the same as olleh’s mode.
chmod -R ugo+X . > script that adds execute permission to all subdirectories of the current directory for the owner, the group owner and all other users.
Regular files should not be changed.
mkdir -m 751 my_dir > script that creates a directory called my_dir with permissions 751 in the working directory.
chgrp school hello > script that changes the group owner to school for the file hello.
