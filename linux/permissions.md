## Linux Permissions
Linux permissions control who can access, modify and execute files and directories.

Permissions are assigned to three categories:

Owner — the user who owns the file or directory Group — users who belong to the group associated with the file or directory Others — everyone else

## Understanding Permissions
The ls -l command can be used to view the permissions of files and directories.

For example:

ls -l

An output may look like:

-rw-r--r-- 1 root root 0 Sep 19 permissions.txt

The first 10 characters show the file type and permissions:

-rw-r--r--

The first character identifies the type:

→ regular file d → directory
The remaining nine characters are split into three groups:

rw- Owner

r-- Group

r-- Other

Each group can contain three types of permissions:

r → read w → write x → execute

→ permission is not granted
For example:

rw-

means the user has read and write permissions but does not have execute permission.

## Changing Permissions
The chmod command is used to change the permissions of files and directories.

Example:

chmod 755 example.txt


Practical Example



<img width="459" height="194" alt="image" src="https://github.com/user-attachments/assets/4d75289e-f405-4399-845f-5bcd0efb2a09" />



* I created a file called `linux.permissions`.
* I then used `ls -l` to view the permissions, which showed `-rw-r--r--`.
* I then used `chmod 775` to change the permissions. I used a chmod calculator to understand which numerical value to use.
* I then used `ls -l` to view the new permissions, which showed `-rwxrwxr-x`.
* This shows that the owner has read, write and execute permissions. The group also has read, write and execute permissions, and others have read and execute permissions but not write permission.



