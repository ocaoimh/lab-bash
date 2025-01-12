![logo_ironhack_blue 7](https://user-images.githubusercontent.com/23629340/40541063-a07a0a8a-601a-11e8-91b5-2f13e4e6b441.png)

# Lab | Bash

## Introduction

In this lab we are going to practice with [`bash`](<https://en.wikipedia.org/wiki/Bash_(Unix_shell)>), a shell and command-line language!

## Setup

1. Fork the repo in your git hub account and then clone the folder "lab-bash" to your machine and navigate to it folder.

2. Check the contents of the folder using the "ls" command

```shell
$ ls
```

and you should see the following:

```shell
exercises  inputs  lorem  lorem-copy  modules  outputs  README.md
```

3. Stay in the same directory/folder and complete the following exercises.

## Exercises

1. Using the echo command print in console "Hello World". Here is some info about echo command [https://discuss.codecademy.com/t/what-are-practical-uses-of-the-echo-command/394788]
2. Create a new directory called `new_dir`.

`mkdir new_dir`


4. Delete/Remove the directory `new_dir`.

`rmdir new_dir`

5. Copy the file `sed.txt` from the `lorem` folder and paste it to the folder `lorem-copy` folder.

`cp  /Users/cormacokeeffe/Documents/GitHub/lab-bash/lorem/sed.txt /Users/cormacokeeffe/Documents/GitHub/lab-bash/lorem-copy`


6. Copy the other two files from the `lorem folder` to `lorem-copy` folder in just one line using semicolon `;`.

`cp at.txt at.txte lorem.txt /Users/cormacokeeffe/Documents/GitHub/lab-bash/lorem-copy`

6. Show the `sed.txt` file content from the `lorem` folder.

`less sed.txt`

### q to escape

8. Show the `at.txt` file and `lorem.txt` file contents from `lorem` folder.


`less at.txt`

`less lorem.txt`


10. Print the first 3 rows in `sed.txt` file from lorem-copy folder.

`head -3 sed.txt`


12. Print the last 3 rows in `sed.txt` file from lorem-copy folder.

`tail -3 sed.txt`


14. Add `Homo homini lupus.` at the end of `sed.txt` file in the `lorem-copy` folder.

`echo 'Homo homini lupus' >> sed.txt`


16. Print the last 3 rows in `sed.txt` file from `lorem-copy` folder. You should see `Homo homini lupus.`.

`tail -3 sed.txt`


18. `sed` command is used to replace the text in a file. Use the `sed` command to replace all occurances of `et` with `ET` in the file `at.txt` file present in the folder `lorem`. You can use the following link to refer to `sed` commands [https://www.linode.com/docs/guides/manipulate-text-from-the-command-line-with-sed/]

`sed -i'' -e 's/et/ET/g' at.txt *`

### NB: regular sed (sed -i 's/et/ET/' at.txt
) didn't work but found this solution here: https://singhkays.com/blog/sed-error-i-expects-followed-by-text/



Check the contents of the sed.txt file using `cat` command.

`cat at.txt`


13. Find who is the system user. 

`who
id cormacokeeffe `


15. Find the current path of the directory you are in.

`pwd`

17. List all files with the extension `.txt` in lorem folder.

`ls *.txt /Users/cormacokeeffe/Documents/GitHub/lab-bash/lorem`


19. Count the rows in `sed.txt` file from lorem folder. Look concatenate `cat` and `wc` with the pipe `|`.

`wc -l sed.txt  /Users/cormacokeeffe/Documents/GitHub/lab-bash/lorem` 


`wc -l sed.txt  /Users/cormacokeeffe/Documents/GitHub/lab-bash/lorem | cat sed.txt` 


21. Count the **files** which start with `lorem` in all directories.

ls -d *lorem* | wc -l 



## Bonus

20. Store your `name` in a variable with `read` command.
```shell
read Cormac
```

22. Print that variable.

```shell
echo Cormac
```

24. Create a new directory named with variable `name`.

```shell
mkdir Cormac
```

26. Remove that directory.

```shell
rmdir Cormac
```
