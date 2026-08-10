## INSTRUCTIONS;

The password for the next level is stored in /etc/bandit_pass/bandit14 and can only be read by user bandit14. For this level, you don’t get the next password, but you get a private SSH key that can be used to log into the next level.

## SOLUTION;

firstly, transfer the sshkey.private using scp
this transfer will be made from your machine to the bandit server (machine>bandit)
you will need to use the passsword from the previous level to get the file transfered

    $ scp -P 2220 bandit13@bandit.labs.overthewire.org:/home/bandit13/sshkey.private .

* -P select the port 2220
* bandit13 is the username of the machine ???
* bandit.labs.overthewire.org is the address of the server communly used to access all the other levels
* /home/bandit13/sshkey.private is the full path of the file
* . is the destination file, according to the functionning of scp ($scp -[flag] src dest)

so the sshkey.private file will be copied in your machine, in the repo you are in currently
you cant use the key like that, you will get a warning because the perm of the file are too openned and the system consider that it is an issue for the security of the file
the perms arent good for ssh ? change it 

    $ sudo chmod 600 sshkey.private

* 600, which make it readable and writable for the owner ONLY

now it is good to use

    $ ssh bandit.labs.overthewire.org -p 2220 -l bandit14 -i sshkey.private

* -i identity file, ssh will use the private key as the password to log in

now that you are logged in, you can display the password of this level, using cat

    $ cat /etc/bandit_pass/bandit14

## VULNERABILITIES;

private ssh keys are a thing you wanna keep secret, it can be used against you in the worst way
