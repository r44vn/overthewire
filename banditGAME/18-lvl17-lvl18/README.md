## INSTRUCTIONS;

There are 2 files in the homedirectory: passwords.old and passwords.new. The password for the next level is in passwords.new and is the only line that has been changed between passwords.old and passwords.new

## SOLUTION;

to compare two ascii files, we use diff

    $ diff -a password.old password.new

* -a for text files

## VULNERABILITIES;

dont store your password that way i guess ?

