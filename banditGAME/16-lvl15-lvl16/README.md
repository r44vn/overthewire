## INSTRUCTIONS;

The password for the next level can be retrieved by submitting the password of the current level to port 30001 on localhost using SSL/TLS encryption.

## SOLUTION;

a service is listening on port 30001 and we need to connect to it using ssl/tls protocol
here is what i used

    $ openssl s_client -connect localhost:30001

and then, type the password of bandit15 to get the one of bandit16

## VULNERABILITIES;

with the good password, you dont become invulnerable with an ssl/tls protocol
actually, nothing is invulnerable over the internet
