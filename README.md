# lINUX ASSIGNMENT-04

Q1. Create a directory named "MyFiles" in your home directory. Navigate into this directory and list its contents.
```
deepak@bhandari:~/home$ ls
deepak  linux_command.md
deepak@bhandari:~/home$ mkdir myFile
deepak@bhandari:~/home$ ls
deepak  linux_command.md  myFile
deepak@bhandari:~/home$ cd myFile/
deepak@bhandari:~/home/myFile$ ls
deepak@bhandari:~/home/myFile$ 
```

Q2.Copy a file named "document.txt" from your home directory to the "MyFiles" directory. Move the file to a subdirectory named "Documents" within "MyFiles."
```
deepak@bhandari:/home/myFile$ ls
Documents
deepak@bhandari:/home/myFile$ cd ..
deepak@bhandari:/home$ sudo mv document.txt /home/myFile/Documents/
deepak@bhandari:/home$ cd my files
bash: cd: too many arguments
deepak@bhandari:/home$ cd myfile
bash: cd: myfile: No such file or directory
deepak@bhandari:/home$ cd myFile
deepak@bhandari:/home/myFile$ ls
Documents
deepak@bhandari:/home/myFile$ cd Documents/
deepak@bhandari:/home/myFile/Documents$ ls
document.txt
deepak@bhandari:/home/myFile/Documents$ 
```

Q3. Create an empty file named "notes.txt" in the "MyFiles" directory. Afterward, delete the file.
```
deepak@bhandari:/home/myFile$ sudo touch notes.txt
deepak@bhandari:/home/myFile$ ls
Documents  notes.txt
deepak@bhandari:/home/myFile$ sudo rm notes.txt 
deepak@bhandari:/home/myFile$ ls
Documents
deepak@bhandari:/home/myFile$ 
```

Q4. Create a hard link named "hardlink.txt" for the file "document.txt" within the "Documents" subdirectory. Also, create a symbolic link named "symlink.txt" in the same location.
```
deepak@bhandari:/home/myFile/Documents$ sudo ln document.txt /home/myFile/Documents/hardlik.txt
deepak@bhandari:/home/myFile/Documents$ ls
document.txt  hardlik.txt
deepak@bhandari:/home/myFile/Documents$ sudo ln -s document.txt /home/myFile/Documents/softlink.txt
deepak@bhandari:/home/myFile/Documents$ ls
document.txt  hardlik.txt  softlink.txt
```
Q5. In the "MyFiles" directory, use a single command to list all files that start with the letter "a" and have a ".txt" extension.
```
deepak@bhandari:/home$ ls myFile/a*.txt
myFile/ab1.txt  myFile/ab2.txt  myFile/ab3.txt  myFile/ab4.txt  myFile/ab5.txt
deepak@bhandari:/home$ 
```

Q6. Rename all files in the "Documents" subdirectory of "MyFiles" with a ".bak" extension. Ensure the original file names are preserved.
```
deepak@bhandari:/home/myFile/Documents$ sudo rename -n 's/\.txt$/.bak/' *.txt
rename(document.txt, document.bak)
rename(hardlik.txt, hardlik.bak)
rename(softlink.txt, softlink.bak)

deepak@bhandari:/home/myFile/Documents$ sudo rename 's/\.txt$/.bak/' *.txt
deepak@bhandari:/home/myFile/Documents$ ls
document.bak  hardlik.bak  softlink.bak
deepak@bhandari:/home/myFile/Documents$ 
```


Q7. Use a wildcard character to copy all files from the "Documents" subdirectory of "MyFiles" to another directory named "Backup."
```

```

Q8. Execute the ls command to list files in the current directory. Save the output to a file named "file_list.txt." Then, use a pipe to filter the output through grep to display only files with a ".txt" extension.
```
deepak@bhandari:/home$ ls -p file_list.txt 
file_list.txt
deepak@bhandari:/home$ grep '\.txt$' file_list.txt 
deepak@bhandari:/home$ 
```

Q9. Create a new text file named "my_notes.txt" using the touch command. Open the file in the Vim editor, add some text, and save the changes.
```
deepak@bhandari:/home$ sudo touch my_notes.txt
deepak@bhandari:/home$ vim my_notes.txt
Press i to enter insert mode.
Add your text.
Press Esc to exit insert mode.
Type :wq and press Enter to save the changes and exit Vim.
```

