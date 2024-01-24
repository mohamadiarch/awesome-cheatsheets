---
source: https://github.com/RehanSaeed/Bash-Cheat-Sheet
---


## Bash Script


## Run
```bash
.sh or .txt        # you can run bash file with .sh or .txt or any other extension
bash ./script.sh    # run with bash
./script.sh        # run with default bash
#!/bin/bash        # Hashbang or Shebang: write this line at the top of your script for default runner (ex: python,sh, bash)
ls -l script.sh    # execute permission
./script.sh "first"       # echo $1 for capture first argument ==> $0 means file name
```

### Variables

```bash
#!/bin/bash
foo=123                # Initialize variable foo with 123
name = "John"     # It's wrong, do not use space before and after = 
name="John Doe"        # use "" for space inside string
declare -i foo=123     # Initialize an integer foo with 123
declare -r foo=123     # Initialize readonly variable foo with 123
echo ali               # Print ali as a string. its better to use string
echo $foo               # Print "foo hi" ==> if variable is not set it will print empty
echo ${foo}             #  Print "foohi"
echo ${foo:-default} # Print variable foo if it exists otherwise print default (you can use single or double qoute too)
echo ${foo:=default}   # Print variable foo if it exists otherwise print default (you can use single or double qoute too)
echo "$HOME"           # Print $HOME as variable ==> double qoutation pasres the variable 
echo '$HOME'           # Print $HOME as string  ==> single qoutation pasres pure string
echo $(date)           # Print date as a output of command
x=$(expr $end - $start)  # Calculate the difference between two numbers
x=(($end - $start))
export foo             # Make foo available to child processes
unset foo              # Make foo unavailable to child processes
```

### Environment Variables

```bash
#!/bin/bash

env            # List all environment variables
echo $PATH     # Print PATH environment variable
$?
$#              #number of arguments from command line
export FOO=Bar # Set an environment variable
```

### Functions

```bash
#!/bin/bash

greet() {
  local world = "World"
  echo "$1 $world"
  return "$1 $world"
}
greet "Hello"
greeting=$(greet "Hello")
```

### Exit Codes

```bash
#!/bin/bash

exit 0   # Exit the script successfully like return 0 in cpp
exit 1   # Exit the script unsuccessfully
echo $?  # Print the last exit code
```

### Conditional Statements

#### Boolean Operators

- `$foo` - Is true
- `!$foo` - Is false

#### Numeric Operators

- `-eq` - Equals
- `-ne` - Not equals
- `-gt` - Greater than
- `-ge` - Greater than or equal to
- `-lt` - Less than
- `-le` - Less than or equal to
- `-e` foo.txt - Check file exists
- `-z` foo - Check if variable exists

#### String Operators

- `=` - Equals
- `==` - Equals
- `-z` - Is null
- `-n` - Is not null
- `<` - Is less than in ASCII alphabetical order
- `>` - Is greater than in ASCII alphabetical order

#### If Statements

```bash
#!/bin/bash
test a -nt b                                           # you can use test as a []
if [-f $file -a -r $file]                             # check $file is file and(-a) readable

if [[$foo = 'bar']]; then
  echo 'one'
elif [[$foo = 'bar']] || [[$foo = 'baz']]; then
  echo 'two'
elif [[$foo = 'ban']] && [[$USER = 'bat']]; then
  echo 'three'
else
  echo 'four'
fi
```

#### Inline If Statements

```bash
#!/bin/bash

[[ $USER = 'rehan' ]] && echo 'yes' || echo 'no'
```

#### While Loops

```bash
#!/bin/bash

declare -i counter
counter=10
while [$counter -gt 2]; do
  echo The counter is $counter
  counter=counter-1
done
```

#### For Loops

```bash
seq 1 10                               # Print 1 2 3 4 5 6 7 8 9 10
for i in {1..10}; do echo $i; done    # Print 1 2 3 4 5 6 7 8 9 10
for i in $(seq 1 10); do echo $i; done    # Print 1 2 3 4 5 6 7 8 9 10

for i in {0..10..2}
  do
    echo "Index: $i"
  done

for filename in file1 file2 file3
  do
    echo "Content: " >> $filename
  done

for filename in *;
  do
    echo "Content: " >> $filename
  done
```

#### async
```bash
sleep 10      # wait 10 secinds
```

#### Case Statements

```bash
#!/bin/bash

echo "What's the weather like tomorrow?"
read weather

case $weather in
  sunny | warm ) echo "Nice weather: " $weather
  ;;
  cloudy | cool ) echo "Not bad weather: " $weather
  ;;
  rainy | cold ) echo "Terrible weather: " $weather
  ;;
  * ) echo "Don't understand"
  ;;
esac
```

