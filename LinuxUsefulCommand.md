> **File Compatibility**

```awk 'sub("$", "\r")' unixFile.txt > windowsFile.txt```

```awk '{ sub("\r$", ""); print }' windowsFile.txt > unixFile.txt```


