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

> >
> > pwd * show current working directory path  
> > mkdir directory * creating a directory   
> > rm -R directory * deleting a directory  
> > touch file.txt * creating a file using `touch` command  
> > rm file.txt * deleting a file  
> > mv file.txt file2.txt * renaming a file  
> > ls -a * listing hidden files  
> > cp directorya/txt.file directoryb/ * copying a file from one directory to another  
> > ls -t * sorts by modify date  
> > ls -l * displays contents in long format  

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
  
> > ls * list contents  
> > ls -a * list contents including hidden files and folders  
> > ls -l * list contents in long format  
> > ls -lh * list conents in long format and in human readable sizes  
> > ls -lah * list contents in long format, human readable size, and includes hidden files and folders  
> > ls -t * sorts files by time and date  
> > ls -Glp * list contents in long format, exclude owner column, and add a / at the end of the directories  


---

### Q3.  More List Files in Unix  

Explore these other [ls options](http://www.techonthenet.com/unix/basic/ls.php) and pick 5 of your favorites:

> > ls -d * list only directories  
> > ls -u * list files by access time  
> > ls -m * displays names as comma seperated list  
> > ls -r * displays files in reverse order  
> > ls -x * displays files as rows across screen  


---

### Q4.  Xargs   

What does `xargs` do? Give an example of how to use it.

> > xargs typically passes an output of one command as an argument for another command. An example of this would be  
> > find ./work -print | xargs grep "class"  
> > This finds files in the folder work and passes each one to grep to search for the word "class".  
 

