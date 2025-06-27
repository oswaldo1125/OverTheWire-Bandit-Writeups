# 🔐 Bandit Level 1 → Level 2

## 🎯 Objective
> The password for the next level is stored in a file called - located in the home directory

## ⚙️ Tools/Commands Used
- `sshpass`
- `export`
- `ls`
- `pwd`
- `cat`

## 🧠 Step-by-Step Solution

1. **Connect:**  
in the first level machine, I used `ssh` command to log into the machine, but for this level, I started using `sshpass` because this command allows us to log in directly, unlike the `ssh`command, which first prompts us for login and then asks for the password manually     
To use the `sshpass`command, we need the following estructure:

```bash
sshpass -p 'password' ssh bandit1@bandit.labs.overthewire.org -p 2220
```
![screenshot]()

2. **find the file**   
to find the file we need to use `ls` command, this  command allow us to list all the files in the  directory.
![screeshot](../ASSETS/ejercicio%202/ejercicio%202.2.jpg)

3. **open file named "-" :**  
normally, when we want to print the contentd of the file, we can use the `cat`command, however, when dealing with a hyphen "-" things work a bit differently.
if we try to use `cat` followed by a filename that begins with `-` the environment interprets is as an option or flag, not as a filename  
to open files like this, there´re differents ways to do
- we can use absolutly rout following by the name of the file `cat /home/bandit1/-` also we can use a relatiavely rout `cat ./-`  
![screenshot](../ASSETS/ejercicio%202/ejercicio%202.3.jpg)

## 💡 Key Takeaway
> What you learned in this level.

---
