Users and Groups
Linux uses users and groups to manage access to files, directories and system resources.

Users
A user account represents an individual or service that can interact with a Linux system.

Each user has their own account and permissions.

Creating a user
The useradd command can be used to create a new user.

useradd username

Viewing users
The /etc/passwd file contains information about user accounts on the system.

The cat command can be used to view its contents:

cat /etc/passwd

Groups
Groups are used to organise users and manage permissions.

A user can belong to one or more groups.

Creating a group
The groupadd command can be used to create a new group.

groupadd groupname

Adding a user to a group
The usermod command can be used to modify a users account. The -aG options can be used to add a user to an existing group.

usermod -aG groupname username

Checking group membership
The groups command shows the groups that a user belongs to.

groups username

Practical Example
I practised creating a new user and group using Killercoda.

<img width="676" height="150" alt="image" src="https://github.com/user-attachments/assets/e47b0675-5c1c-43e1-a1a1-a8555a3da15c" />


image
I first created a group called linux-group:

groupadd linux-group

I then created a user called linux-user:

useradd linux-user

Next, I added linux-user to the linux-group supplementary group:

usermod -aG linux-group linus-user

Used the groups command to check which groups the user belonged to:

groups linux-user

The output showed:

linux-user : linux-user linux-group

This shows that linux-user belongs to both its primary group, linux-user, and the supplementary group, linux-group.

I then used the id command to view more detailed information about the user:

id linux-user

The output was:

uid=1002(linux-user) gid=1003(linux-user) groups=1003(linux-user),1002(linux-group)

This showed the user's UID, primary GID and group memberships.
