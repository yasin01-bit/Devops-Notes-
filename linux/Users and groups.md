## Creating user
<img width="759" height="872" alt="image" src="https://github.com/user-attachments/assets/410fabcf-d440-469c-a739-db673cea1686" />





- Here i created a user called 'myuser' using the useradd command 
- i then used the 'su' command to log in
- i got the warning as i have only just created the user, so no file or directory exists for it
- i then used the 'whoami' command to verify i am a new user on the system
- i then used sudo apt-get update command to confirm i dont have sudo privileges
- i then used command sudo usermod -aG to give my user sudo privileges
- i then used su 'command' to log in again, followed by sudo passwd to login with my password which is hidden on the screenshot.
- i then used sudo apt-get update to complete the set up



## Revoking user access from sudo privileges
<img width="439" height="63" alt="image" src="https://github.com/user-attachments/assets/9fab34ab-9ab6-4531-91d1-08138a1d55e0" />



   - sudo deluser myuser sudo - is the command i used to revoke access 









## Groups 
<img width="368" height="131" alt="image" src="https://github.com/user-attachments/assets/c4502f92-bd40-4ab3-a368-5355074b7afb" />

- first used 'cat /etc/group' command to identify groups in linux file system
- i created a group via the 'sudo groupadd' command, (then validated this group is on linux filesystem and was created by using above command)
- Next stage will be creating a user as my last user wasnt saved and then adding this user to my group 
