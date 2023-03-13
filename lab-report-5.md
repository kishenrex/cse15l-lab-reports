# Find 

## Option 1: -name
[Source Link -name](https://www.tecmint.com/35-practical-examples-of-linux-find-command/)
This option finds all files which have the following filename.

### Example 1:
```
$ find -name "ch7.txt"
```

### Output 1:
```
./written_2/non-fiction/OUP/Abernathy/ch7.txt
./written_2/non-fiction/OUP/Berk/ch7.txt
./written_2/non-fiction/OUP/Kauffman/ch7.txt
```

In example 1, we search for all files called "ch7.txt". This results in the paths of 3 different files called "ch7.txt" being printed to the command line, which are in subdirectories of the current working directory. This command is useful to find files which have a certain name.


### Example 2:
```
$ find -name "Abernathy"
```

### Output 2:
```
./written_2/non-fiction/OUP/Abernathy
```

In example 2, we search for the directory named Abernathy, and the output of this is the path of the directory with the name "Abernathy". Hence, the `-name` command can also be used to find directories, as well as files.


## Option 2: -type
[Source Link -type](https://www.tecmint.com/35-practical-examples-of-linux-find-command/)
This option allows you to find files of a certain filetype. You can also do this without the `-type `option (with just `-name`, but this is another way to accomplish this goal

### Example 3:
```
$ find -type f -name "*.md"
```

### Output 3:
```
./README.md
```

In example 3, I searched for all files with a ".md" extension, which resulted in the README file being outputted as a path to the command line. Hence, the type option, used with the `-name` option can be used to find all files matching a specific filetype.

### Example 4:
```
$ find written_2/non-fiction/OUP/Berk/ -type f -name "*.txt"
```

### Output 4:
```
written_2/non-fiction/OUP/Berk/ch1.txt
written_2/non-fiction/OUP/Berk/ch2.txt
written_2/non-fiction/OUP/Berk/CH4.txt
written_2/non-fiction/OUP/Berk/ch7.txt
```

In example 4, I searched for all files with a "txt" extension, within the Berk subdirectory, which returned a list of all txt files in the Berk subdirectory. Hence this command can be used to find files of a specific type even within subdirectories.


## Option 3: -exec
[Source Link -exec](https://www.baeldung.com/linux/find-exec-command)
This command extends find's functionality, allowing it to execute commands and more.

### Example 5: 
```
find written_2/non-fiction/OUP/Berk/ -type f -name "*.txt" -exec file {} \;
```

### Output 5:
```
written_2/non-fiction/OUP/Berk/ch1.txt: Unicode text, UTF-8 text, with very long lines (1200), with CRLF line terminators
written_2/non-fiction/OUP/Berk/ch2.txt: Unicode text, UTF-8 text, with very long lines (1144), with CRLF line terminators
written_2/non-fiction/OUP/Berk/CH4.txt: Unicode text, UTF-8 text, with very long lines (1166), with CRLF line terminators
written_2/non-fiction/OUP/Berk/ch7.txt: Unicode text, UTF-8 text, with very long lines (1189), with CRLF line terminators
```

In example 5, I use the same command as example 4, but to extend it, I also get bash to determine the filetype (using the exec option) of each of the files returned by the find command. Hence, the exec option can be used to get important information about the files returned from a find command. 


### Example 6:
```
$ find written_2/non-fiction/OUP/Berk/ -name "*.txt" -exec echo file {} +;
```

### Output 6:
```
file written_2/non-fiction/OUP/Berk/ch1.txt written_2/non-fiction/OUP/Berk/ch2.txt written_2/non-fiction/OUP/Berk/CH4.txt written_2/non-fiction/OUP/Berk/ch7.txt
```

In example 6, I use the "+" delimiter instead of the "\" delimiter, which means only 1 echo is made, instead of a newline being made for each echo call. Overall, this command is similar to that seen in Example, but instead this one echoes (prints out) each file on one line, concatenated. Hence, this demonstrates how `-exec` can have multiple functionalities, through the use of delimiters.


## Option 4: -atime
[Source Link -atime](https://www.tecmint.com/35-practical-examples-of-linux-find-command/)
This option can be used to find files accessed a number of days prior.

### Example 7:
```
$ find / -atime 1
``` 

### Output 7:
```
/tmp/bng_ticket/20230311_211702_3009803400/active_packages.txt
/tmp/bng_ticket/20230311_211702_3009803400/activity_variable_info.txt
/tmp/bng_ticket/20230311_211702_3009803400/bug_screenshot.bmp
/tmp/bng_ticket/20230311_211702_3009803400/build_repro_info.txt
/tmp/bng_ticket/20230311_211702_3009803400/cvars.xml
/tmp/bng_ticket/20230311_211702_3009803400/global_status_info.txt
/tmp/bng_ticket/20230311_211702_3009803400/minidump.dmp
/tmp/bng_ticket/20230311_211702_3009803400/processes.csv
/tmp/bng_ticket/20230311_211702_3009803400/report_in_progress.txt
/tmp/mat-debug-19544.log
/tmp/mat-debug-20824.log
/tmp/mat-debug-25776.log
/tmp/mat-debug-35412.log
/tmp/mat-debug-46992.log
/tmp/mat-debug-8944.log
/tmp/wct4023.tmp
/tmp/wct5044.tmp
/tmp/wct6DA.tmp
/tmp/wct75CC.tmp
/tmp/wct7743.tmp
/tmp/wctD7C2.tmp
/tmp/{2193F421-808B-40F8-9C4C-DF0A201BB8AC} - OProcSessId.dat
/usr/share/vim/vim82/tools/vim_vs_net.cmd
```

In example 7, I searched for all files accessed 1 day prior, and the output was the paths of the files accessed 1 day prior. Hence, this option can be used to find files accessed a given number of days prior.


## Option 5: -size
[Source Link -size](https://www.tecmint.com/35-practical-examples-of-linux-find-command/)
This option can allow you to find files of a certain file size.

### Example 8:
```
$ find / -size 2M
```

### Output 8:
```
/bin/mintty.exe
/bin/msys-gettextlib-0-21.dll
/bin/msys-gnutls-30.dll
/bin/msys-iconv-2.dll
/bin/msys-sqlite3-0.dll
/bin/msys-unistring-5.dll
/mingw64/bin/libiconv-2.dll
/mingw64/bin/libp11-kit-0.dll
/mingw64/bin/libstdc++-6.dll
/mingw64/bin/libunistring-2.dll
/mingw64/bin/Microsoft.Identity.Client.dll
/mingw64/bin/pdftotext.exe
/mingw64/bin/tcl86.dll
/mingw64/bin/tk86.dll
/mingw64/libexec/git-core/libiconv-2.dll
/mingw64/libexec/git-core/libp11-kit-0.dll
/mingw64/libexec/git-core/libstdc++-6.dll
/mingw64/libexec/git-core/libunistring-2.dll
/mingw64/libexec/git-core/Microsoft.Identity.Client.dll
/mingw64/libexec/git-core/tcl86.dll
/mingw64/libexec/git-core/tk86.dll
/tmp/471d1f2d-72ed-40a7-b929-a3133595433f.tmp
/tmp/6bf63b6a-30c2-4a94-849f-0d46e5d4dfb9.tmp
/tmp/78e59604-bde9-42bc-b1dc-75d586528c6b.tmp
/tmp/890f2f4f-6754-4e7a-9788-5bdb763c9304.tmp
/tmp/ce3c48db-fcfb-44b1-bc44-138f74944657.tmp
/unins000.dat
/usr/bin/mintty.exe
/usr/bin/msys-gettextlib-0-21.dll
/usr/bin/msys-gnutls-30.dll
/usr/bin/msys-iconv-2.dll
/usr/bin/msys-sqlite3-0.dll
/usr/bin/msys-unistring-5.dll
/usr/lib/perl5/core_perl/auto/Encode/CN/CN.dll
/usr/lib/perl5/core_perl/auto/Encode/JP/JP.dll
/usr/lib/perl5/core_perl/auto/Encode/KR/KR.dll
/usr/lib/perl5/core_perl/auto/Encode/TW/TW.dll
/usr/lib/perl5/vendor_perl/auto/SVN/_Core/_Core.dll
/usr/share/perl5/core_perl/unicore/Name.pl
/usr/share/vim/vim82/doc/version8.txt
/usr/share/vim/vim82/doc/version9.txt
```

In this example, I search for all files which are 2MB, and all the files which mach this condition are printed to the command line as paths. Hence, this command can be used to find files of a given file size.
