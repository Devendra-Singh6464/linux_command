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
```

Q11. Edit the Bash startup script (e.g., .bashrc) to set an environment variable named "CUSTOM_PATH" to a specific directory path. Ensure the variable is available in new shell sessions.
```
deepak@bhandari:/home$ echo 'export CUSTOM_PATH=/your/specific/directory/path' >> ~/.bashrc
deepak@bhandari:/home$ source ~/.bashrc
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
 
