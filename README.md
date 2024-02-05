# Tmux Cheat Sheet

This is a cheat sheet for basic tmux commands for session management.

## Getting Started with tmux

tmux is a terminal multiplexer, allowing you to create, manage, and navigate through multiple terminal sessions from a single window. Below are some common commands to help you get started with tmux.

### 1. Create a New Session with a Name

```bash
tmux new -s <session_name>
```
Replace <session_name> with your desired session name.


### 2. Detach from a Session

To detach from a session, press Ctrl + b then d.


### 3. Reattach to an Existing Session by Name

```bash
tmux attach -t <session_name>
```
Replace <session_name> with the name of the session you want to reattach.


### 4. Delete a Session by Name

```bash
tmux kill-session -t <session_name>
```
Replace <session_name> with the name of the session you want to delete.


### 5. Delete all sessions

```bash
tmux ls | grep : | cut -d. -f1 | awk '{print substr($1, 0, length($1)-1)}' | xargs -I {} tmux kill-session -t {}
```
Warning: This command will terminate all your tmux sessions.


### 6. List All tmux Sessions
```bash
tmux ls
```
