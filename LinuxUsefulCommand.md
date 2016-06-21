
1. awk 'sub("$", "\r")' unixFile.txt > windowsFile.txt
2. awk '{ sub("\r$", ""); print }' windowsFile.txt > unixFile.txt
3. 
