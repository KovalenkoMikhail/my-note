🐧 Linux and WSL Cheatsheet
This paper helps you with Linux and WSL. It has simple commands and tips for your work.

⚙️ Basic Commands
What is WSL?
WSL is for Windows. It helps you use Linux programs on a Windows computer. It works with VS Code.

Basic Linux Commands
Move to a folder: cd

See files in a folder: ls

See your location: pwd

Copy a file: cp

Move or change a file name: mv

Delete a file: rm

Delete a folder: rm -rf

📊 Check Your Computer
You must check your computer. It helps it work well and not have problems.


Лицензировано Google
Check Disk Space
Check your disk space. A full disk can stop the computer.

Commands to remember:

df -h: Show disk space. It is a fast way.

du -sh /path/to/directory: Show how big a folder is.

du -sch /path/* | sort -h: See which files are the biggest in a folder.

Job Interview Questions:

Q: How do you know the disk is full?

A: I check with df -h. I can also get a message from the system.

Q: What is the difference between df and du?

A: df shows all disk space. du shows files and folders.

Check Memory (RAM)
Check memory to see if the computer is fast.

Commands to remember:

free -h: See how much memory is free.

top / htop: See which program uses a lot of memory.

ps aux --sort=-%mem: See the program that uses the most memory.

Job Interview Questions:

Q: What is Swap space?

A: Swap is part of the disk. It is like extra memory. If the computer uses it too much, it becomes slow.

Q: How to know a real memory problem?

A: I look at the available space with free -h. If it is small, it is a problem.

Check CPU Usage
Check the CPU to see if the computer is busy.

Commands to remember:

top / htop: Good tools to see the CPU in real-time.

uptime: See how long the computer is on. It also shows the load average.

ps aux --sort=-%cpu: See the program that uses the most CPU.

Job Interview Questions:

Q: What is "Load Average"?

A: It is a number. It shows how many programs are waiting to use the CPU. A big number is bad.

Install Updates
Install updates to be safe. It is very important.

Commands to remember:

sudo apt update and sudo apt upgrade: Update all your programs.

unattended-upgrades: This can update your computer for you.

Job Interview Questions:

Q: Why not auto-update?

A: It can break the program. It is better to check first.

Q: What if an update breaks a program?

A: I stop the update and fix the problem. I tell my team.

Use Scripts
Scripts help you do tasks fast. They save time and stop mistakes.

Example Script: This script finds old files and deletes them.

#!/bin/bash

# Path to the logs folder
LOG_DIR="/var/log/my_app"

# Check if the folder is there
if [ ! -d "$LOG_DIR" ]; then
    echo "Folder $LOG_DIR not found."
    exit 1
fi

echo "Start log rotation..."

# Find .log files older than 7 days and make them smaller
find "$LOG_DIR" -type f -name "*.log" -mtime +7 -exec gzip {} \;

# Find and delete files older than 30 days
find "$LOG_DIR" -type f -name "*.log.gz" -mtime +30 -delete

echo "Log rotation is done."

exit 0

Deploy New Software
Deploying is to put a new program on a server. It can be a manual or an automatic process.

Job Interview Questions:

Q: How to deploy with no server downtime?

A: I use a special way. For example, Blue/Green or Canary deploy. The old program works until the new one is ready.


Лицензировано Google
Simple Commands Summary
df -h: Check disk space.

du -sh /path: Check a folder size.

top/htop: See which program uses CPU and memory.

free -h: Check memory.

uptime: Check server load.

tail -f file.log: See a log file live.

grep "Error" file.log: Find "Error" in a log file.

chmod +x script.sh: Make a script run.

ps aux | grep java: Find a java program.

kill -9 PID: Stop a program fast.
