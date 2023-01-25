![image](https://user-images.githubusercontent.com/105258746/188752518-2606bf0a-0726-4c8a-8843-eb06d121d9cd.png)

# SHELL, init files, variables and expansions PROJECTS

## TASKS

### Note: When doing this project, After using text editor of your choice to create and access the file on insert mode.Ensure the first line is always having `#!/bin/bash`, then the second line is having the correct command/answer.
(From your terminal, convert the file created to `SCRIPT` i.e: chmod u+x filename)

### File: 0-alias is a script that creates an alias.

- input: `alias ls="rm *"`

### File: 1-hello_you is a script that prints hello user, where user is the current Linux user.

- input: `echo "hello $USER"`

### File: 2-path is a script that adds /action to the PATH.

- input: `PATH=$PATH:/action`

### File: 3-paths is a script that counts the number of directories in the PATH.

- input: `echo $PATH | tr ':' '\n' | wc -l`

### File: 4-global_variables is a script that lists environment variables.

- input: `printenv`

### File: 5-local_variables is a script that lists all local variables and environment variables, and functions.

- input: `set`

### File: 6-create_local_variable is a script that creates a new local variable.

- input: `BEST="School"`

### File: 7-create_global_variable is a script that creates a new global variable.

- input: `export BEST="School"`

### File: 8-true_knowledge is a script that prints the result of the addition of 128 with the value stored in the environment variable TRUEKNOWLEDGE, followed by a new line.

- input: `echo $((128 + $TRUEKNOWLEDGE))`

### File: 9-divide_and_rule is a script that prints the result of POWER divided by DIVIDE, followed by a new line.

- input: `echo $((POWER/DIVIDE))`

### File: 10-love_exponent_breath is a script that displays the result of BREATH to the power LOVE.

- input: `echo $((BREATH**LOVE))`

### File: 11-binary_to_decimal` is a script that converts a number from base 2 to base 10.

- input: `echo $((2#$BINARY))`

### File: 12-combinations is a script that prints all possible combinations of two letters, except oo.

- input: `echo {a..z}{a..z} | tr ' ' '\n' | grep -v "oo"`

### File: 13-print_float is a script that prints a number with two decimal places.

- input: `printf '%.2f\n' $NUM`

### File: 100-decimal_to_hexadecimal is a script that converts a number from base 10 to base 16.

- input: `printf '%x\n' $DECIMAL`

### File: 101-rot13 is a script that encodes and decodes text using the rot13 encryption.

- input: `tr 'A-Za-z' 'N-ZA-Mn-za-m'`

### File: 102-odd is a script that prints every other line from the input, starting with the first line.

- input: `paste -d, - - | cut -d, -f1`

### File: 103-water_and_stir is a shell script that adds the two numbers stored in the environment variables WATER and STIR and prints the result.

- input: `printf "%o\n" $(( $((5#$(echo $WATER | tr water 01234))) + $((5#$(echo $STIR | tr stir. 01234))) )) | tr 01234567 bestchol`
