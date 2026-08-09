## INSTRUCTIONS;

The password for the next level is stored in the file data.txt, which contains base64 encoded data

## SOLUTION;

to decode a base64 encoded file, use

    $ base64 -d data.txt

* -d = flag decode

## VULNERABILITIES;

    "Base64 is a binary-to-text encoding that uses 64 printable characters to represent each 6-bit segment of a sequence of byte values"

not a reliable encryption tool for your passwords
