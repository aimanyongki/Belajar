# Python in the Background

Sometimes running a program can take a long time.
This shows you how to run a python script in the background using `nohup`, a POSIX command to ignore the HUP (hangup) signal.
Other alternatives are available, such as: `screen`, etc. <br>

Basic command:<br>
`$ nohup abcd &`<br>
`$ exit`

In my case, I would like to run a python script on the server. Here is my settings. <br>
First, we could add a shebang command on the top of our script <br>
`#!/usr/bin/env python`<br>
Then we need to activate the Conda environment, or source the custom Python path that we want to use.
By doing so, `#!/usr/bin/env` will find the right Python version, and also will make sure that the script will run correctly inside the virtual environment.<br>

Then, set permissions of the file to allow execution<br>
`chmod +x myscript.py`

Run the script with `nohup` which allows you to close the terminal without stopping the execution<br>
`nohup /path/to/myscript.py &`

For now you can exit the session until the execution is finished. <br>

In case you want to check whether the script is running or not, you can use `htop` command.
You can get your `PID` number and kill the process if you want to stop the process, by typing <br>
`kill PIDnumber`

When the process is finished, you can check the log file about what happened and fix your program if there are some errors.<br>
Please note that you can only check the log file during the execution if you specify the command to avoid output buffering by adding `-u` flag <br>
`nohup -u /path/to/myscript.py > output.log &` <br>
<br>
<br>
References:
https://janakiev.com/blog/python-background/ <br>
`“#!/usr/bin/env NAME”` vs `“#!/path/to/NAME”` <br>
https://unix.stackexchange.com/questions/29608/why-is-it-better-to-use-usr-bin-env-name-instead-of-path-to-name-as-my
