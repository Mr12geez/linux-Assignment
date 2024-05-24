# linux-Assignment
Questions & Answers for system access and file system 

Commands in Linux:	
How to create a file?	touch example.txt

How to create a directory?	mkdir my_directory

How to list the contents of a directory?	ls

How to change the directory?	cd my_directory

How to create a user?	adduser new_user

How to give permissions to a user?	chmod u+rwx file.txt

How to change the user?	su username

Accessing a Linux Server:	
What are the different ways to access a Linux server?	- SSH (Secure Shell) - FTP (File Transfer Protocol) - SFTP (SSH File Transfer Protocol) - Web-based Control Panels (e.g., cPanel, Plesk)

Root Directory vs Root User:	
What is the difference between the root directory and the root user?	- Root Directory: Top-level directory in the filesystem hierarchy (/) while Root User: Special user account with administrative privileges (superuser)

Root Directory and Home Directory:	
In Linux, is your root directory your home directory?	No, the root directory (/) is not the same as a user's home directory. The root user's home directory is typically /root, while regular users' home directories are usually located under /home.


Questions and Answers for Linux concepts 

What is the command that gives you information about other commands in Linux? - The man command is used to display the manual pages for other commands in Linux. It provides detailed information on command syntax, options, and usage examples. Example: man ls

What is a pipe command for? And how do we use it with grep?	A pipe command, denoted by |, connects the output of one command to another in Unix-like systems. When used with grep, it filters text based on patterns. For instance, cat example.txt | grep apple prints lines containing "apple" from example.txt. This simplifies text processing tasks effectively.

Write the command to give read, write, executable permission to a file called filename to the user and the group and no permission to others?	chmod ug+rwx filename This command grants read, write, and execute permissions to the user (u) and the group (g), while denying any permissions to others.

What is chown for?	The chown command is used to change the ownership of files and directories in Linux. It allows you to change both the user and group ownership of a file or directory. Example: chown user:group filename

What command do we use to remove files and directories in Linux?	The rm command is used to remove files and directories in Linux. To remove a file, you can use: rm filename. To remove a directory and its contents recursively, you can use: rm -r directoryname.

What command do we use to see the content of a file without editing the file?	The cat command is used to display the contents of a file without editing it. Example: cat filename

How do you check the processes running on your Linux server?	The ps command is used to display information about currently running processes on a Linux server. For a more detailed and continuously updated list, you can use: top or htop

Where are the logs stored in Linux?	Logs in Linux are typically stored in the /var/log directory. Various system and application logs are stored here, providing valuable information for troubleshooting and monitoring.


Questions and Answers for Networking: 

What is the difference between static and DHCP IP?	Static IP: Manually assigned, doesn't change. DHCP IP: Assigned dynamically by a DHCP server.

How to define static IP address in Ubuntu server?	Edit /etc/netplan/01-netcfg.yaml, specify IP, gateway, DNS under network: with renderer: networkd.

How to check if you have a package installed in Ubuntu system?	Use `dpkg -l

What is the purpose of DNS?	DNS (Domain Name System) translates domain names to IP addresses, facilitating human-readable web browsing.

What command is used to check the IP address in Linux?	ifconfig or ip addr show command is used to check IP address in Linux.

What is tcpdump used for?	Tcpdump is a packet analyzer used for network troubleshooting and packet capturing.

What is a firewall? What command is used in Linux to allow/disallow ports?A firewall filters network traffic. In Linux, iptables is used for firewall configuration. Commands like iptables -A INPUT -p tcp --dport port_number -j ACCEPT allow ports.


Questions and Answers for Shell Script 

What is a kernel?	The kernel is the core component of an operating system that manages system resources and facilitates communication between hardware and software.

What is the first line in shell script?	#!/bin/bash is the first line, known as a shebang, indicating the script should be interpreted using the Bash shell.

Why do we need shell script?	Shell scripts automate tasks, enhance productivity, and provide a convenient way to execute commands and programs in a sequence.

What is an if statement, for loop in shell script? In what case do you use each of the two?	if statements execute code conditionally based on a condition. for loops iterate over a sequence of values. if is for conditional branching, while for is for iteration over a list of items.

What is the output text in Linux? What is the command to read value from a user?	Output text is information displayed in the terminal. read command reads input from a user in a shell script.


Questions and Answers for Command with one example each

awk:	awk '{print $1}' file.txt extracts the first column from file.txt and prints it.

sed:	sed 's/old/new/' file.txt substitutes the first occurrence of "old" with "new" in file.txt.

cut:	cut -d',' -f1 file.csv extracts the first field from comma-separated values in file.csv.

sort:	sort file.txt sorts the lines in file.txt alphabetically.

