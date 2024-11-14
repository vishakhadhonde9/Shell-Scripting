# SHELL SCRIPTING -
- In Linux, a shell is a command-line interface that allows users to interact with the operating system and execute various commands.
- It's both a user interface and a scripting language that provides a way to communicate with the computer system through textual commands.
- The shell is a type of program called an interpreter.

### TYPES OF SHELL -
- BASH
- PYTHON
- SH
- ZSH

# Shebang -
- The shebang (#!) is a special sequence of characters at the beginning of a script file that tells the operating system which interpreter should be used to execute the script.
- It's followed by the path to the interpreter binary.
- This is particularly useful for shell scripts to ensure they're executed by the correct shell, even if the user's default shell is different.
- For example, in a Bash shell script, the shebang line would be:
    - #!/bin/bash
- Let's break down this example:
    - **#!:** This is the shebang sequence that indicates the start of the shebang line.
    - **/bin/bash:** This is the path to the Bash interpreter binary. It tells the system to use the Bash interpreter to execute the script.

# How to Execute Script -
- **Step 1: Create a Shell Script**
    - Open a Text Editor: You can use any text editor like vim, nano.
        - vim my_script.sh
    - Add the Shebang Line: This line indicates which interpreter to use.
        - #!/bin/bash
    - Write Your Script: Below the shebang line, you can write your script.
        - #!/bin/bash
        - echo "Hello, World!"
- **Step 2: Make the Script Executable**
    - Before you can run your script, you need to make it executable by assigning execute permission.
        - chmod a+x my_script.sh
        - chmod 755 my_script.sh
- **Step 3: Execute the Script**
    - ./my_script.sh or
    - bash my_script.sh

 
   
