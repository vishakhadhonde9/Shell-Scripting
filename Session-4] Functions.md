# Function-
- A function is a collection of statements or block of resuable code that execute a specified task.

### Syntax-
    function functionName () {  
        # Commands to be executed  
    }  

## Calling function-
        functionName arguments
## Arguments-
- Shell functions can accept arguments just like command-line scripts.
- You access these arguments using special variables: $1 for the first argument, $2 for the second, and so on.
- To access all the arguments, you use $@ or $*.

## Example-
     1]
        #!/bin/sh

        # Define your function here
        Hello () {
           echo "Hello World"
        }
        
        # Invoke your function
        Hello


     2]   
         #!/bin/bash
         # Define a function with parameters
         greet() {
             echo "Hello, $1!"
             echo "You are $2 years old."
         }
    
         # Call the function with two arguments
         greet "Alice" 25

    3] 
        #!/bin/bash
    
        # Define the function that takes two arguments
        add_numbers() {
            sum=$(( $1 + $2 ))
            echo "Sum: $sum"
        }
        
        # Call the function with two arguments
        add_numbers 5 10
