# [5- Working with text (CLI)]

[Geef een korte beschrijving van het onderwerp]

## Key-terms

[Schrijf hier een lijst met belangrijke termen met eventueel een korte uitleg.]

## Opdracht

Exercise:

- Find out your current working directory.
- Make a listing of all files and directories in your home directory.
- Within your home directory, create a new directory named ‘techgrounds’.
- Within the techgrounds directory, create a file containing some text.
- Move around your directory tree using both absolute and relative paths.

### Gebruikte bronnen

- https://www.youtube.com/watch?v=iSKncMygQDs 
  How to use grep command to find a file in Linux | Linux in a Minute
  
  `grep -RI Techgrounds ~/`  ( does a recursive search in HOME folder for the word Techgrounds in non binary files )

- [linux - How to redirect output to a file and stdout - Stack Overflow](https://stackoverflow.com/questions/418896/how-to-redirect-output-to-a-file-and-stdout)

### Ervaren problemen

[Geef een korte beschrijving van de problemen waar je tegenaan bent gelopen met je gevonden oplossing.]

### Resultaat

Exercise:

- Find out your current working directory.
  `pwd`
- Make a listing of all files and directories in your home directory.
  `l ~/`
- Within your home directory, create a new directory named ‘techgrounds’.
  `sudo mkdir techgrounds`
- Within the techgrounds directory, create a file containing some text.
  1/ `sudo touch text.txt` 
  2/ `echo "Techgrounds is knowledge 2024" >> text.txt`
- Move around your directory tree using both absolute and relative paths.
