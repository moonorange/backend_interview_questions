# QA for linux quizzes

## Differences between > and >> on linux

\> overwrites the contents of an existing file, while >> appends new data to the end of it.

## How do you check CPU usage in Linux?

Use top to see CPU usage per core, Memory usage, and Running processes (real-time)
I can sort the process by cpu usage, memory usage, etc.

htop is a better UI version of top.

## How do you check memory usage?

Use free -h or vmstat

## How do you check disk usage?

df -h (filesystem usage)
du -sh (directory usage)

## How do you list running processes?

ps aux returns all running processes
top
pgrep <process name> returns PID of match process

## How do you terminate a process

kill <PID>
kill -9 <PID> (force kill)

## How do you find a file in Linux?

find /path -name filename
locate filename

## How do you check active network connections?

ss -tulnp shows which ports are open and which process are using them.

-t → TCP
-u → UDP
-l → listening ports
-n → numeric output (no DNS)
-p → process info
