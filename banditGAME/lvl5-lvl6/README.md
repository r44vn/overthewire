INSTRUSTIONS;

The password for the next level is stored in a file somewhere under the inhere directory and has all of the following properties:


    human-readable
    1033 bytes in size
    not executable

SOLUTION;

lets not focus on the "human-readable", with find, you can get the cmd who filter everyother files which is not 1033 byte and executable

$find . \! -executable -size 1033c

VULNERABILITIES;

a lot of differents files is not the thing who is going to protect your sensible files
