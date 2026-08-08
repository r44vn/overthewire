## INSTRUCTIONS;

The password for the next level is stored somewhere on the server and has all of the following properties:

* owned by user bandit7
* owned by group bandit6
* 33 bytes in size


## SOLUTION;

    $ find / -size 33c -user bandit7 -group bandit6 2>/dev/null

we are searching on root (/) size 33byte (-size) with the good user and the good group flag, and then every error messages are sended directly to trash with 
    
    2>/dev/null

2> is every error messages and /dev/null is the trash in the filesystem

## VULNERABILITIES;

dont hide your sensible data in a randole folder of your filesystem. it wont hide you
