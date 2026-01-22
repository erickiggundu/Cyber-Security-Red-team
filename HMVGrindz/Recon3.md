#Url/link
https://hackmyvm.eu/hmvgrind/srv-01.php
#Challenge Description
Before leaving, Tron told me that he left some secret into a file called .dontdeleteme, what is the content of the file?
Nice.
#Concept
file Reconnaisance
#Method of Solving

What I Did

    Searched for a hidden file using find
    Found /etc/.dontdeleteme
    Read it with cat
    Extracted a hash: f25a2fc72690b780b2a14e140ef6a9e0

The Technique

File Enumeration Attack

    Search system for hidden files (files starting with .)
    Extract sensitive data (passwords, flags, credentials)

Commands Used
bash

find / -name ".dontdeleteme" 2>/dev/null  # Search
cat /etc/.dontdeleteme                     # Read

Result

Found a 32-character MD5 hash - likely a password or CTF flag
