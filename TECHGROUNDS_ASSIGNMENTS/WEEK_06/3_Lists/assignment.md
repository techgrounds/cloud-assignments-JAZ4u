# [3/ Lists]

You can declare a list of values in a single variable. A list is represented by square brackets [ ], and each value is separated by a comma.

Each position in a list has a number associated with it called the index. Indexes start at 0, so the first item in a list will have the index 0. The second item will have index 1, etc. You can call individual items in a list by calling its index.

You can loop over a list using a for loop. Instead of a number within a range, *i* (or whatever you name the variable you declare) will have the value of an item in the list. You can still use range() to loop over a list. In this case, *i* will be used to call an index in a list.

## Key-terms

[Schrijf hier een lijst met belangrijke termen met eventueel een korte uitleg.]

## Assignment

Exercise 1:

- Create a new script.
- Create a variable that contains a list of five names.
- Loop over the list using a for loop. Print every individual name in the list on a new line.  
  Example output:

![](https://lwfiles.mycourse.app/642fed69f84f1f76d03f116a-public/ebook/ae3ea63690cd68e7b44908417984166f/image4.png)

 Exercise 2:

- Create a new script.

- Create a list of five integers.

- Use a for loop to do the following for every item in the list:

- Print the value of that item added to the value of the next item in the list.

- If it is the last item, add it to the value of the first item instead (since there is no next item).  
  Example output:

![](https://lwfiles.mycourse.app/642fed69f84f1f76d03f116a-public/ebook/ae3ea63690cd68e7b44908417984166f/image3.png)

The first result above is created by adding 9 and 80. The second result is created by adding 80 and 16, etc. The last result is created by adding 35 and 9.

### Used sources

[Plaats hier de bronnen die je hebt gebruikt.]

### Encountered problems

[Geef een korte beschrijving van de problemen waar je tegenaan bent gelopen met je gevonden oplossing.]

### Result

Exercise 1:

- Create a new script.
- Create a variable that contains a list of five names.
- Loop over the list using a for loop. Print every individual name in the list on a new line.  
  Example output:

![](https://lwfiles.mycourse.app/642fed69f84f1f76d03f116a-public/ebook/ae3ea63690cd68e7b44908417984166f/image4.png)

```
# Create a list of five names
names = ["Jaz", "Elmarie", "Shay", "Sam", "Shikha"]

# Loop over the list using a for loop
for name in names:
    # Print every individual name in the list on a new line
    print(name)
```

![list_names.png](C:\Users\Administrator\OneDrive\Documenten\TechGrounds\Clone\cloud-assignments-JAZ4u\TECHGROUNDS_ASSIGNMENTS\WEEK_06\3_Lists\list_names.png)

 Exercise 2:

- Create a new script.

- Create a list of five integers.

- Use a for loop to do the following for every item in the list:

- Print the value of that item added to the value of the next item in the list.

- If it is the last item, add it to the value of the first item instead (since there is no next item).  
  Example output:

![](https://lwfiles.mycourse.app/642fed69f84f1f76d03f116a-public/ebook/ae3ea63690cd68e7b44908417984166f/image3.png)

The first result above is created by adding 9 and 80. The second result is created by adding 80 and 16, etc. The last result is created by adding 35 and 9.

Result of excercise 2:

- We create a list of five integers named `numbers`.
- We use a for loop to iterate over the indices of the list using `range(len(numbers))`.
- For each index `i`, we calculate the index of the next item in the list using `(i + 1) % len(numbers)`. This ensures that when we reach the last item in the list, it wraps around to the first item.
- We print the sum of the current item and the next item using `numbers[i] + numbers[next_index]`.

```
# Create a list of five integers
numbers = [10, 20, 30, 40, 50]

# Use a for loop to iterate over the list
for i in range(len(numbers)):
    # Calculate the index of the next item in the list
    next_index = (i + 1) % len(numbers)

    # Print the value of the current item added to the value of the next item
    print(numbers[i] + numbers[next_index])
```

![list_5int.png](C:\Users\Administrator\OneDrive\Documenten\TechGrounds\Clone\cloud-assignments-JAZ4u\TECHGROUNDS_ASSIGNMENTS\WEEK_06\3_Lists\list_5int.png)