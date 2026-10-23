# Day 1 - setup complete
- 23 Oct: Setup completed (WSL, Java 17, Git, SSH, VsCode)
- 24 Oct: Practiced git commit with editor

## Day 0 - 23 Oct 2026: Environment setup and Linux basics

### Setup
- Installed Ubuntu on WSL2 and set the username and password
- Installed Java 17, Git, curl and extra tools (tree, htop, jq)
- Limited WSL memory to 4 GB with `.wslconfig` (swap now 4 GB)
- Updated WSL (`wsl --update`) and checked the kernel with `uname -r`
- Created an SSH key, added it to GitHub and tested it with `ssh -T git@github.com`
- Connected VS Code to WSL (the corner shows WSL: Ubuntu)

### Linux concepts learned
- `PATH` is the list of folders the shell searches for commands
- `which` shows where a program is stored
- Exit codes: 0 = success, 1 = failed, 127 = command not found
- Linux is case-sensitive (`which` works, `WHICH` does not)
- Permissions: r = 4, w = 2, x = 1. So -rwxr-xr-x = 755 and -rw-r--r-- = 644
- `free -h`: the "available" column matters more than "free"
- Output is for reading, and only commands are typed at the prompt

### Git concepts learned
- Three places: working folder, staging area (`git add`), history (`git commit`), then GitHub (`git push`)
- `git commit` without `-m` opens an editor
- Fixed a wrong commit message with `git rebase -i` and `reword`
- `git push --force-with-lease` is safe only on a branch nobody else uses

### Commands practiced
`pwd`, `ls -l`, `ll`, `cd`, `cat`, `nl`, `tail`, `echo $PATH`, `echo $?`, `which`, `chmod 755`, `touch`, `rm`, `sed -i`, `free -h`, `nproc`, `df -h`, `git add`, `git commit`, `git push`, `git log --oneline`

### Errors and fixes
- `Repository not found`: wrong GitHub username in the clone link
- `command not found` (127): typed output as a command
- `nl` with no file name waited for input; stopped it with Ctrl + C
- `--online` is wrong, `--oneline` is correct