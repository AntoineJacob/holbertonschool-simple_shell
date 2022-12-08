## HSH: The Holberton School Shell
The  shell is a Holberton School project in the first trimester, helps student to understand the advanced
concepts behind the shell program include process, system call, bit manipulation, file managment, error handling ...

### General
* Who designed and implemented the original Unix operating system
* Who wrote the first version of the UNIX shell
* Who invented the B programming language (the direct predecessor to the C programming language)
* Who is Ken Thompson
* How does a shell work
* What is a pid and a ppid
* How to manipulate the environment of the current process
* What is the difference between a function and a system call
* How to create processes
* What are the three prototypes of `main`
* How does the shell use the `PATH` to find the programs
* How to execute another program with the `execve` system call
* How to suspend the execution of a process until one of its children terminates
* What is `EOF` / “end-of-file”?

### Requirements
* General
* Allowed editors: vi, vim, emacs
* All your files will be compiled on Ubuntu 20.04 LTS using gcc, using the options -Wall -Werror -Wextra -pedantic -std=gnu89
* All your files should end with a new line
* A README.md file, at the root of the folder of the project is mandatory
* Your code should use the Betty style. It will be checked using betty-style.pl and betty-doc.pl
* Your shell should not have any memory leaks
* No more than 5 functions per file
* All your header files should be include guarded
* Use system calls only when you need to `(why?)`

## List of allowed functions and system calls
* access (man 2 access)
* chdir (man 2 chdir)
* close (man 2 close)
* closedir (man 3 closedir)
* execve (man 2 execve)
* exit (man 3 exit)
* _exit (man 2 _exit)
* fflush (man 3 fflush)
* fork (man 2 fork)
* free (man 3 free)
* getcwd (man 3 getcwd)
* getline (man 3 getline)
* getpid (man 2 getpid)
* isatty (man 3 isatty)
* kill (man 2 kill)
* malloc (man 3 malloc)
* open (man 2 open)
* opendir (man 3 opendir)
* perror (man 3 perror)
* printf (man 3 printf)
* fprintf (man 3 fprintf)
* vfprintf (man 3 vfprintf)
* sprintf (man 3 sprintf)
* putchar (man 3 putchar)
* read (man 2 read)
* readdir (man 3 readdir)
*signal (man 2 signal)
* stat (__xstat) (man 2 stat)
* lstat (__lxstat) (man 2 lstat)
* fstat (__fxstat) (man 2 fstat)
* strtok (man 3 strtok)
* wait (man 2 wait)
* waitpid (man 2 waitpid)
* wait3 (man 2 wait3)
* wait4 (man 2 wait4)
* write (man 2 write)

### Compilation
All files will be compiled with the following: `$ gcc -Wall -Werror -Wextra -pedantic *.c`

### How to use our shell
First, you have to clone our projet by copy `https://github.com/AntoineJacob/holbertonschool-simple_shell.git`

Then, you have to complil it `gcc 4.8.4 -Wall -Werror -Wextra -pedantic *.c -o hsh`

You can now run our shell by typing `./hsh`

### Memory leaks
If you want to check memory leaks, you can use `valgrind --leak-check=full ./hsh`

### Manual
You can have more informations about how to use our shell by typing `man ./man_1_simple_shell`

### What the function return ?
 A return command is used to exit from a shell function. It takes a parameter [N], if N is mentioned then it returns [N] and if N is not mentioned then it returns the status of the last command executed within the function or script. N can only be a numeric value. Note that echo $? can be used to display the last return status.

### Exemples of outputs:
### In interactive mode
- with ls
```
username@your-regular-prompt:/holbertonschool-simple_shell# ./hsh
$ ls
AUTHORS  EOF.c  README.md  environ.c  errors.c  execute.c  exit.c  fork.c  frees.c  gen-authors  hsh  main.c  path.c  prompt.c  shell.h  strfunct.c  tokenize.c
$
```
### In non-interactive mode
- with echo "/bin/ls" | ./hsh
```
username@your-regular-prompt:/holbertonschool-simple_shell# echo "/bin/ls" | ./hsh
AUTHORS  environ.c  EOF.c  errors.c  execute.c  exit.c  fork.c  frees.c  gen-authors  hsh  main.c  path.c  prompt.c  README.md  shell.h  strfunct.c  tokenize.c
$
```
## To compare with the basic Unix Shell :
### In interactive mode

- with ls
```
username@your-regular-prompt:/holbertonschool-simple_shell# ls
AUTHORS  EOF.c  README.md  environ.c  errors.c  execute.c  exit.c  fork.c  frees.c  gen-authors  hsh  main.c  path.c  prompt.c  shell.h  strfunct.c  tokenize.c
username@your-regular-prompt:/holbertonschool-simple_shell#
```
### In non-interactive mode
- with echo "/bin/ls" | /bin/sh
```
username@your-regular-prompt:/holbertonschool-simple_shell# echo "/bin/ls" | /bin/sh
AUTHORS  environ.c  EOF.c  errors.c  execute.c  exit.c  fork.c  frees.c  gen-authors  hsh  main.c  path.c  prompt.c  README.md  shell.h  strfunct.c  tokenize.c
username@your-regular-prompt:/holbertonschool-simple_shell#
```
### Comments
 No memory leaks, but we need to debug some parts of the code to get the 100%.

### Authors
* Antoine jacob - https://github.com/AntoineJacob
* Kylian Vallier - https://github.com/https://github.com/instagram-aesgod