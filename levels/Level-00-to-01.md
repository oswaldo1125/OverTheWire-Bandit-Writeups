# 🔐 Bandit Level 0 → Level 1

## 🎯 Objective
> The password for the next level is stored in a file called readme located in the home directory. Use this password to log into bandit1 using SSH. Whenever you find a password for a level, use SSH (on port 2220) to log into that level and continue the game.

## ⚙️ Tools/Commands Used
- `ssh`
- `export`
- `ls`
- `cat`

## 🧠 Step-by-Step Solution

1. **Connect:**  
to start the challenge, we first need to conect to an SSH server. we use the following command: 
```bash
ssh bandit0@bandit.labs.overthewire.org -p 2220
```
- `ssh:` tells the system to start a secure connection to a remorte server.
- `bandit0:` the username we use to log in.
- `@:` separates the username from the server address
- `-p:` specifies the port number we must use for the connection (instead of the default port 22)  
![screenshot](../ASSETS/ejercicio%201.2.jpg)

2. **change default terminal:**  
sometimes, when we log into a new machine, certain commands may not work properly, this is usually due to the environment settings.   
for example, when we connect to the bandit level 0 machine, the shortcut `ctrl + l` (used to clear the screen) doesn´t work as expected.  
to fix this, we can use the following command:
```bash 
export TERM=xterm
```
![screenshot](../ASSETS/ejercicio%201.1.jpg)

3. **Visualize the file:**  
after logging into the machine and setting the environment, we can view the files within the current directory:
```bash
ls /home/bandit0
```
![screenshot](../ASSETS/ejercicio%201.3.jpg)

4. **print and read the file´s content:**  
once we locate the file, we use the `cat`command to display its contents. 
```bash
cat /home/bandit0/readme
```
![screenshot](../ASSETS/ejercicio%201.4.jpg)

## 💡 Key Takeaway
> What you learned in this level:  
In this first level, I learned how to use the `ssh` command to connect to SSH servers. I also discovered that there are different ways to run a command. For example, when using `ls` or `cat`, I can execute the command by placing it after `./` (which represents the current directory), or by providing the absolute path, such as /home/bandit0/readme.
---
