# Files and Directories

Linux uses files and directories to organise information and data.

## Directories

A directory is used to organise and contain files and other directories.

### Creating a directory

The `mkdir` command creates a new directory.

```bash
mkdir linux-demo
```

### Navigating directories

The `cd` command is used to move between directories.

```bash
cd linux-demo
```

The `pwd` command shows the current working directory.

```bash
pwd
```

### Parent directory

`..` represents the parent directory. Running `cd ..` moves from the current directory to the directory above it.

```bash
cd ..
```

## Files

Files can contain information such as text, scripts or other data.

### Creating a file

The `touch` command can be used to create empty files.

```bash
touch example.txt
```

### Displaying a file

The `cat` command can be used to display the content of a file.

```bash
cat example.txt
```


## Practical example

i practised creating and navigating directories and creating a file using killerkoda


<img width="343" height="286" alt="image" src="https://github.com/user-attachments/assets/6cfd6255-1c96-4b8e-b1ce-07137f7ef62c" />






- Used `pwd` to show the full path of the current working directory, which confirmed I was in the `/root` directory.
- Used `mkdir` to create a directory called `linux-demo`.
- Used `ls` to list the contents of the directory. There were no files at this point, so nothing was displayed.
- Used `cd` to navigate into the `linux-demo` directory.
- Used `touch` to create a file called `example.file`.
- Used `cd ..` to navigate back to the parent directory, `/root`.




