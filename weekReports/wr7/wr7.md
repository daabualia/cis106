---
name: Dana Abualia
semester: fall 23
course: cis106
---

# Week Reports 7

## Commands 

* **The cat command:**
  * The cat command is used for displaying the content of a file.
  * The formula of the command is **(cat + option + file).**
    * **Two example:**
      * cat -n ~/Documents/bible.txt , -n is to display the content of a file with line numbers.
      * cat -b ~/Documents/todo.md , -b is to display the content of a file with line numbers excluding empty lines.

* **The tac command:**
  * The tac command is used for diplaying the content of file in reverse order.
  * The formula of the tac command is **(tac + option + file).**
      *  **Two example:**
         *   tac bible.txt
         *   tac ~/Documents/todo.md

    
  * **The head command:**
    * The head command displays the top N number of lines of a given file. First 10 lines of  a file.
    * The formula of the command **(head + option + file).**
      * **Two example:**
        * head ~/Documents/Books/dracuala.txt
        * head -5 ~/Documents/Book/dracula.txt, the -5 display the first 5 lines of a file.

* **The tail command:**
  * The tail command displays the last N number of lines of a given file. The last 10 lines.
  * The formula of the tail command is **(tail + option + file)**
    * **Two example:**
      * tail ~/Documents/Books/dracula.txt
      * tail -5 ~/Documents/Books/dracula.txt , -5 displays the last 5 lines of a file.

* **The cut command.**
  * The cut command is used to extract a specific section of each line of a file and display it to the screen.
  * The formula is **(cut + option + file)**
    * **Two examples:**
      * cut -d ':' -f1 /etc/passwd , display a list of all users in your system.
      * cut -d ':' -f1,7 /etc/passwd , display a list of all users in your system with their login shell.

* **The paste command.**
  * Th paste command is used for joining files horizontally in columns.
  * The formula is ** Paste + option +file.**
    * **Two examples:**
      * paste bible.txt book.txt
      * paste -d ":" bible.txt book.txt, merging two files using a different delimiter. 

* **The Sort command:**
  * The sort command is used for sorting files.
  * The formula for sort command **sort + option + file.**
    * **Two examples:**
      * sort -o sorted.lst usr.lst, sort a file and save the output to a new file.
      * sort -r users.txt, sort a file in a reserve order.

* **The wc command:**
  * The wc command is used for printing the number of lines, characters and bytes in a file.
  * The formula is **wc + option + file**
    * **Two Examples:**
      * wc -m users.txt , Display the number of characters in a file.
      * wc -l users.txt , Display the number or lines in a file.

* **The tr command**
  * The tr command is used for translating or deleting characters from a standard output.
  * The formula is ** standard output | tr + option + set
    * **For examples**
      * cat file.txt | tr ',' '.'      , translate one character to another.
      * cat program.py | tr "[:space:]" '\t' , translate white space in to tabs.

* **The diff command**
  * The diff command compares files and displays the differences between them.
  * The formula is **diff + option + file1 + file2
    * **Two examples**
      * diff cars.csv cars-backup.csv
      * diff -y cars.csv cars-backup.csv. , display the difference between two files in a column format.
* **The grep command**
  * Grep is used to search a text in given file. greb works line by line basis.
  * The formula is **grep + option + search criteria + file.**
    * ** Two Examples:**
      * grep -n 'dracula' ~/Documents/Books/dracula.txt , search any line that contains the word dracula regardless of case with number line.
      * grep -o 'dracula' ~/Documents/Books/dracula.txt , search and match only the word.

* **The Awk command**
  * The awk command is a scripting language used for processing and displaying text.
  * The formula is **awk + option + {awk command} +file +file to save.
    * **Five Examples:**
      * awk -F: '{print $1} /etc/passwd , it prints the first field of the file.
      * awk -F: '{print $NF}' /etc/passwd , it prints the last field of the file.
      * awk -F: '{print toupper($1)}' /etc/passwd , convert the first field to upper/lower case.
      * awk '{print length($0)}' /etc/passwd , it prints the length of line. 
      * awk 'NR > 3 { print }" /etc/passwd , it starts printing a file from a given line.(exclude the first 2 lines).
* **The Sed command:**
  * The sed command is a stream editor that perform operations on files and standard output.
  * The formula is **sed options + sed script + file
    * **Five Examples:**
      * sed 's/apples/bananas/' fruit-list.lst , Replacing a string in a givin file.
      * sed 's/apples/bananas/4' fruit-list.lst , replacing the number of occurrences of a patteren in a file.
      * sed '3 s/apples/bananas/' fruit-list.lst , replacing string on a specific line number.
      * sed '5d' fruit-list.lst , is to delete a particular line (line 5).
      * sed G fruit-list.lst , is to insert one black lind after each line.








   
