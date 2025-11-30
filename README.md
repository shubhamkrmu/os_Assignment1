OS Process Management using Python

This repository contains Python programs demonstrating Linux process management concepts using the os module.

Works only on Linux / WSL — os.fork() and /proc are not supported on Windows.

Features / Tasks
1. Create N Child Processes

Uses os.fork()

Each child prints PID, parent PID, and a message

Parent waits using os.wait()

2. Execute Commands using exec()

Each child runs Linux commands (ls, date, ps) using os.execvp() or subprocess.

3. Zombie & Orphan Processes

Zombie → Parent does NOT wait

Orphan → Parent exits before child

Check zombies using:

ps -el | grep defunct

4. Read Process Info from /proc

Reads:

Name

State

RAM usage

Executable path

Open file descriptors

5. CPU Scheduling with nice()

Creates CPU-heavy tasks with different priorities:

nice = -5 (high priority)
nice = 0
nice = 10 (low priority)

How to Run
1. Clone the repo
git clone https://github.com/<username>/<repo>.git
cd <repo>

2. Run the main program
python3 process_management.py

3. Choose a menu option

