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

2. Actions here...

## 💡 Key Takeaway
> What you learned in this level.

---
