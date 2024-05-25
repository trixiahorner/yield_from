# Python '*yield from*' Statement: Iterating Through Nested Lists

## Introduction
This repository demonstrates how to use the '*yield from*' statement in Python to iterate through a nested list. 
<br>
<br>
Using the '*yield from*' statement to iterate through a nested list is a powerful and elegant way to flatten the structure and yield elements from sublists as if they were part of a single list.

## Explanation
The yield from statement is used to delegate the yielding process to another generator or iterable. 
In this example, yield from sublist iterates through each sublist within the nested_list, yielding each item one by one.
```
def iterate_nested_lists(nested_list):
    for sublist in nested_list:
        yield from sublist

nested_list = [
    [1, 2, 3],
    [4, 5, 6],
    [7, 8, 9]
]

for value in iterate_nested_lists(nested_list):
    print(value)
```

## Example Code
```
def iterate_Hamilton_list(Hamilton):
  for sublist in Hamilton:
    yield from sublist

#nested list
Hamilton = [["Hamilton", "Burr"], 
            ["Washington", "Jefferson", "Lafayette", "King George"],
            ["Angelica", "Eliza", "Peggy", "Mariah"],
            ["Philip", "Madison"]]

#iterate through nested list and print element of each sublist
for character in iterate_Hamilton_list(Hamilton):
  print(character)
```

## Output
The above code will produce the following output:
```
Hamilton
Burr
Washington
Jefferson
Lafayette
King George
Angelica
Eliza
Peggy
Mariah
Philip
Madison
```

## Advantages
- Readability: Simplifies nested iterations, making the code more readable.
- Conciseness: Reduces the amount of code required for nested loops.
- Efficiency: Streamlines the process of iterating through complex data structures.

<br>
<br>

![code](https://github.com/trixiahorner/yield_from/blob/main/images/hamilton.png?raw=true)



