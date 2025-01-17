I choose the commands find.

command-line option 1: -type

command-line option 1.1
Command: find /tmp -name chapter-1.txt -type f -print | xargs /bin/rm -f
![Image](https://github.com/wahanucsd/docsearch/blob/main/Screen%20Shot%202022-10-31%20at%202.08.23%20AM.png)
Explanation: This command will find the file named "chapter-1.txt" 
in the directory and delete the file.
This command is useful because when there are too many files, 
it is very hard to find the file we want in the directory and
delete this file.



command-line option 1.2
Command: find . -type f -exec file '{}' \;
![Image](https://github.com/wahanucsd/docsearch/blob/main/Screen%20Shot%202022-10-31%20at%202.12.41%20AM.png)
Explanation: This command will run file on every file in the directory.
This command is useful because we could easily see every file with their name and directory.


command-line option 1.3
Command: find /tmp \( -type f -o -type d -o -type l \)
![Image](https://github.com/wahanucsd/docsearch/blob/main/Screen%20Shot%202022-10-31%20at%202.20.27%20AM.png)
Explanation: This command could pass the three types- files, 
directories, and symbolic links- as a comman-separated list.
This command is useful because it could deal with many diffrent types of files at the same time.



command-line option 2: -name

command-line option 2.1
Command: find /tmp -name chapter-1.txt -type f -print | xargs /bin/rm -f
![Image](https://github.com/wahanucsd/docsearch/blob/main/Screen%20Shot%202022-10-31%20at%202.08.23%20AM.png)
Explanation: This command will find the file named "chapter-1.txt" 
in the directory and delete the file.
This command is useful. Because if there are too many files in the directory,
it is hard to find the file we want to delete.

command-line option 2.2
Command: find / -name needle -print -quit
![Image](https://github.com/wahanucsd/docsearch/blob/main/Screen%20Shot%202022-10-31%20at%202.33.01%20AM.png)
Explanation: This command could search the file called needle 
and stop if the first one has been found.
This command is useful. Because if there are too many files in the directory,
it is hard to find the first file that has the same name with the command.

command-line option 2.3
Command: find /tmp -name core -type f -print0 | xargs -0 /bin/rm -f
![Image](https://github.com/wahanucsd/docsearch/blob/main/Screen%20Shot%202022-10-31%20at%202.40.29%20AM.png)
Explanation: This command will find the file named "core" 
in the directory and delete the file.
This command is useful because when there are too many files, 
it is very hard to find the file we want in the directory and
delete this file.




command-line option 3: -perm

command-line option 3.1
Command: find . -perm 664
![Image](https://github.com/wahanucsd/docsearch/blob/main/Screen%20Shot%202022-10-31%20at%202.44.54%20AM.png)
Explanation: This command could search the file which owner could read
and write but others only can read. This command is useful if we want to find different types of file when there
are many files in the directory.


command-line options1 3.2
Command: find . -perm -664
![Image](https://github.com/wahanucsd/docsearch/blob/main/Screen%20Shot%202022-10-31%20at%202.47.35%20AM.png)
Explanation: This command could search the file which owner could read 
and write but others can read without other permission bits. This command is useful if we want to find different types of file when there
are many files in the directory.


command-line options1 3.2
Command: find . -perm -g+w,u+w
![Image](https://github.com/wahanucsd/docsearch/blob/main/Screen%20Shot%202022-10-31%20at%203.00.13%20AM.png)
Explanation: This command could search the file which could be written 
by their owner and their group. This command is useful if we want to find different types of file when there
are many files in the directory.
