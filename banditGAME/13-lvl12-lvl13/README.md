## INSTRUCTIONS;

The password for the next level is stored in the file data.txt, which is a hexdump of a file that has been repeatedly compressed.

## SOLUTION;

firstly, copy the data.txt file in "/tmp" in order to modify it

    $ mktemp -d
    $ cp data.txt [temp file]
    $cd [temp file]

so for this level, we got an hex dump file, in a .txt file.
we firstly need to reverse the "hexdump" that has been applied to the file with

    $ xxd -r data.txt [file name, well use "out"]

* -r stand for reverse

and then, analyse the result of the cmd

    $ file out

we then get how did the original file was compressed
decompress it with the good cmd, repeat the process until you got the original ascii file, the password will be inside it

## VULNERABILITIES;

if you compress a file over and over, or convert it into a hexdump, it is still not protected
