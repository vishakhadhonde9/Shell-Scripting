# Conditional Statements -
- A conditional statement in shell scripting allows your script to make decisions based on certain conditions.
- It checks whether a condition is true or false and then executes specific commands accordingly.
# if, elif and else-
- if: Checks the first condition.
- elif: Checks an additional condition if the previous one was false.
- else: Executes if all previous conditions are false.
#### syntax:
      if {condition}
      then
        {execute this}
      else
        {execute this}
      fi

# Looping -
- Looping structures help you repeat a set of commands multiple times.
- There are several types of loops in Shell Script:
    - for loop
    - while loop
    - until loop
    - select loop

# 1] for loop -
- A for loop allows you to iterate over a list of items or a range of numbers.
### Syntax -
          for variable in item1 item2 item3 ... 
          do
              # commands to execute
          done
 ### Examples:
      1] for fruit in apple banana orange
         do
             echo "I like $fruit"
         done

      2] for i in {1..5}
         do
             echo "Number: $i"
         done

     3] for i in $(seq 1 5)
        do
            echo "Number: $i"
        done

# 2] while loop -
-  while loop is used to execute a block of code repeatedly as long as a given condition is true.
-  The condition is checked before each iteration, and if it evaluates to true, the loop continues; if it evaluates to false, the loop terminates.

### Syntax - 
     while [ condition ]
     do
         # commands to execute
     done

#### Examples:
     1] i=1
        while [ $i -le 5 ]
        do
            echo "Number $i"
            ((i++))  # Increment i by 1
       done
     2] #!/bin/bash
        echo "Please enter a number between 1 and 10:"
        read num
        while [ $num -lt 1 ] || [ $num -gt 10 ]; do
            echo "Invalid input. Please enter a number between 1 and 10:"
            read num
        done
        echo "You entered a valid number: $num"
 
 # Conditions -
- -lt (less than)
- -le (less than or equal to)
- -gt (greater than)
- -ge (greater than or equal to)
- -eq (equal to)
- -ne (not equal to)
- -z (string is empty)
- -n (string is not empty)

# until loop -
- The until loop in shell scripting is similar to the while loop but loop runs as long as the condition is false, and it stops when the condition becomes true.

### Syntax-
      until [ condition ]
      do
          # commands to be executed
      done

#### Examples -
      i=1
      until [ $i -gt 5 ]
      do
         echo "Number $i"
         ((i++))  # Increment i by 1
     done 

# select loop -
-  select loop provides a simple way to present a menu to the user and let them choose an option.
-  It is often used in interactive scripts where you want the user to select an option from a list.

### Syntax -
     select var in option1 option2 option3 ... 
     do
         # commands to be executed based on the selected option
     done

#### Examples -
      
