# Intro to Bash Scripting

## The Shebang Line

A **shebang line** tells the operating system which interpreter should be used to run a script.

For example:

```bash
#!/bin/bash
```

- `#!` identifies the line as a shebang.
- `/bin/bash` tells the system to use Bash to interpret the script.

### Practical Example

1. I used the `touch` command to create a file called `example.sh`.
2. I used `vim` to open a text editor in my terminal and write a Bash script (see the second screenshot).
3. I used `chmod +x` to give the file executable permissions.

<img width="1630" height="528" alt="image" src="https://github.com/user-attachments/assets/3cabc160-1adb-484e-bad2-ef757781b863" />


I executed the script in three ways:

<img width="1630" height="528" alt="image" src="https://github.com/user-attachments/assets/0c751edf-ad4a-4190-b9fa-02b2e976284d" />


| Command | What it does |
|---|---|
| `./example.sh` | Tells the shell to run the script from the current directory |
| `sh example.sh` | Runs the script using the `sh` interpreter |
| `bash example.sh` | Runs the script using the `bash` interpreter |

Below is the Bash script I wrote, which can be executed using `./`, `sh` and `bash`.

<img width="1994" height="528" alt="image" src="https://github.com/user-attachments/assets/ef3b5d5a-802e-4f9a-a8a5-43794568c9fb" />



---

## Comments

Comments are lines in a script that are **not executed** as part of the code. They serve as informative text for the reader.

There are two types of comments:

- **Single line comments:** start the line with `#`
- **Multiline comments:** use `:` followed by text inside single quotation marks `' '`

<img width="1488" height="564" alt="image" src="https://github.com/user-attachments/assets/f9e44188-a0ff-4d0c-aaf6-5261bc2126ab" />


If you run `example.sh` using `./`, the comments will not be shown in the output.

To read the comments in the terminal, use the `cat` command followed by the filename:

```bash
cat example.sh
```

<!-- Add screenshot here -->

---

## Running Scripts From Anywhere

In my previous notes I showed how `./` can be used to run a script in its current directory.

**What if we want to run the script from anywhere without specifying its path?**

To do this, the script needs to be placed in a directory that is listed in the `PATH` environment variable.

> `PATH` is an environment variable that tells the shell which directories to search for executable files in response to commands.

In the example below, I moved the file to `/usr/local/bin` (a directory in `PATH`) and made it executable:

<img width="1756" height="216" alt="image" src="https://github.com/user-attachments/assets/acb5f07b-1a3b-413d-88c6-fd9ffb415e50" />


Now when I run the script without specifying its directory, the shell can find and execute it:

```bash
example.sh
```

<!-- Add screenshot here -->
