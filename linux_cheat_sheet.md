# Linux Cheatsheet

## What are environment variables?

- Dynamic values that influence the behavior of processes and applications in the OS
- Pass config info to programms and scripts without having to modify the code itself

Exist as Key-value pairs e.g.
- HOME=/home/username (sets home directory)
- PATH=/usr/bin:/bin  (sets paths for OS to look for executable files)
- PWD (stores current directory for use)

## Setting variables

Variables are assigned with an equals sign ```MY_VAR="Hello"```

Variables are called/accessed with dollar sign ```echo $MY_VAR```

## Setting environment variables

Set environment variable with ```export MY_ENV_VAR="Hello, World"```

## Making Environment Variables Persistant

1. add the  ```export MY_ENV_VAR="Hello, World``` line to config files like ```~/.bashrc```
2. reload the file with ```source ~/.bashrc```

## What is a process

- An instance of a program running in the system
- Each process has a unique process ID (PID)

## View running processes

Use ```ps``` or ```top```

## What are child processes?

- Processes created by another process (the parent process)
- When shell script calls a command the command is run as a child porocess

## Running process in background

Add an ```&``` at the end of command e.g. ```sleep 60 &```

## Kill Processes

terminate process using its PID ```kill PID```

for forcefull termination use ```kill -9 PID```

## Linux Permissions

Permission system to control file access

3 permission groups
1. Owner: The file creator
2. Group: Other users in files group
3. Others: Everyone else

Each group has 3 permissions
1. Read (r): Permission to view the file
2. Write (w): Permission to modify the file
3. Execute (x): Permission to execute the file as a program

Permissions are expressed in three digits using octal (base-8) values:
- 4 = Read
- 2 = Write
- 1 = Execute

These are combined to define a groups permission
- e.g. 7 = r + w + x

Permissions often expressed as 3 digit number:
- 1st digit = Owner
- 2nd digit = Group
- 3rd digit = Others

## Change permissions 

use ```chmod xxx file.txt``` with xxx being the permissions

e.g. ```chmod 744 file.txt``` = rwx-r--r--