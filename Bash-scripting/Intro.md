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

<!-- Add your screenshots here, e.g. ![Creating the script](images/screenshot1.png) -->

I executed the script in three ways:

| Command | What it does |
|---|---|
| `./example.sh` | Tells the shell to run the script from the current directory |
| `sh example.sh` | Runs the script using the `sh` interpreter |
| `bash example.sh` | Runs the script using the `bash` interpreter |

Below is the Bash script I wrote, which can be executed using `./`, `sh` and `bash`.

<!-- Add screenshot of the script here -->

---

## Comments

Comments are lines in a script that are **not executed** as part of the code. They serve as informative text for the reader.

There are two types of comments:

- **Single line comments:** start the line with `#`
- **Multiline comments:** use `:` followed by text inside single quotation marks `' '`
  

<img width="1488" height="564" alt="image" src="https://github.com/user-attachments/assets/80b9548e-c731-4366-94fc-37ea8a7c7c75" />


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

```bash
sudo mv example.sh /usr/local/bin/
sudo chmod +x /usr/local/bin/example.sh
```

Now when I run the script without specifying its directory, the shell can find and execute it:

```bash
example.sh
```

<!-- Add screenshot here -->
