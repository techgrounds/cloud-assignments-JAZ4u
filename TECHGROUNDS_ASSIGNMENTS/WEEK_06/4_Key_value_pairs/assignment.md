# [4/ Key-value pairs]

Key-value pairs are a general concept you will definitely encounter. Some examples of where you will find them are NoSQL databases or AWS/Azure resource tags. Dictionaries (dict) in Python also use key-value pairs to store information. Dicts in Python are written using curly brackets {}. You can get values from the dict by calling its key.

## Key-terms

[Schrijf hier een lijst met belangrijke termen met eventueel een korte uitleg.]

## Assignment

Exercise 1:

- Create a new script.
- Create a dictionary with the following keys and values:

| **Key**    | **Value**      |
| ---------- | -------------- |
| First name | Casper         |
| Last name  | Velzen         |
| Job title  | Learning coach |
| Company    | Techgrounds    |

- Loop over the dictionary and print every key-value pair in the terminal.

 Exercise 2:

- Create a new script.
- Use user input to ask for their information (first name, last name, job title, company). Store the information in a dictionary.
- Write the information to a csv file (comma-separated values). The data should not be overwritten when you run the script multiple times.

### Used sources

[Plaats hier de bronnen die je hebt gebruikt.]

### Encountered problems

[Geef een korte beschrijving van de problemen waar je tegenaan bent gelopen met je gevonden oplossing.]

### Result

Exercise 1:

- Create a new script.
- Create a dictionary with the following keys and values:

| **Key**    | **Value**      |
| ---------- | -------------- |
| First name | Casper         |
| Last name  | Velzen         |
| Job title  | Learning coach |
| Company    | Techgrounds    |

- Loop over the dictionary and print every key-value pair in the terminal.
  
  ```
  # Create a dictionary with the specified keys and values
  person_info = {
      "First name": "Casper",
      "Last name": "Velzen",
      "Job title": "Learning coach",
      "Company": "Techgrounds"
  }
  
  # Loop over the dictionary and print every key-value pair
  for key, value in person_info.items():
      print(key + ":", value)
  
  ```
  
  

 Exercise 2:

- Create a new script.
- Use user input to ask for their information (first name, last name, job title, company). Store the information in a dictionary.
- Write the information to a csv file (comma-separated values). The data should not be overwritten when you run the script multiple times.

```

```