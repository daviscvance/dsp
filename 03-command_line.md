# Learn command line

Please follow and complete the free online [Bash Scripting Tutorial](https://ryanstutorials.net/bash-scripting-tutorial/) or [Codecademy's Learn the Command Line](https://www.codecademy.com/learn/learn-the-command-line). These are helpful tutorials. You should be able to go through these in a couple of hours.

**Note:** Bash is not installed on a PC. Rather, PC users must install Cygwin. Once Cygwin has been installed, the command line interface will _emulate_ bash. You can find all information regarding Cygwin [here](https://www.cygwin.com/).

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

> > 1. `pwd` - prints working directory
> > 2. `mkdir <dir>` - makes a new directory
> > 3. `rmdir <dir>` - removes a directory
> > 4. `touch <file>` - creates blank file if file _DNE_
> > 5. `rm <file>` - removes a file
> > 6. `mv <source> <destination>` - renames or moves file
> > 7. `ls -a` - lists files in working dir., includes _.hidden_ files
> > 8. `cp <source> <destination>` - copies a source file/ dir. into the destination
> > 9. `chmod [permissions] [path]` - changes access permissions by specified user
> > 10. `man <command>` - opens the manual page for a command

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

> > 1. ls - lists files in working directory
> > 2. `ls -a` - lists files in working dir., includes _.hidden_ files (files that start with .)
> > 3. `ls -l` - lists files in working dir., in long format (provides additional file info)
> > 4. `ls -lh` - lists files in working dir., in long format with unit suffixes for file sizes
> > 5. `ls -lah` - lists files in working dir., in long format with unit suffixes for file sizes, includes _.hidden_ files
> > 6. `ls -t` - lists files in working dir., sorts by time modified (newest first), then sorts in lexicographical order
> > 7. `ls -Glp` - lists files in working dir., in long format, writes a slash (`/`) after each file if it is a dir., and has colorized output

---

### Q3.  More List Files in Unix  

Explore these other [ls options](http://www.techonthenet.com/unix/basic/ls.php) and pick 5 of your favorites:

> > 1. -p puts a helpful slash at the end of directories
> > 2. -R shows subdirectory contents
> > 3. -1 displays each file/dir. on its own line
> > 4. -m displays listings separated by commas
> > 5. -S sorts by file size

---

### Q4.  Xargs   

What does `xargs` do? Give an example of how to use it.

> > `xargs` allows user to run a command on all items in a list. For example, if we want to rename file extensions ending in a certain format we can pass a list into the `xarg` command and it will perform that command on the listings.
> > ```console
basename -s .JPG -a *.JPG | xargs -n1 -i mv {}.JPG {}.jpg
```
