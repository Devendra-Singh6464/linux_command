# linux_40_Command


## Q1.How to make a directory.  
   - Command definition in single line:
     - Example: mkdir command is use for create directory  
   - Command:
     - Syntax:'mkdir directory_name'  
     >mkdir demo
   - Describe the command:
     - Example:
     - mkdir: It is used to create a directory
     
![Alt text](<Screenshot from 2023-12-14 10-19-34-1.png>)

## Q2. How to Remove a directory.
    To remove a directory in Linux, you can use the rmdir or rm command. However, these commands have some differences in their functionality:

- Using rmdir:

   - Command definition in single line:
     - Example: The rmdir command is specifically used to remove directories.  
   - Command:
     - Syntax: rmdir 'directory_name'
     > Example: rmdir demo
   - Describe the cammand:
     - Example: 
       - rmdir: The rmdir command is specifically used to remove empty directories.

  ![Alt text](<Screenshot from 2023-12-14 10-20-20-1.png>)

- Using rm:  

The rm command, when used with the `-r` or `-rf` option, can be used to delete directories recursively, along with their contents.

- Syntax to remove an directory:
  > rm -d directory_name 

  ![Alt text](<Screenshot from 2023-12-14 11-01-44.png>)

- Syntax to remove a directory and its contents recursively (use with caution, as it deletes files and subdirectories inside the specified directory):
  > rm -r directory_name

  ![Alt text](<Screenshot from 2023-12-14 11-02-54.png>)


- Syntax to forcefully remove a directory and its contents without prompting for confirmation:
  > rm -rf directory_name   

  ![Alt text](<Screenshot from 2023-12-14 11-03-58.png>)

Note of Caution: Be extremely cautious while using ` rm`,`-rf`as it will forcefully delete the specified directory and its contents without asking for confirmation


## Q3. Make a copy of a file.  

To make a copy of a file in Linux, you can use the cp command. The basic syntax for copying a file is:


- Syntax:  
  - cp source_file_name destination_file_name
  > cp data.txt data1.txt

  ![Alt text](<Screenshot from 2023-12-14 11-45-42.png>)  


Replace `source_file` with the file you want to copy and `destination_file` with the name or path where you want to create the copy.

For example, to copy a file named `original.txt` to create a copy named `copy_of_original.txt` in the same directory:


## Q4. Move or rename a file.

To move or rename a file in Linux, you can use the `mv` command, which is capable of performing both renaming and moving files or directories.

Renaming a File:  

To rename a file, use mv followed by the current filename and the desired new filename:

Syntax:
- mv current_file_name new_file_name
> mv data.txt newdata.txt 

  ![Alt text](<Screenshot from 2023-12-14 12-00-03.png>)


## Q5. Create an empty file.

The `touch` command is often used to create empty files or update timestamps of existing files. If the file does not exist, `touch` will create an empty file.

Syntax: 
- touch filename.ext

>touch empty_file.txt

![Alt text](<Screenshot from 2023-12-14 12-09-38.png>)

For example:  To create an empty file named empty_file.txt.


## Q5. Remove multiple files with a single command.

To remove multiple files with a single command in Linux, you can use the `rm` (remove) command followed by the names of the files you want to delete.

You can specify the names of the files you want to remove:

Syntax:

- rm file1.txt file2.txt file3.txt
> rm data1.txt empty_file.txt newdata.txt

 ![Alt text](<Screenshot from 2023-12-14 12-34-05.png>)


- Removing Files Interactively:  
You can use the -i flag with rm to prompt for confirmation before deleting each file:

Syntax:
- rm -i file1_name file2_name file3_name

>rm -i file.txt file2.txt emptly.txt

![Alt text](<Screenshot from 2023-12-14 12-38-09.png>)

This command will prompt for confirmation before deleting each file individually.


- Using Wildcards (*):  
You can also use wildcards to match multiple files based on a pattern:

Remove Files with a Common Pattern:  
For instance, to remove all files with the `.txt` extension in the current directory:

- rm *.txt
>rm *.txt

![Alt text](<Screenshot from 2023-12-14 12-42-29.png>)


## Q6. Remove content from the folder without removing folder.

To remove all files and subdirectories within a folder without deleting the folder itself, you can use the `rm` command with the `-r` (recursive) option, targeting only the contents of the directory, not the directory itself.

Syntax:
- rm -r /path/to/directory/*
>rm -r demo/*

![Alt text](<Screenshot from 2023-12-14 13-07-04.png>)

![Alt text](<Screenshot from 2023-12-14 13-07-19.png>)

Replace `/path/to/directory` with the actual path to the directory whose contents you want to remove.


## Q7. Create multiple folder(a-z) with a single command.

example command using brace expansion and the mkdir command to create folders from `a` to `z`:

Syntax:
- mkdir {a..z}
>mkdir {a..z}

![Alt text](<Screenshot from 2023-12-14 12-52-36.png>)

Executing this command will create directories with the names `a`, `b`, `c`, ..., `z` in the current working directory. Each directory will be named after a letter from `a` to `z`.
