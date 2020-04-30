Terminology 
Shell scripting: commands written for the shell to execute 
Shell script: A file or program that shell will execute
Sh (Bourne Shell): A shell interpreter
Bash (Bourne Again Shell): The improved version of Sh

How it works
Let's take an example. 
One common command people used is touch for creating a file. touch is a binary executable file located inside /bin directory of the system. 

After executing the touch command, the shell interpreter will checks for an alias present in .bash_profile in home directory. If alias is not present, then it looks for a binary executable file in the PATH.

We are allowed to execute multiple Bash commands saved in a file and execute them at once with bash function.
....






https://itnext.io/bash-scripting-everything-you-need-to-know-about-bash-shell-programming-cd08595f2fba
https://devhints.io/bash
