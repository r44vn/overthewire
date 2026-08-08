INSTRUCTIONS;

The password for the next level is stored in the file data.txt and is the only line of text that occurs only once

SOLLUTION;
    
    $sort data.txt | uniq -u
sort every line with sort and print the unic one with uniq -u

VULNERABILITIES;

the fact that your password is in a giant .txt file doesnt protect you at all
