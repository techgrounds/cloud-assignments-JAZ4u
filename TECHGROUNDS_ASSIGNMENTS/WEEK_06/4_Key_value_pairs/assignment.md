# [4/ Key-value pairs]

Key-value pairs are a general concept you will definitely encounter. Some examples of where you will find them are NoSQL databases or AWS/Azure resource tags. Dictionaries (dict) in Python also use key-value pairs to store information. Dicts in Python are written using curly brackets {}. You can get values from the dict by calling its key.

## Key-terms

- NoSQL

- Dictionaries (dict)

- Python : curly brackets {}

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
  
  Result of excercise 1:
  
  This script will output each key-value pair in the `person_info` dictionary in the terminal.

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

  ![key_value_pairs.png](key_value_pairs.png)

 Exercise 2:

- Create a new script.

- Use user input to ask for their information (first name, last name, job title, company). Store the information in a dictionary.

- Write the information to a csv file (comma-separated values). The data should not be overwritten when you run the script multiple times.
  
  Result of Excercise 2:
  
  This script first defines two functions: `get_user_info()` to collect user information and `write_to_csv()` to append this information to a CSV file. The `main()` function orchestrates these actions. Each time you run the script, it prompts the user for their information, appends it to the CSV file, and prints a confirmation message. The CSV file is created if it doesn't exist, and subsequent runs of the script will append new entries without overwriting existing data.

```
import csv
import os

# Function to get user information
def get_user_info():
    first_name = input("Enter your first name: ")
    last_name = input("Enter your last name: ")
    job_title = input("Enter your job title: ")
    company = input("Enter your company: ")
    return {
        "First name": first_name,
        "Last name": last_name,
        "Job title": job_title,
        "Company": company
    }

# Function to write user information to CSV file
def write_to_csv(data):
    file_exists = os.path.isfile("user_info.csv")
    with open("user_info.csv", mode='a', newline='') as file:
        fieldnames = ["First name", "Last name", "Job title", "Company"]
        writer = csv.DictWriter(file, fieldnames=fieldnames)
        if not file_exists:
            writer.writeheader()  # Write header only if the file is created for the first time
        writer.writerow(data)

# Main function
def main():
    user_info = get_user_info()
    write_to_csv(user_info)
    print("User information has been saved to user_info.csv.")

if __name__ == "__main__":
    main()
```

![user_inf_csv.png](user_inf_csv.png)