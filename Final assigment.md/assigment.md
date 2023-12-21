# Question1 


## awk
* Description: 
  * Its a language for processing and displaying text.
* formula/syntax
  * awk + options + {awk command} + file + file to save (optional)
* 3 Examples 
  * awk -F: '{print $1}' /etc/passwd
    * print first field of /etc/passwd file
  * awk -F: '{print toupper(&1)}' /etc/passwd
    * convert the first field to upper/lower case
  * awk '{print length($0)}' /etc/passwd
    * prints the length of a line(record)

## cat
* Description
  * The cat command is used for displaying the content of a file and concatenate files.
* formula/syntax
  * cat + option + files to display 
* 3 examples
  * cat -n /etc/passwd
    * display the content of a file with line numbers.
  * cat -E /etc/passwd
    * display $ at end of each line
  * cat -b 
    * display the content of file with line numbers excluding empty line
  


## cp
* Description
  * copy files and directories
* formula/syntax
  * cp + file to copy + destination 
* 3 Examples
  * cp -r ~/Documents/wallpapers ~/pictures 
    * to copy a directory with absolute path
  * sudo cp -r script.sh program.py home.html assets/ /var/wwr/html/
    * to copy multiple files in a single command 

## cut
* Description 
  * remove sections from each line of files
* formula/syntax
  * cut + option + files
* 3 Examples 
  * cut -d ':' -f1 /etc/passwd 
    * Display a list of all the users in your system 
  * cut -d ':' -f1,7 --output-delimiter=' => ' /etc/passwd
    * Cut a file using a delimiter but changing the delimiter in the output.
  * cut -d ':' -f1,7 /etc/passwd
    * Display a list of all the users in your system with their login shell.


## grep
* Description
  * grep searches for patterns in each file and used to search text in a giving file
* formula/syntax 
  * grep + option search criteria + files 
* 3 examples 
  * grep 'dracula' ~/Documents/dracula.txt
    * search any line that contains the word "dracula" in the given field 
  * grep -wc '/bin/bash' /etc/passwd
    * search the display the total number of times a a giving word appears in a file.
  * grep -n '^[A-Z] ~/Documents/Books/war-and-peace.txt
    * search for all the lines that start with a capital letter
  


## head
* Description
  * Print the first 10 lines of each file to standard output.
* formula/syntax
  * head + option + files
* 3 examples 
  * head -5 ~/Documents/Books/dracula.txt
    * Display the first 5 lines of a file.
  * head ~/Documents/Books/dracula.txt 
    * Display the first 10 lines of a file.
  * head --help
    * display this help.

## ls
* Description
  * ls information about the files
* formula/syntax
  * ls + option + directory to list
* 3 Examples
  * ls -t ~/Documents
    * list all the files in a giving directory sorted by last modified
  * ls -X ~/Documents 
    * List all files in a giving directory sorted by file size.
  * ls -r ~/Documents 
    * list all the files in a given directory sorted by name in reverse order. 

  

## man
* Description
  * manual pages are documentation files that describe linux shell
* formula/syntax
  * man + command 
* 3 Examples
  * man 5 passwd
    * open a specific man page for the passwd command 
  * man -f passwd
    * show the man page section of the passwd command
  * man -a passwd
    * show all the available pages of a command.


## mkdir
* Description 
  * is used for creating a single directory or multiple directories.
* formula/syntax 
  * mkdir + the name of the directory 
* 3 Examples
  * mkdir wall papers 
    * create a directory in the present working directory 
  * mkdir ~/wallpaper forest
    * create a directory in a different directory using absolute path 
  * mkdir -p wallpapers_others/movies 
    * create a directory with a parent directory at the same time.


## mv
* Description 
  * moves and renames directories 
* formula/syntax
  * mv + source + destination
    * the basic formula of the mv command 
  * mv + file/directory to rename + new name
    * for renaming files/directories the formula remains the same
* 3 Examples 
  *  mv Downloads/homework.pdf Documents/
    * to move a file from a directory to another using relative path
  * sudo mv ~/Downloads/theme /usr/share/themes
    * to move a directory from one directory to another using absolute path
  * mv homework.dox cis106homework.docx
    * to rename a file 


## tac
* Description 
  * the tac command is used for displaying the content of a file in reverse order
* formula/syntax
  * tac + option + files to display 
* 3 Examples
  * tac todo.md
    * display the content located in the pwd
  * tac ~/Documents/todo.md
    * display the content of a file using absolute path. 


## tail
* Description 
  * the tail command displays the last N number of lines, it prints the last 10 lines.
* formula/syntax
  * tail + option + file 
* 3 examples
  * tail ~/Documents/Books/dracula.txt
    * display the last 10 lines of a file.
  * tail -5 ~/Documents/Book/dracula.txt
    * Display the last 5 lines of a file.


## touch
* Description
  * is used for creating a files 
* formula/syntax
  * touch + file name
* 3 examples 
  * touch list
    * to create a file called list
  * touch list_of_cars.txt script.py names.csv
    * to create several files
  * touch Downloads/games2.txt
    * to create a file using relative path.


## tr
* Description 
  * the tr command is used for translating or deleting characters from standard output.
* formula/syntax 
  * standard output | tr + option + set + set 
* 3 examples 
  *  cat file.txt | tr '.' ',' 
    * translate one character to another ( for example a period with a comma)
  * cat program.py | tr "[:space;]" '\t'
    * translate white space into tabs
  * cat file.py | tr -s "[:space:] ' '
    * translate tabs into space. 


## tree
* Description
  * list contents of directories in a tree-like format.
* formula/syntax 
  * tree + option + directory 
* 3 Examples 
  * tree -d 
    *List directories only. 
  * tree -l
    *  Follows symbolic links if they point to directories, as if they were  directories
  * tree -f 
    * Prints the full path prefix for each file



# Question 2
**How to work with multiple terminals open?**
just press the right terminal to add a terminal.
**How to work with manual pages?**
type man followed by the name of command you want to look up,

**How to parse (search) for specific words in the manual page**
grep / search  or man -k 
**How to redirect output (> and |)**
If I want to redirect the output of the ls command to a file named pizza.txt I can use ls > output.txt
The | operator is used to pipe the output of one command to another command.
**How to append the output of a command to a file**
to append the out put I use >>
**How to use wildcards For copying and moving multiple files at the same time**
using the * for copying and moving or removing all files
**How to use brace expansion For creating entire directory structures in a single command**
mkdir -p music/{jazz,rock}/{mp3files,videos}/new{1..3}

