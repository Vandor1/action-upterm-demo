
# action-upterm demo

This repository demonstrates using owenthereal/action-upterm to SSH into a GitHub Actions runner, backed by tmux.  
The workflow creates `demo_folder/hello.txt` so you can verify file access interactively.

## How to use
1. Push a commit or run the workflow manually.
2. Open the workflow run → job logs. Look for the SSH connection string printed by the Action.
3. From your terminal: `ssh <that-connection-string>` (your GitHub profile must have an SSH public key).
4. Inside the session, try:


ls -la
ls -la demo_folder
cat demo_folder/hello.txt
tmux ls

