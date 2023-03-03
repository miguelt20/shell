# The Shell
The shell is a program that takes commands from the keyboard and gives them to the operating system to perform. In the old days, it was the only user interface available on a Unix-like system such as Linux. Nowadays, we have graphical user interfaces (GUIs) in addition to command line interfaces (CLIs) such as the shell.

This repository contains the basic steps to learn how to use a shell properly and take advantage of it.

## Basic commands

Here are some of the basic commands to navigate, manipulate files or to look for help in the Man pages.
- `pwd`
- `cd`
- `ls` 
- `cp`
- `mv`
- `rm`
- `touch`
- `mkdir`
- `help`
- `man`
- `less`
- `file`
- `ln`
- `type`
- `which`

## Permissions
Every file and directory in your UNIX/Linux system has following 3 permissions and here are some of the commands to change or give permissions to a file.
- `chmod`
- `sudo`
- `su`
- `chown`
- `chgrp`
- `id`
- `groups`
- `whoami`
- `adduser`
- `useradd`
- `addgroup`

## Loops, conditions and parsing
### Loops
Loops allow us to take a series of commands and keep re-running them until a particular situation is reached. They are useful for automating repetitive tasks.

```bash
#!/bin/bash
# Basic while loop

counter=1
while [ $counter -le 10 ]
do
    echo $counter
    ((counter++))
done

echo All done
```
#### Result of the script

```bash
user@bash$ ./while_loop.sh
1
2
3
4
5
6
7
8
9
10
All done

user@bash:
```