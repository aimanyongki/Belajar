# Python in the Background

Sometimes running a program can take a long time. <br>
This shows you how to run a python script in the background using `nohup`, a POSIX command to ignore the HUP (hangup) signal. <br>
Other alternatives are available, such as: `screen`, etc. <br>

Basic command:<br>
`$ nohup abcd &`<br>
`$ exit`

In my case, I would like to run a python script on the server. Here is my settings. <br>
First, we could add a shebang command on the top of our script <br>
`#!/usr/bin/env python`

Then, set permissions of the file to allow execution<br>
`chmod +x myscript.py`

Run the script with `nohup` which allows you to close the terminal without stopping the execution<br>
`nohup /path/to/myscript.py &`

For now you can exit the session until the execution is finished. <br>

In case you want to check whether the script is running or not, you can use `htop` command. <br>
You can get your `PID` number and kill the process if you want to stop the process, by typing <br>
`kill PIDnumber`

When the process is finished, you can check the log file about what happened and fix your program if there are some errors.<br>
Please note that you can only check the log file during the execution if you specify the command to avoid output buffering by adding `-u` flag <br>
`nohup -u /path/to/myscript.py > output.log &`
