## INSTRUCTIONS;

The password for the next level is stored in the file data.txt in one of the few human-readable strings, preceded by several ‘=’ characters.

## SOLUTION;

when you concatenate data.txt with

    $ cat data.txt

you got some gibberish bcs the file is non-human readable, but when you sort it, it concatenate the file to the standard output.

it is described on the man page of sort;
    
    "Write sorted concatenation of all FILE(s) to standard output."

so you get the password straight up!

## VULNERABILITIES;

when a file is not human-readable, it is not protected and there is always some ways of reversing the process
