# Learn command line

Please follow and complete the free online [Bash Scripting Tutorial](https://ryanstutorials.net/bash-scripting-tutorial/) or [Codecademy's Learn the Command Line](https://www.codecademy.com/learn/learn-the-command-line). These are helpful tutorials. You should be able to go through these in a couple of hours.

**Note:** Bash is not installed on a PC. Rather, PC users must install Cygwin. Once Cygwin has been installed, the command line interface witll _emulate_ bash. You can find all information regarding Cygwin [here](https://www.cygwin.com/).

---

### Q1.  Cheat Sheet of Commands  

Here's a list of items with which you should be familiar:  
* show current working directory path
* creating a directory
* deleting a directory
* creating a file using `touch` command
* deleting a file
* renaming a file
* listing hidden files
* copying a file from one directory to another

Make a cheat sheet for yourself: a list of at least **ten** commands and what they do.  (Use the 8 items above and add a couple of your own.)  

> > * `pwd`
> > * `mkdir my_directory`
> > * `rmdir my_directory # if my_directory is empty`
> > or `rm -R my_directory # if my_directory is not empty`
> > * `touch my_file.txt`
> > * `rm my_file.txt`
> > * `mv my_file.txt my_file2.txt`
> > * `ls .?*`
> > * `cp my_dir/my_file.txt another_dir`
> > * `chmod 755 my_script.sh # sets permissions to read/write/execute for owner, and read/execute for everyone else`
> > * `echo $PATH # print to screen the contents of $PATH variable` 

---

### Q2.  List Files in Unix   

What do the following commands do:  
`ls`  
`ls -a`  
`ls -l`  
`ls -lh`  
`ls -lah`  
`ls -t`  
`ls -Glp`  

> > `ls` lists the contents of current directory  
> > `ls -a` lists all contents of the current directory, including hidden files  
> > `ls -l` lists directory contents in long format, with file permissions  
> > `ls -lh` same as with -l flag, but with readable file size  
> > `ls -lah` lists all of the current directory's contents, in long format and with readable file size  
> > `ls -t` lists directory contents sorted by time  
> > `ls -Glp` lists directory contents in long format, without group names, and with a slash to indicate directories  

---

### Q3.  More List Files in Unix  

Explore these other [ls options](http://www.techonthenet.com/unix/basic/ls.php) and pick 5 of your favorites:

> > `ls -u`  
> > `ls -R`  
> > `ls -d`  
> > `ls -m`  
> > `ls -ru`  

---

### Q4.  Xargs   

What does `xargs` do? Give an example of how to use it.

> > `xargs` reads items from standard input, separated by blanks by default, and executes a command once for each item read.  
> > Example:  
> > `echo "new_file.txt another_file.txt" | xargs touch`

 

