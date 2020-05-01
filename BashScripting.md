## Terminology
**Shell scripting**: commands written for the shell to execute<br>
**Shell script**: A file or program that shell will execute<br>
**Sh (Bourne Shell)**: A shell interpreter<br>
**Bash (Bourne Again Shell)**: The improved version of Sh<br>

## How it works
Let's take an example.<br>
One common command people used is `touch` for creating a file. `touch` is a binary executable file located inside `/bin` directory of the system.<br>

After executing the `touch` command, the shell interpreter will checks for an alias present in `.bash_profile` in home directory. If alias is not present, then it looks for a binary executable file in the `PATH`.<br>

We are allowed to execute multiple Bash commands saved in a file and execute them at once with bash function. <br>
....<br>
<br>
<br>
Simple example <br>
`$ touch hello` <br>

make it executable <br> 
`$ chmod 774 hello` <br>

Open editor, add the following line <br>
`echo "Hello World!"` <br>

Save it and run in the script by typing <br>
`$ ./hello` <br>

In order to make sure that the script will run using the Bash shell, we need to use shebang line. <br>
Shebang is the geeky way to describe the `#!` characters that explicitly specify which shell to use when running script. <br>
Adding shebang line as the first line of the script: <br>
`#!/usr/bin/bash` <br>
`echo "Hello World!"` <br>
<br>
Run the `hello` script once more 
<br>
<br>
<br>
<br>
<br>
<br>
A sysadmin's guide to Bash scripting, by opensource.com
https://itnext.io/bash-scripting-everything-you-need-to-know-about-bash-shell-programming-cd08595f2fba <br>
https://devhints.io/bash
