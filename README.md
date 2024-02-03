# lINUX ASSIGNMENT-04

Q1. Create a directory named "MyFiles" in your home directory. Navigate into this directory and list its contents.
```
deepak@bhandari:~$ mkdir myFiles
deepak@bhandari:~$ cd myFiles/
deepak@bhandari:~/myFiles$ ls
deepak@bhandari:~/myFiles$ 
```
Q2.Copy a file named "document.txt" from your home directory to the "MyFiles" directory. Move the file to a subdirectory named "Documents" within "MyFiles."

```
deepak@bhandari:~$ touch document.txt
deepak@bhandari:~$ cp document.txt myFiles/
deepak@bhandari:~/myFiles$ ls
document.txt
deepak@bhandari:~$ mv myFiles/document.txt myFiles/Documents
deepak@bhandari:~/myFiles$ ls
Documents
deepak@bhandari:~/myFiles$ ll
total 8
drwxrwxr-x  2 deepak deepak 4096 Feb  3 13:16 ./
drwxr-x--- 78 deepak deepak 4096 Feb  3 13:14 ../
-rw-rw-r--  1 deepak deepak    0 Feb  3 13:15 Documents
```
