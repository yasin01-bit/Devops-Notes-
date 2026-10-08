## Linux Pipes
A pipe | is used to take the output from one command and pass it as the input to another command.

This allows multiple commands to be combined together to perform a task.

## Using Pipes
The basic syntax is:

command1 | command2

The output from command1 is passed to command2.

For example:

ls | grep ".txt"

In this example:

ls lists the files and directories. | passes the output from ls to the next command. grep ".txt" searches the output for files containing .txt.


Practical Example


<img width="323" height="236" alt="image" src="https://github.com/user-attachments/assets/7fb7c67f-e68c-4987-8d85-55571ced8238" />



* I first created several files: `file1`, `file2`, `file3` and `file4`.
* I then used `ls` to list the files.
* I used a pipe to pass the output of `ls` to `grep` and search for files containing "file":

```bash
  ls | grep file
```

* The output showed:

```text
  file1 file2 file3 file4
```

* This demonstrated how the pipe passed the output from `ls` into `grep`, allowing me to filter the results.
