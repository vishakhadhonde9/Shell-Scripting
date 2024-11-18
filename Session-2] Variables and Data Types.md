# Variables -
- Variables are used to store data.
- Variables are used to store data that can be referenced and manipulated throughout the script.
- **Variable Declearation:**
  - variable_name=value
    - myvar="Hello"
    - my_number=42
    - my_array=("apple" "banana" "cherry")
- Make sure there are no spaces around the = sign.
- **Accessing Variables -**
  -  Use the dollar sign ($) before the variable name to access its value.
  -  To check and print variable value
    - echo $variable_name
### Rules for variable declearation -
- We should not use special symbols in variables (like @#$% etc)
- The variable name should start with the alphabet only and the variable should not start with a Number/digit (like 1a,2c etc).
- It is recommended to use UPPERCASE characters.

# Read-only Variables -
- Shell provides a way to mark variables as read-only by using the read-only command.
- After a variable is marked read-only, its value cannot be changed.
- For example, the following script generates an error while trying to change the value of NAME −

   - #!/bin/sh
   - NAME="Zara Ali"
   - readonly NAME
   - NAME="Qadiri"

# Data Types-
- Shell scripting doesn't have strict data types like other programming languages.
- Variables are treated as strings by default.

# String Manipulation -
- String is set of charachters, words, integers and numbers in single unit.
- String is defined in " ".
- String manipulation in shell scripting involves various operations on strings, such as concatenation, substring extraction, searching, and replacing.
####  Concatenation - Concatenation involves combining two or more strings to create a new string. 
    #!/bin/bash
    string1="Hello, "
    string2="World!"
    result=$string1$string2
    echo "Concatenated string: $result"

####  Substring Extraction: You can extract a portion of a string using substrings. 
     #!/bin/bash
     string="Hello, World!"
     substring=${string:7:5} # Starting from index 7, extract 5 characters
     echo "Substring: $substring"
  
#### Searching and Replacing: Searching involves finding a specific substring within a string, and replacing involves substituting one substring with another.
     #!/bin/bash
     string="Hello, World! Hello!"
     search="Hello"
     replace="Hi"
     result=${string//$search/$replace} # Replace all occurrences
     echo "Original string: $string"
     echo "Result after replacement: $result"

# Array -
- Array is data type that stores a collection of elements of the same type in contiguous memory locations.

## 3. Array Manipulation - 
- You can modify arrays by adding, removing, and updating elements.
#### Example -
     #!/bin/bash
     fruits=("Apple" "Banana" "Orange")
     
     # Adding an element
     fruits+=("Grapes")
     
     # Updating an element
     fruits[1]="Mango"
    
     # Removing an element
     unset fruits[0]
    
     # Display the modified array
     echo "Modified array:"
     for fruit in "${fruits[@]}"; do
       echo "Fruit: $fruit"
     done
    
     
# Example-

    #!/bin/bash
    
    # Declare variables
    greeting="Hello"
    name="Alice"
    number=5
    fruits=("apple" "banana" "cherry")
    
    # Access and print variables
    echo "$greeting, $name!"  # Outputs: Hello, Alice!
    echo "Number: $number"     # Outputs: Number: 5
    
    # Accessing array elements
    echo "First fruit: ${fruits[0]}"  # Outputs: First fruit: apple
    echo "All fruits: ${fruits[@]}"     # Outputs: All fruits: apple banana cherry
