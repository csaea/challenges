# Bash/Linux Scripting Challenges 

> **IMPORTANT**: Run these challenges in a virtual machine! Otherwise you may ruin your own system.
> 
> [https://apps.cyber.org/](https://apps.cyber.org/)

## Table of Contents
- [System Challenges](#System-Challenges)
- [Attack Simulation Challenges](#Attack-Simulation-Challenges)

---

## System Challenges 

### Challenge 1.1 - Tree to File

**Objectives**:  
- Create an executable script that outputs the `tree` structure of a directory and its subdirectories into a new text file. 
- Display a message when the script is complete and automatically open the new file.

**Commands/Concepts**: `tree`, `echo`, `>`, `open`

---

### Challenge 1.2 - Backup Script  

**Objectives**:  
- Create a backup script that copies all contents from one directory to a backup folder. 
- List all the files in the backup directory in the terminal. 
- Print a message that the backup is complete, along with the date.

**Commands/Concepts**: `cp`, `mkdir`, `ls`, `echo`, `date` 

---

## Attack Simulation Challenges

### Challenge 2.1 - CPU Resource Flood

**Objectives**: Use resource exhaustion to simulate:
1. A DoS attack
2. A countermeasure

**Steps**:
1. In one terminal window, run `top` and take note of the total tasks running.
2. In a second terminal, create a script that iterates over a `dd` command 1000 times to overload the system.
3. Run the script.
4. Monitor CPU usage with `top` or `htop` to observe the resource consumption. *(Warning! Your system may crash.)*
5. Write a countermeasure script that limits the number of processes that can run.
6. Try running the first script again and see if your second script is successful. 

**Commands/Concepts**: `dd`, `top` or `htop`, `ulimit`.

---

### Challenge 2.2 - File Permissions

**Objectives**: Demonstrate how malware might alter file permissions to gain unauthorized access.

**Part I**:  
- Create an executable file using `touch`.
- Modify the file permissions using `chmod` to make it executable by others.
- Simulate an attack where a script is placed inside a shared directory and is executed without proper authorization.

**Part II**:  
- Write a countermeasure script to restore secure permissions to all files in a directory.

**Commands/Concepts**: `chmod`, `touch`, `ls`, `chmod 777`, `find`.

---

### Challenge 2.3 - Malware Executing System Commands (Privilege Escalation)

**Objectives**: Learn how attackers use privilege escalation through malicious scripts.

**Part I**:  
- Create a script that executes a system command (like `ls` or `cat`) but is disguised as an innocuous file.
- Use `chmod` to make the file executable and simulate the attack.

**Part II**:  
- Write a detection script that identifies and alerts the user to newly created executable files in sensitive directories.

**Commands/Concepts**: `chmod`, `ls`, `cat`, `ps`, `find`.

---

### Challenge 2.4 - The Hidden Alias

**Objective**: Learn how attackers can hide malicious commands in aliases or environment variables.

**Steps**:
- Create an alias that runs a harmful command when you type a common command (e.g., `ls`).
- Use `echo` to define the alias in the `.bashrc` file.
- Test the alias by typing the command (e.g., `ls`) to see the malicious behavior.
- Write a script that lists all current aliases and looks for suspicious ones.

**Commands/Concepts**: `alias`, `echo`, `cat`, `grep`.

---

### Challenge 2.5 - Propagation

**Objective**: Propagate via USB drives.

**Steps**:
- Write a simple script that copies itself to a USB drive and automatically runs when the USB is inserted.
- Use `touch` and `cp` to simulate the process of copying malicious files to the USB.
- Create a script to detect if a device is connected and if there are new executable files on the USB.

**Commands/Concepts**: `cp`, `ls`, `touch`, `chmod`, `find`.

---

### Challenge 2.6 - Modify System Files

**Objective**: Show how an attacker might inject malicious code into critical system files.

**Steps**:
- Use `echo` and `cat` to append a command to a critical file (e.g., `/etc/hosts` or `/etc/passwd`).
- Simulate the effect by trying to access the system or a network service.
- Create a monitoring script that checks these files regularly for unauthorized changes.

**Commands/Concepts**: `echo`, `cat`, `cp`, `chmod`, `find`.