Q10.Run the date command and store the output in a variable named "current_date." Display the value of the variable and append it to the "my_notes.txt" file.
```
deepak@bhandari:/home$ current_date=$(date)
deepak@bhandari:/home$ echo "Current date: $current_date"
Current date: Saturday 03 February 2024 06:05:49 PM IST
sudo su
echo "$current_date" >> my_notes.txt
```

Q11. Edit the Bash startup script (e.g., .bashrc) to set an environment variable named "CUSTOM_PATH" to a specific directory path. Ensure the variable is available in new shell sessions.
```
deepak@bhandari:/home$ echo 'export CUSTOM_PATH=/your/specific/directory/path' >> ~/.bashrc
deepak@bhandari:/home$ source ~/.bashrc
```

Q12. Use the echo command to add a new line of text to the "my_notes.txt" file without overwriting existing content. Verify that the new text is appended.
```

```

Q13. List all files in the "/etc" directory, filter the output to include only those containing the word "conf," and save the result to a file named "conf_files.txt."
```

```

Q14. Open the "my_notes.txt" file in Vim. Use Vim's search and replace functionality to replace all occurrences of the word "important" with "critical." Save the changes.
```
deepak@bhandari:~$ vim my_notes.txt
Inside Vim, press `Esc` to ensure you are in normal mode.
Type the following command to search and replace:
```:%s/important/critical/g```

Save the changes and exit Vim by typing:
:wq
```

Q15. Create a new user account named "john_doe." Set the user's home directory to "/home/john_doe" and assign the user to the "users" group.
```
deepak@bhandari:~$ sudo useradd -m -d /home/john_doe -g users john_doe
[sudo] password for deepak:
```

Q16. Add the user "john_doe" to the sudoers file, allowing them superuser privileges. Confirm that "john_doe" can execute commands with sudo.
```
sudo visudo
Inside visudo file write below content and save it and exit

john_doe ALL=(ALL:ALL) ALL
Write any desire path

sudo ls /Desktop
sudo su
 
```

Q17. Modify the user account "john_doe" to change the default shell to "/bin/bash" and set the account's expiration date to one month from today.
```
sudo chsh -s /bin/bash john_doe
sudo chage -E $(date -d "+1 month" +"%Y-%m-%d") john_doe
```

Q18. Create a new group named "development_team." Add "john_doe" to this group and verify the group's existence.
```
sudo groupadd development_team
sudo usermod -aG development_team john_doe
getent group development_team
```

Q19. Remove "john_doe" from the "users" group and add them to the "development_team" group. Confirm the changes.
```
sudo gpasswd -d john_doe users
sudo usermod -aG development_team john_doe
groups john_doe
```

Q20. Delete the user account "john_doe" and ensure that their home directory is also removed.
```
sudo userdel -r john_doe
groups jhon_doe
```

Q21.	Delete the group "development_team" and ensure that all users previously belonging to the group are appropriately handled.
```
getent group development_team
sudo usermod -g users jhon_doe
sudo groupdel development_team
getent group development_team
```

Q22.	Implement a password policy that requires users to change their passwords every 90 days. Apply this policy to all existing and new user accounts.
```
sudo chage -M 90 -m 0 -W 7 -I 30 -E -1 $(cut -d: -f1 /etc/passwd)
sudo vim /etc/login.defs
```
Inside this file add max pass day as 90 and min pass day as 0
```
PASS_MAX_DAYS   90
PASS_MIN_DAYS   0
```

Q23.	Manually lock the user account "john_doe." Attempt to log in as "john_doe" to confirm that the account is locked. Then, unlock the account.
```
sudo passwd -l john_doe
su - john_doe
sudo passwd -u john_doe
```

Q24.	Use the id command to display detailed information about the "john_doe" user, including user ID, group ID, and supplementary groups.
```
id john_doe
id -u john_doe
id -g john_doe
id -G john_doe
```

Q25.	Configure the password aging for the user "john_doe" to enforce a maximum password age of 60 days. Confirm that the changes take effect.
```
sudo chage -M 60 john_doe
sudo chage -l john_doe
```
