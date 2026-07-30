INSTRUCTIONS;

The goal of this level is for you to log into the game using SSH. The host to which you need to connect is bandit.labs.overthewire.org, on port 2220. The username is bandit0 and the password is bandit0. Once logged in, go to the Level 1 page to find out how to beat Level 1.

SOLUTION;

ok, lets connect to the game using ssh;

#ssh bandit.labs.overthewire.org -p 2220 -l bandit0

-p is to be able to select the port
-l is used to put the username

everything was found on 'man ssh'
