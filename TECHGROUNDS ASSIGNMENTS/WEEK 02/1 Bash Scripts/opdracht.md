# [1 Bash Scripts]

[Geef een korte beschrijving van het onderwerp]

## Key-terms

- Scripts

- PATH vaiable

- $VARIABLENAME

- 

## Opdracht

<u>Exercise 1:</u>

- Create a directory called ‘scripts’. Place all the scripts you make in this directory.
- Add the scripts directory to the PATH variable.
- Create a script that appends a line of text to a text file whenever it is executed.
- Create a script that installs the httpd package, activates httpd, and enables httpd. Finally, your script should print the status of httpd in the terminal.

<u>Exercise 2:</u>

- Create a script that generates a random number between 1 and 10, stores it in a variable, and then appends the number to a text file.

<u>Exercise 3:</u>

- Create a script that generates a random number between 1 and 10, stores it in a variable, and then appends the number to a text file only if the number is bigger than 5. If the number is 5 or smaller, it should append a line of text saying "the number is 5 or smaller" to that text file instead.

### Gebruikte bronnen

- https://www.howtogeek.com/658904/how-to-add-a-directory-to-your-path-in-linux/

- https://www.theserverside.com/blog/Coffee-Talk-Java-News-Stories-and-Opinions/run-Unix-shell-script-Linux-Ubuntu-command-chmod-777-permission-steps

### Ervaren problemen

When I tried to use Gedit , I encountered this eror message:
(gedit:1430): Gtk-WARNING **: cannot open display: $ sudo gedit

solution :

https://askubuntu.com/questions/930425/gedit1430-gtk-warning-cannot-open-display

```
sudo apt -y install gnome
```

### Resultaat

<u>Exercise 1:</u>

- Create a directory called ‘scripts’. Place all the scripts you make in this directory.
  
  ```
  mkdir scripts
  ```

- Add the scripts directory to the PATH variable.
  
  ```
  export PATH=/scripts:$PATH
  ```

- Create a script that appends a line of text to a text file whenever it is executed.
  
  ```
  $ mkdir scripts
  $ cd scripts
  $ touch appendtxt.sh
  $ chmod 777 appendtxt.sh
  $ echo 'echo hello-techgrounds' >> appendtxt.sh
  $ /scripts/appendtext.sh
  hello-techgrounds
  ```

- Create a script that installs the httpd package, activates httpd, and enables httpd. Finally, your script should print the status of httpd in the terminal.

<u>Exercise 2:</u>

- Create a script that generates a random number between 1 and 10, stores it in a variable, and then appends the number to a text file.

<u>Exercise 3:</u>

- Create a script that generates a random number between 1 and 10, stores it in a variable, and then appends the number to a text file only if the number is bigger than 5. If the number is 5 or smaller, it should append a line of text saying "the number is 5 or smaller" to that text file instead.
