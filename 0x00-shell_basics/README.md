  [ALX COHORT]![image](https://user-images.githubusercontent.com/105258746/187828479-63082744-4c64-4bac-9f56-e32bae98a9a9.png)

# SHELL, BASICS BASH PROJECTS

## TASKS

### Note: When doing this project, After using text editor of your choice to create and access the file on insert mode.Ensure the first line is always having # !/bin/bash, then the second line is having the correct command/answer.
(From your terminal, convert the file created to `SCRIPT` i.e: cdmod u+x 1-listit)

## 0. Write a script that prints the absolute path name of the current working directory.
### File: 0-current_working_directory 
``input: pwd`` *(print working directory)*
    
## 1. Display the contents list of your current directory.
### File: 1-listit
``input: ls`` *(list directory contents)*
    
## 2. Write a script that changes the working directory to the user’s home directory.
### File: 2-bring_me_home
``input: cd`` *(change directory)*
    
## 3. Display current directory contents in a long format.
### File: 3-listfiles
``input: ls -l`` *(list directory contents in long form)*
    
## 4. Display current directory contents, including hidden files (starting with .). Use the long format.
### File: 4-listmorefiles
``input: ls -la`` *(list directory contents in long form, including hidden files)*
    
## 5. Display current directory contents.
### File: 5-listfilesdigitonly
``input:  ls -la`` *(Note: Are files inherently ordered?)*
    
## 6. Create a script that creates a directory named my_first_directory in the /tmp/ directory.
### File: 6-firstdirectory
``input: mkdir /tmp/my_first_directory`` *(Create a holberton directory inside the tmp directory)*
   
## 7. Move the file betty from /tmp/ to /tmp/my_first_directory.
### File: 7-movethatfile
``input: mv /tmp/betty /tmp/my_first_directory/betty`` *(Move file betty, which is located inside the tmp directory, to the holberton directory, which is also located inside the tmp directory. This exercise required some dir traversing.)*
    
## 8. Delete the file betty.
### File: 8-firstdelete
``input: rm /tmp/my_first_directory/betty``  *(Remove file betty located in tmp/my_first_directory directory.)*
    
## 9. Delete the directory my_first_directory that is in the /tmp directory.**
### File: 9-firstdirdeletion
``input: rmdir /tmp/my_first_directory``     *(Remove directory my_first_directory located in directory tmp.)*
    
## 10. Write a script that changes the working directory to the previous one.
### File: 10-back
``input: cd -``    *(Change directory to the previous directory you were in.)*
    
## 11. Write a script that lists all files (even ones with names beginning with a period character, which are normally hidden) in the current directory and the parent of the working directory and the /boot directory (in this order), in long format.
### File: 11-lists
``*input: ls -la . .. /boot``   *(List all files/directories, including hidden files/directories, from 3 separate directories: current directory, parent of working directory, and /boot directory. The ls command allows multiple directories to be listed separated by spaces.)*
    
## 12. Write a script that prints the type of the file named iamafile. The file iamafile will be in the /tmp directory when we will run your script.
### File: 12-file_type
``input: file /tmp/iamafile``  *(Prints the type of file iamafile.)*
    
## 13. Create a symbolic link to /bin/ls, named __ls__. The symbolic link should be created in the current working directory.
### File: 13-symbolic_link
``input: ln -s /bin/ls __ls__``  *(Create a symbolic link named ls for /bin/ls)*
    
## 14. Create a script that copies all the HTML files from the current working directory to the parent of the working directory, but only copy files that did not exist in the parent of the working directory or were newer than the versions in the parent of the working directory.
### File: 14-copy_html
``input: cp -u *.html ..``   *(Copy all html files from the current directory to the parent directory, but only copy files that didn't exist in the parent directory or are newer versions than the ones that already exist in the parent directory. The -u option didn't show on the terminal manual page. The -u option copies the file into the directory if its a newer version. If the file doesn't exist in the directory, it will copy over. The -n option works for copying files that don't exist in the parent directory, but it doesn't check if the file is a newer version or not.)
    
## 15. Create a script that moves all files beginning with an uppercase letter to the directory /tmp/u. You can assume that the directory /tmp/u will exist when we will run your script.
### File: 100-lets_move
``input: mv [[:upper:]]* /tmp/u``  *(Move all files that begin with a capital letter to /tmp/u)*
    
## 16. Create a script that deletes all files in the current working directory that end with the character ~.
### File: 101-clean_emacs
``input: rm *~``   *(Deletes all files in the current directory that end with a ~)*

## 17. Create a script that creates the directories welcome/, welcome/to/ and welcome/to/school in the current directory. You are only allowed to use two spaces (and lines) in your script, not more.
### File: 102-tree
``input: mkdir -p welcome/to/school``   *(Create directory `welcome` in current directory. Create directory `to` inside directory `welcome`. Create directory `holberton` inside directory `to`. The -p option creates any intermediate directories in the path argument.)*

## 18. Write a command that lists all the files and directories of the current directory, separated by commas (,) and hidden directory names(..) should end with a slash (/)
### File: 103-commas
``input:  ls -map*``
*(List all files and directories of the current directory, separated by commas. Directory names should end with a `/`. The listing should be alph ordered, except for dot (.) or dot dot (..), which should be listed at the beginning.)*
  The -a option is to show any hidden files.
  The -p option writes a `/` at the end of directory names.
  The -m option streams the output, separating each listing with commas.
  
## 19. Create a magic file school.mgc that can be used with the command file to detect School data files. School data files always contain the string SCHOOL at offset 0.
### File: school.mgc
``input 1: 0 string SCHOOL School data``

``input 2: !:mime School``

*Then_on_your_terminal_run:* ``file -C -m school.mgc``


Create a magic file called `school.mgc` that can be used with the command `file` to detect `School` data files. Holberton data files always contain "SCHOOL" at offset 0.

  This exercise was much different from the previous exercises. From what I understand, the magic file is used to detect patterns in files and will give a specified output depending on a matching pattern.
  The first argument is a number representing the offset.
  The second argument is the data type you are searching for. In our case, it is a string.
  The third argument is the data you are searching for. In our case, "SCHOOL", which we specified as a string in the second argument.
  The fourth argument is the message you want to output on match. If the search matches, it will output this message.
  The last argument is separated by a line. Since the fourth argument can be long and contain multiple strings, we separate the fourth and fifth arguments with this new line. This last argument can be multiple different things. In this case, a MIME type.
  According to bash manual, a "MIME type is given on a separate line, which must be the next non-blank or comment line after the magic line that identifies the file type".
  I knew to search for a MIME type because the example provided:
  $ file --mime-type -m school.mgc *
  The above returns message "School" when matching a MIME ?? Not exactly sure, but this is what I can tell from what I've tested out and can see from the output and examples.
  $ file -m school.mgc *
  The above will return message "School data" for any offset 0 "SCHOOL" matches.
  A cool thing to note is that the `file` command is compiling and running the magic file. So there is no need to compile to magic "permanently".
  NOTE: Compiling a magic source file:
  $ file -C -m <filename>.mgc
  This produces the compiled magic file.
  $ file -i -m <filename>.mgc *
  This allows you to use the compiled file by specifying its name using the -m switch again.




