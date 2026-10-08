# Linux File Ownership
Linux assigns ownership of files and directories to a user and a group.

The owner and group are important because Linux permissions determine what the owner, group and other users can do with a file or directory.

# Viewing Ownership
The ls -l command can be used to view the owner and group of a file.

For example:

ls -l ownership.txt

An output may look like:

-rw-r--r-- 1 root root 0 Sep 19 ownership.txt

In this example:

-rw-r--r-- 1 root root

The first root is the owner of the file, while the second root is the group associated with the file.

# Changing Ownership
The chown command is used to change the ownership of files and directories.

For example:

chown linux-user ownership.txt

This changes the owner of ownership.txt to linux-user.

The group can also be changed using:

chown :linux-group ownership.txt

Both the owner and group can be changed at the same time:

chown linux-user:linux-group ownership.txt

Practical example



<img width="459" height="194" alt="image" src="https://github.com/user-attachments/assets/09aa15f6-6225-401f-acaa-51a5ed99e45e" />








* I created a file called `linux.ownership`.
* I then created a user called `linux-user` and a group called `linux-group`.
* I used `ls -l` to view the owner and group of the file. The owner was `root` and the group was `root`.
* I then used `chown` to change the owner and group from `root` to `linux-user` and `linux-group`.
* I used `ls -l` again to view the new owner and group. The owner was now `linux-user` and the group was `linux-group`.

