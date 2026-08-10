## INTSTRUCTIONS;

The password for the next level is stored in a file called - located in the home directory

## SOLUTION;

i know there is other ways of doin it, but i did it that way;

the file was mod blocked, didnt had the right to modify it, so i created my own version


created a temp file in a temp env, in which you will be able to rename the dashed file

    $ mktemp -d
    $ cp '-' [temp repo created by mktemp]
    $ cd [temp repo]

rename the file named '-'
    
    $mv '-' aaa

display it

    $cat aaa

## VULNERABILITIES;

a dashed file can maybe obstruct our abilities to read it but it is not a good way of protecting your passw
