## How to work with Jupyter Notebook remotely (via SSH)
<br>

1. Log in over `ssh username@remoteserver` <br>

2. Activate conda envs <br>
`conda activate py3` <br>

3. Run jupyter notebook <br>
`jupyter notebook --no-browser --port=8888` <br>

4.a. Open new terminal, type <br>
`ssh -NL 8888:localhost:8888 username@remoteserver` <br>

4.b. SSH tunnel via multiple host <br>
`ssh -t -L 8888:localhost:8888 username1@remoteserver1 ssh -L 8888:localhost:8888 -N username2@remoteserver2` <br>

5. Open browser on your local computer, copy the Jupyter Notebook's URL from step 3 [e.g. http://localhost:8888/?token=...], pu it on your browser's address bar <br>

6. Happy coding!
