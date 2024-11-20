# Bash/Linux Scripting Challenges 

1 System Challenges
2 Simulated Attack Challenges

## Challenge 1.1 - Input to File

Objective: 
- Create an executable script that accepts one line of user input and redirects it to a txt file.

Commands/Concepts: `read`, `echo`, `>`

## Challenge 1.2 - Backup Script  

Objective: 
- Create a backup script that copies all contents from one directory to a backup folder. 
- List all the files in the backup directory in terminal. 
- Print a message that the backup is complete, along with the date. 

Commands/Concepts: `cp`, `mkdir`, `ls`, `echo` 

Bonus: Include a new file in the Backup Folder displaying the date that the backup occured. 




## Challenge 2.1 Simulate a Denial-of-Service (DoS) Attack Using Resource Exhaustion

Objective: Learn how malicious users might use resource exhaustion to perform a DoS attack.


Part 1. Create a script that launches multiple instances of a resource-heavy command (e.g., ping or dd) to flood the network or system resources.
        Monitor CPU usage with top or htop to observe the resource consumption.
        
Part 2. Write a countermeasure script that limits the number of allowed processes (e.g., using ulimit).

Commands/Concepts: ping, dd, top, ulimit.

## Challenge 2.2: Malicious File Permissions

Objective: Demonstrate how malware might alter file permissions to gain unauthorized access.

Part I. 
-Create a file using touch.
-Modify the file permissions using chmod to make it executable or readable by others.
-Simulate an attack where a script is placed inside a shared directory and is executed without proper authorization.

Part II.
-Write a script to restore secure permissions to all files in a directory.

Commands/Concepts: `chmod`, `touch`, `ls`, `chmod 777`, `find`.

## Challenge 3: Malware Executing System Commands (Privilege Escalation)

Objective: Learn how attackers use privilege escalation through malicious scripts.

Part I. 
Create a script that executes a system command (like ls or cat) but is disguised as an innocuous file.
Use chmod to make the file executable and simulate the attack.

Part II.
Write a detection script that identifies and alerts the user to newly created executable files in sensitive directories.

Commands/Concepts: chmod, ls, cat, ps, find.

Challenge 4: Simulate a Backdoor with Cron Jobs

Objective: Understand how an attacker might use cron jobs for persistence.

    Steps:
        Create a malicious script that could run periodically, like a reverse shell or data exfiltration.
        Add it to crontab to run at a scheduled time (e.g., every minute).
        Write a script that monitors changes to crontab and alerts the user when an unusual cron job is added.

    Commands/Concepts: crontab, cron, chmod, ps, cat, echo.

## Challenge 5: Data Exfiltration Using wget

Objective: Simulate how malware can steal sensitive data using common utilities like wget.

-Create a sample text file with sensitive data.
-Use wget to send the file to an external server (simulated or real) over HTTP.

-Create a script that scans for outgoing requests to suspicious domains using netstat and grep.

Commands/Concepts: wget, netstat, grep, cat.

## Challenge 6: Hidden Malware with echo and Aliases

Objective: Learn how attackers can hide malicious commands in aliases or environment variables.

-Create an alias that runs a harmful command when you type a common command (e.g., ls).
-Use echo to define the alias in the .bashrc file.
-Test the alias by typing the command (e.g., ls) to see the malicious behavior.
-Write a script that lists all current aliases and looks for suspicious ones.

Commands/Concepts: alias, echo, cat, grep.

## Challenge 7: Script to Infect USB Drives (Malware Propagation)

Objective: Understand how malware can propagate via USB drives.

-Write a simple script that copies itself to a USB drive and automatically runs when the USB is inserted.
-Use touch and cp to simulate the process of copying malicious files to the USB.

-Create a script to detect if a device is connected and if there are new executable files on the USB.

Commands/Concepts: cp, ls, touch, chmod, find.

## Challenge 8: Detecting a Reverse Shell

Objective: Understand how attackers might establish reverse shells to control compromised systems.

    Steps:
        Create a reverse shell script using nc (netcat) that connects back to an attacker's machine.
        Simulate the victim running this reverse shell.
        Use netstat to identify suspicious outgoing connections to the attacker's machine.
        Write a script to scan for reverse shell connections and alert the user.

    Commands/Concepts: nc, netstat, ps, grep, echo.

Challenge 9: Modify System Files with echo and cat

Objective: Show how an attacker might inject malicious code into critical system files.

    Steps:
        Use echo and cat to append a command to a critical file (e.g., /etc/hosts or /etc/passwd).
        Simulate the effect by trying to access the system or a network service.
        Create a monitoring script that checks these files regularly for unauthorized changes.

    Commands/Concepts: echo, cat, cp, chmod, find.

Challenge 10: Malw
