# linux_40_Command

## Q1.How to make a directory.  
   - Command definition in single line:
     - Example: mkdir command is use for create directory  
   - Command:
     - Syntax:'mkdir directory_name'
       ```    
          mkdir demo
       ```
   - Describe the command:
     - Example:
     - mkdir: It is used to create a directory

![image](https://github.com/Devendra-Singh6464/linux_command/assets/136952464/bceefd61-f906-4ce2-a7e9-b92e74a8db80)
   
## Q2. How to Remove a directory.
   To remove a directory in Linux, you can use the rmdir or rm command. However, these commands have some differences in their functionality:

- Using rmdir:

   - Command definition in single line:
     - Example: The rmdir command is specifically used to remove directories.  
   - Command:
     - Syntax: rmdir 'directory_name'
       ```
       rmdir demo
       ```
   - Describe the cammand:
     - Example: 
       - rmdir: The rmdir command is specifically used to remove empty directories.

  ![image](https://github.com/Devendra-Singh6464/linux_command/assets/136952464/6c9bae1c-4af3-4f8f-88a5-636ae168f4d7)

- Using rm:  

The rm command, when used with the `-r` or `-rf` option, can be used to delete directories recursively, along with their contents.

- Syntax to remove an directory:
  rm -d directory_name
 
 ```
  rm -d demo  
 ``` 

  ![image](https://github.com/Devendra-Singh6464/linux_command/assets/136952464/adcf5678-b420-45fd-96e3-eedbedeff926)

- Syntax to remove a directory and its contents recursively (use with caution, as it deletes files and subdirectories inside the specified directory):
  > rm -r directory_name
  ```
    rm -r demo
  ```

 ![image](https://github.com/Devendra-Singh6464/linux_command/assets/136952464/f5bf6563-a40c-4c5d-a399-93627c5f3cfb)


- Syntax to forcefully remove a directory and its contents without prompting for confirmation:
  > rm -rf directory_name   
 ```
   rm -rf demo
```
 ![image](https://github.com/Devendra-Singh6464/linux_command/assets/136952464/e41e6898-648a-4feb-bb33-fa265bd61b29)


Note of Caution: Be extremely cautious while using ` rm`,`-rf`as it will forcefully delete the specified directory and its contents without asking for confirmation

## Q3. Make a copy of a file.  

To make a copy of a file in Linux, you can use the cp command. The basic syntax for copying a file is:

- Syntax:  
  - cp source_file_name destination_file_name
  ```
     cp data.txt data1.txt
  ```
  ![image](https://github.com/Devendra-Singh6464/linux_command/assets/136952464/8c99c7f7-d969-4c99-bec5-6a8bbde6422a)

Replace `source_file` with the file you want to copy and `destination_file` with the name or path where you want to create the copy.

For example, to copy a file named `original.txt` to create a copy named `copy_of_original.txt` in the same directory:


## Q4. Move or rename a file.

To move or rename a file in Linux, you can use the `mv` command, which is capable of performing both renaming and moving files or directories.

Renaming a File:  

To rename a file, use mv followed by the current filename and the desired new filename:

Syntax:
- mv current_file_name new_file_name
```
 mv data.txt newdata.txt 
```
  ![image](https://github.com/Devendra-Singh6464/linux_command/assets/136952464/31306c15-2d3f-48a7-81ff-20de19953cab)

## Q5. Create an empty file.

The `touch` command is often used to create empty files or update timestamps of existing files. If the file does not exist, `touch` will create an empty file.

Syntax: 
- touch filename.ext
```
touch empty_file.txt
```
![image](https://github.com/Devendra-Singh6464/linux_command/assets/136952464/9161e4e9-c680-4a61-ab52-e6cb44beaf7b)

For example:  To create an empty file named empty_file.txt.

## Q5. Remove multiple files with a single command.

To remove multiple files with a single command in Linux, you can use the `rm` (remove) command followed by the names of the files you want to delete.

You can specify the names of the files you want to remove:

Syntax:

- rm file1.txt file2.txt file3.txt
```
 rm data1.txt empty_file.txt newdata.txt
```
 ![image](https://github.com/Devendra-Singh6464/linux_command/assets/136952464/c2484c71-efa0-45e1-bde7-184d2abac7c1)

- Removing Files Interactively:  
You can use the -i flag with rm to prompt for confirmation before deleting each file:

Syntax:
- rm -i file1_name file2_name file3_name
```
rm -i file.txt file2.txt emptly.txt
```
![image](https://github.com/Devendra-Singh6464/linux_command/assets/136952464/4cc5714e-9eb4-4ff6-ac2f-e8ce4975ef88)

This command will prompt for confirmation before deleting each file individually.

- Using Wildcards (*):  
You can also use wildcards to match multiple files based on a pattern:

Remove Files with a Common Pattern:  
For instance, to remove all files with the `.txt` extension in the current directory:

- rm *.txt
```
rm *.txt
```
![image](https://github.com/Devendra-Singh6464/linux_command/assets/136952464/4b029059-a232-4acb-909d-2e8f80b21bdc)


## Q6. Remove content from the folder without removing folder.

To remove all files and subdirectories within a folder without deleting the folder itself, you can use the `rm` command with the `-r` (recursive) option, targeting only the contents of the directory, not the directory itself.

Syntax:
- rm -r /path/to/directory/*
```
rm -r demo/*
```
![image](https://github.com/Devendra-Singh6464/linux_command/assets/136952464/cf7d2a40-2220-4021-8de4-a275110e9d77)

![image](https://github.com/Devendra-Singh6464/linux_command/assets/136952464/7984c8ac-9f52-4327-b57c-1cba463b9a74)

Replace `/path/to/directory` with the actual path to the directory whose contents you want to remove.

## Q7. Create multiple folder(a-z) with a single command.

example command using brace expansion and the mkdir command to create folders from `a` to `z`:

Syntax:
- mkdir {a..z}
```
mkdir {a..z}
```
![image](https://github.com/Devendra-Singh6464/linux_command/assets/136952464/7093c8bf-d482-4812-8d98-155fd1df9ebd)


Executing this command will create directories with the names `a`, `b`, `c`, ..., `z` in the current working directory. Each directory will be named after a letter from `a` to `z`.


## VIM file command -

### to save
```
esc :w
```

### to saver and exit
```
esc : wq!
```
### to quit without saving
```
esc :q!
```
### to copy a line, go to the line
```
esc: yy
```
### to paste line
```
esc:p
```
### to copy multiple line,N lines
```
esc : Nyy
```
### undo changes
```
esc: u
```
### move to top of file
```
esc : 1G
```
### move to bottom of the file
```
esc : G
```
### move to specific line
```
esc : N G
```
### to show line number
```
esc : set number OR : set nu
```
### to remove line number
```
esc : set number OR : set nonu
```
### to search for a word
```
esc : /<word-to-search>
```
### search and replace
```
esc :%s/<world-to-search>/<world-to-replace>
```
### replace globally
```
esc:%s/<world-to-search>/<world-to-replace>/g
```

### to watch all vim command
$ vimtotur

