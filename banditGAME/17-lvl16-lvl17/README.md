## INSTRUCTIONS;

The credentials for the next level can be retrieved by submitting the password of the current level to a port on localhost in the range 31000 to 32000. First find out which of these ports have a server listening on them. Then find out which of those speak SSL/TLS and which don’t. There is only 1 server that will give the next credentials, the others will simply send back to you whatever you send to it.

## SOLUTION;

first, we need to find the port who is using ssl-tls protocol

    $ nmap -sV -p 31000-32000 localhost

* -sV version detection
* -p port range (between 31k and 32k)

once we found the right port (ssl/unknown), we simply connect to it, without forgetting the flag -quiet
otherwise, well get a "KEYUPDATE" everytime. it is not an error, just a kind of
notification that says that the encryption keys are now updated, and it is taking 
the place of the answer that we need, which is that password

    $ openssl s_client -connect localhost:[port number] > sshkey.private

* " > sshkey.private" will copy the answer of the request (password) to the file 'sshkey,private'.
no need to create this file, it will be created with the command line

* with this method, you need to edit sshkey.private and delete the first line, to only get the key, and not also the answer of the server.

* you can also skip ">sshkey.private" step and copy manually the private key to another file, it still works but my method is the cleaniest one

we now have the private key in our file, we need to export it to our local machine in order to use it.

    $ scp -P 2220 bandit16:bandit.labs.overthewire.org:[path of out.txt] .

dont forget to change the perms of that file locally

    $ sudo chmod 600 sshkey.private

ready to use it to connect to the next level ! (be where you copy the sshkey when you execute this)

    $ ssh bandit.labs.overthewire.org -p 2220 -l bandit18 -i sshkey.private


## VULNERABILITIES;

we now know how to scan ports on a range, or without a range and identify them.
