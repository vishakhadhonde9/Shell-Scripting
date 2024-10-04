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

# Data Types-
- Shell scripting doesn't have strict data types like other programming languages.
- Variables are treated as strings by default.

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
