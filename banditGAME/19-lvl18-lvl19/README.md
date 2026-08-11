## INSTRUCTIONS;

The password for the next level is stored in a file readme in the homedirectory. Unfortunately, someone has modified .bashrc to log you out when you log in with SSH.

## SOLUTION;

there is a bash scipt who is autoomatically disconnect us while the password is true
we can still execute some commands while we are trying to connect to the ser

    $ ssh bandit.labs.overthewire.org -p 2220 -l banditX ls
    $ ssh bandit.labs.overthewire.org -p 2220 -l banditX cat xx

since the password .txt file is in the home dir, we can just cat it and get it


## VULNERABILITIES;

an auto disconnect bashscript isnt the right way of protecting your data
