# [1 Bash Scripts]

Bash scripts are scripts written in the Bash (Bourne Again Shell) programming language. 

Bash is a Unix shell and command language, and it is the default shell on most Linux and macOS systems. Bash scripts are used to automate tasks, execute commands, and perform various operations on Unix-like systems.

Here are some key features and characteristics of Bash scripts:

1 Text-based: Bash scripts are essentially text files containing a series of commands and instructions that are interpreted and executed by the Bash shell.

2 Scripting language: Bash provides various programming constructs such as variables, conditionals, loops, functions, and error handling, making it suitable for writing scripts to automate tasks.

3 Interpreted: Bash scripts are interpreted rather than compiled. When you run a Bash script, the commands are executed directly by the Bash interpreter line by line.

4 Shell environment: Bash scripts have access to the shell environment, including environment variables, standard input/output, and file system operations.

5 Extensible: Bash scripts can invoke external commands and utilities, allowing you to leverage the vast array of command-line tools available on Unix-like systems.

6 Portability: Bash scripts written for one Unix-like system can often be run on other Unix-like systems with minimal or no modifications, as long as they don't rely on system-specific features.]

## Key-terms

- Scripts
  
  Scripts, in the context of computing, are files containing sequences of commands or instructions written in a specific programming or scripting language. These files are used to automate tasks, execute commands, or perform specific operations on a computer system.
  
  

- PATH variable
  
  The `PATH` variable is an environment variable used by the operating system to specify a set of directories where executable programs are located. When you enter a command in the terminal, the shell searches through these directories to find the executable corresponding to that command.

- $VARIABLENAME
  
  In Unix-like operating systems, including Ubuntu, the `$VARIABLENAME` syntax represents the value of the environment variable named `VARIABLENAME`. Environment variables are dynamic named values that can affect the behavior of processes and programs running in the system.

- Bash
  
  In the context of Ubuntu and other Unix-like operating systems, "Bash" refers to the Bourne Again Shell. It's a command processor that typically runs in a text window where the user types commands that cause actions. Bash can also read commands from a file, called a script. Like other Unix shells, it supports filename wildcarding, piping, here documents, command substitution, variables, and control structures for condition-testing and iteration.

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

- [How to create and run a shell script in Linux and Ubuntu](https://www.theserverside.com/blog/Coffee-Talk-Java-News-Stories-and-Opinions/run-Unix-shell-script-Linux-Ubuntu-command-chmod-777-permission-steps)

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

-

```
 $ touch install_httpd.sh
 $ chmod 777 install_httpd.sh
```

```
**text inside install_httpd.sh **

#!/bin/bash

# Install the httpd package

sudo apt-get update
sudo apt-get install -y apache2

# Start and enable httpd

sudo systemctl start apache2
sudo systemctl enable apache2

# Print the status of httpd

sudo systemctl status apache2
```

```
**To execute my script:**

$ /scripts/appendtext.sh
 hello-techgrounds
```

![httpd_install.sh script1.png](C:\Users\Administrator\OneDrive\Documenten\TechGrounds\Clone\cloud-assignments-JAZ4u\00_includes\WEEK%2002%20-%20screenshots\1%20Bash%20Scripts\httpd_install.sh%20script1.png)

![httpd_install.sh script2.png](C:\Users\Administrator\OneDrive\Documenten\TechGrounds\Clone\cloud-assignments-JAZ4u\00_includes\WEEK%2002%20-%20screenshots\1%20Bash%20Scripts\httpd_install.sh%20script2.png)

<u>Exercise 2:</u>

- Create a script that generates a random number between 1 and 10, stores it in a variable, and then appends the number to a text file.

```
  $ touch generate_random_number.sh
  $ chmod 777 generate_random_number.sh


**text inside generate_random_number.sh**
#!/bin/bash

# Generate a random number between 1 and 10

random_number=$((RANDOM % 10 + 1))

# Append the random number to a text file

echo "$random_number" >> random_numbers.txt

echo "Random number $random_number appended to random_numbers.txt."
```

Then you can execute the script:

```
./generate_random_number.sh
```

![generate_random_number.sh.png](C:\Users\Administrator\OneDrive\Documenten\TechGrounds\Clone\cloud-assignments-JAZ4u\00_includes\WEEK%2002%20-%20screenshots\1%20Bash%20Scripts\generate_random_number.sh.png)

<u>Exercise 3:</u>

- Create a script that generates a random number between 1 and 10, stores it in a variable, and then appends the number to a text file only if the number is bigger than 5. If the number is 5 or smaller, it should append a line of text saying "the number is 5 or smaller" to that text file instead.
  
  ```
  
  ```

```

```

![generate_random_number seperate at 5.png](C:\Users\Administrator\OneDrive\Documenten\TechGrounds\Clone\cloud-assignments-JAZ4u\00_includes\WEEK%2002%20-%20screenshots\1%20Bash%20Scripts\generate_random_number%20seperate%20at%205.png)
