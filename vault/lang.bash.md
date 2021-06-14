---
id: 140f486f-2ad7-42c3-bc52-d051f14715ac
title: Bash
desc: ''
updated: 1621439845973
created: 1621434195573
---

Cheat Sheet ref: https://gist.github.com/bradtraversy/ac3b1136fc7d739a788ad1e42a78b610

----

Bash script file extension: `.sh`.

Make file executable: `chmod +x file.sh`

Run file: `./file.sh`

Where is bash: `which bash`

Put bash location at top of file: `#! /bin/bash`

####  ECHO COMMAND
```bash
echo Hello World!
```

#### VARIABLES
Uppercase by convention
Letters, numbers, underscores
```bash
NAME="Jon"
echo "My name is $NAME"
# or
echo "My name is ${NAME}"
```

#### USER INPUT
```bash
NAME="Jon"
read -p "Enter your name: " NAME
echo "Hello $NAME, nice to meet you!"
```

 #### SIMPLE IF STATEMENT
```bash
NAME="Jon"
if [ "$NAME" == "Jon" ]
then
    echo "Your name is $Jon"
fi
```

#### IF-ELSE
```bash
NAME="Jack"
if [ "$NAME" == "Jon" ]
then
    echo "Your name is Jon"
else
    echo "Your name is not Jon"
fi
```

#### ELSE-IF (elif)
```bash
NAME="Jack"
if [ "$NAME" == "Jon" ]
then
    echo "Your name is Jon"
elif [ "$NAME" == "Jack" ]
then
    echo "Your name is Jack"
else
    echo "Your name is not Jon or Jack"
fi
```

#### COMPARISON
`FOO -eq BAR` returns true if the values are equal
`FOO -ne BAR` returns true if the values not equal
`FOO -gt BAR` returns true if `FOO` is greater than `BAR`
`FOO -ge BAR` returns true if `FOO` is greater than or equal to `BAR`
`FOO -lt BAR` returns true if `FOO` is less than `BAR`
`FOO -le BAR` returns true if `FOO` is less than or equal to `BAR`
```bash
FOO=1
BAR=2
if [ "$FOO" == "$BAR" ]
then
    echo "$FOO is greater than $BAR"
else
    echo "$FOO is less than $BAR"
fi
```

#### FILE CONDITIONS
`-d` file   True if the file is a directory
`-e` file   True if the file exists (note that this is not particularly portable, thus `-f` is generally used)
`-f` file   True if the provided string is a file
`-g` file   True if the group id is set on a file
`-r` file   True if the file is readable
`-s` file   True if the file has a non-zero size
`-u`    True if the user id is set on a file
`-w`    True if the file is writable
`-x`    True if the file is an executable
```bash
FILE="test.txt"
if [ -e "$FILE" ]
then
  echo "$FILE exists"
else
  echo "$FILE does NOT exist"
fi
```