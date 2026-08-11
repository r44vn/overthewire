## INSTRUCTIONS;

To gain access to the next level, you should use the setuid binary in the homedirectory. Execute it without arguments to find out how to use it. The password for this level can be found in the usual place (/etc/bandit_pass), after you have used the setuid binary.

## SOLUTION;

"It allows a program to run with the effective user ID of the file's owner rather than the user who executes the program. "
lets execute the command we need to get the password

    $ ./setuidfile cat /etc/bandit_pass/bandit20

* ./ is used to execute an executable file

## VULNERABILITIES;

setuid files can be a real issue for your infos if somebody with bad intentions takes it
