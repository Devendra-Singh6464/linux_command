# lINUX ASSIGNMENT-04

Q1. Create a directory named "MyFiles" in your home directory. Navigate into this directory and list its contents.
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

```

Q6. Rename all files in the "Documents" subdirectory of "MyFiles" with a ".bak" extension. Ensure the original file names are preserved.
```

```
