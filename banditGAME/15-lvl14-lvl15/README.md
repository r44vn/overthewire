## INSTRUCTIONS;

The password for the next level can be retrieved by submitting the password of the current level to port 30000 on localhost.

## SOLUTION;

the goal of this exercise is to communicate with the port 30000.
we need to open a tcp connection with nc (netcat) to do it.

    $ nc localhost 30000

submit the right password and you are done

## VULNERABILITIES;

do not store your password on a random port of your ssh server
