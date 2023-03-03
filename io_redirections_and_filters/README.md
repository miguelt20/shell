# I/O Redirection
In this project, we will explore a powerful feature used by command line programs called input/output redirection. As we have seen, many commands such as ls print their output on the display. This does not have to be the case, however. By using some special notations we can redirect the output of many commands to files, devices, and even to the input of other commands.

By using some special notations we can redirect the output of many commands to files, devices, and even to the input of other commands.

### Standard Output
Most command line programs that display their results do so by sending their results to a facility called standard output. By default, standard output directs its contents to the display. To redirect standard output to a file, the ">" character is used like this:

```bash
user@bash$ ls > file_list.txt
```
In this example, the ls command is executed and the results are written in a file named file_list.txt. Since the output of ls was redirected to the file, no results appear on the display.

Each time the command above is repeated, file_list.txt is overwritten from the beginning with the output of the command ls. To have the new results appended to the file instead, we use ">>" like this:

```bash
user@bash$ ls >> file_list.txt
```
When the results are appended, the new results are added to the end of the file, thus making the file longer each time the command is repeated. If the file does not exist when we attempt to append the redirected output, the file will be created.

### Standard Input

Many commands can accept input from a facility called standard input. By default, standard input gets its contents from the keyboard, but like standard output, it can be redirected. To redirect standard input from a file instead of the keyboard, the "<" character is used like this:

```bash
user@bash$ sort < file_list.txt
```
In the example above, we used the sort command to process the contents of file_list.txt. The results are output on the display since the standard output was not redirected. We could redirect standard output to another file like this:
```bash
user@bash$ sort < file_list.txt > sorted_file_list.txt
```
As we can see, a command can have both its input and output redirected. Be aware that the order of the redirection does not matter. The only requirement is that the redirection operators (the "<" and ">") must appear after the other options and arguments in the command.

Here are some of the commands used in the scripts:

- `echo`: The echo command can be used for displaying a line of string/text that is passed as the arguments. 
- `cat`: One of its most common usages is to print the content of a file onto the standard output stream.
- `head`: It prints the first 10 lines of the specified files.
- `tail`: It prints the last few number of lines (10 lines by default) of a certain file, then terminates.
- `find`: It can be used to find files and directories and perform subsequent operations on them. It supports searching by file, folder, name, creation date, modification date, owner and permissions.
- `wc`: It calculates a file's word, line, character, or byte count.
- `sort`: It is a tool for sorting file contents and printing the result in standard output.
- `uniq`: The uniq command deletes repeated lines in a file.
- `grep`: It is one of the most versatile and useful Linux commands available. It works by searching for text and strings that users define in a given file.
- `tr`: It is a Linux command-line utility that translates or deletes characters from standard input ( stdin ) and writes the result to standard output ( stdout ).
- `rev`: It copies the named files to standard output, reversing the order of characters in every line.
- `cut`: It is a command-line utility that allows you to cut out sections of a specified file or piped data and print the result to standard output.
