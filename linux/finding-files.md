## Finding Files
Linux provides commands that can be used to search for files and directories. One of the main commands used for this is find.

## The find Command
The find command is used to search for files and directories based on different criteria, such as their name, type or size.

The basic syntax is:

find [location] [criteria]

For example:

find .

The . represents the current working directory, so this command searches from the current directory.

## Finding a File by Name
The -name option can be used to search for a file with a specific name.

For example:

find . -name "example.txt"

This searches the current directory and its subdirectories for a file called example.txt.

The find command can also be used to search for directories.

For example:

find . -type d -name "file-search"

The -type d option tells find to search specifically for directories.

Practical Example

<img width="389" height="193" alt="image" src="https://github.com/user-attachments/assets/53088738-31c7-46e2-8555-79bf2b3f3f3f" />


I first created a directory called file-search using the mkdir command.
I then navigated into the directory using the cd command.
I created three files called file1, file2, file3 using the touch command.
I used ls to confirm that the files had been created:
I then used find to search for the file called file2. This command returned ./file2 which shows that the file had been successfully located.
