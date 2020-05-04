## How to work with Jupyter Notebook remotely (via SSH)
<br>

1. Log in over `ssh username@remoteserver` <br>

2. Activate conda envs <br>
`conda activate py3` <br>

3. Run jupyter notebook <br>
`jupyter notebook --no-browser --port=8888` <br>

4. Open new terminal, type <br>
`ssh -NL 8888:localhost:8888 username@remoteserver` <br>

5. Open browser on your local computer, go to Jupyter Notebook's URL <br>
