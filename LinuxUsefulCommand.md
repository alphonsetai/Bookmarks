> **File Compatibility**

```awk 'sub("$", "\r")' unixFile.txt > windowsFile.txt```

```awk '{ sub("\r$", ""); print }' windowsFile.txt > unixFile.txt```

> **Process**

```ps -au | grep [USERNAME]```

> Create Soft & Hard Links

```ln -sf [target] [source]```

*Soft Links(-s Parameter)* : point to the file name

*Hard Links(By Default)*   : point to the file contents(share the same inode)

> Symbol Table Information

```nm -n [ELF_file]```
*Note:-n option sort symbols by address*

*Symbol Table Information*
<VirtualAddress>        <SymbolType>    <SymbolName>
0000000000601038        B                __bss_start

SymbolType : Lower case = local & Upper case = external

> List of Object include in static lib

```ar -t [libname.a]```

> List of shared Object used

```ldd [libname.so]  OR ldd [Executable]```

