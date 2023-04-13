<p style="text-align:center;"><img title="a title" alt="Alt text" src="/bash-resources/bash-logo-small.png">         <img title="a title" alt="Alt text" src="/bash-resources/linux.png"></p?>

# Linux , Bash & Shell Scripting

*Please Note : Though this repository has been created considering users of all levels (beginners, intermediate and experts) , but it is recommended that before using the repo , you should complete a docker course offered by pluralsight which is available to all LGB employees. The course will provide all the required and idepth knowledge about docker and should be supplemented by hands On labs supplied as part of this repo.*

**Here is the course link and description -- >   <<Link to be added>>**

## What is Linux

Linux is a free and open-source operating system (OS) based on the Unix operating system. It was first created by Linus Torvalds in 1991 and has since become one of the most widely used operating systems in the world.

Linux is known for its flexibility, stability, and security, and is used in a wide range of applications, from servers and supercomputers to smartphones and embedded systems. Linux is also popular among developers and programmers, who use it as a platform for software development and testing.

One of the key features of Linux is that it is distributed under a free and open-source license, which means that anyone can use, modify, and distribute the source code of the operating system. This has led to a large and vibrant community of developers who contribute to the development of Linux and create various distributions, or versions, of the operating system.

## Linux Folder Structure

<img title="a title" alt="Alt text" src="/bash-resources/file.png">

Linux is organized in a hierarchical file system structure, similar to other Unix-like operating systems. The root directory is the top-level directory in the hierarchy, represented by a forward slash (/), and all other files and directories are organized beneath it. Here is a brief overview of the main directories in the Linux file system:

- **/bin:** Contains binary files (programs) that are essential to the system's operation. These are often used by the system administrator or system scripts.

- **/boot:** Contains the files needed to boot the system, including the Linux kernel, boot loader, and configuration files.

- **/dev:** Contains device files, which are special files that represent devices like hard drives, printers, and USB devices.

- **/etc:** Contains system configuration files, including network settings, system startup scripts, user account information, and more.

- **/home:** Contains the home directories for individual users on the system.

- **/lib and /lib64:** Contains library files, which are collections of precompiled code used by applications and the operating system.

- **/mnt:** Contains directories for mounting external storage devices, such as USB drives or network shares.

- **/opt:** Contains optional software packages that are installed on the system.

- **/proc:** Contains system information and process data, presented as files that can be read by programs.

- **/root:** The home directory for the root user, which is the system administrator.

- **/sbin:** Contains system binaries (programs) that are essential to the system's operation. These are often used by the system administrator or system scripts.

- **/tmp:** Contains temporary files that are created by various programs.

- **/usr:** Contains user programs and supporting files, including libraries, documentation, and shared resources.

- **/var:** Contains variable data files, such as log files, system mail, and printer spools.

This file system structure is important for managing and organizing the files and directories on a Linux system, and it provides a standardized way of accessing and manipulating the files and directories in the system.



## Linux Distros
Some of the most popular Linux distros include:

1.  **Ubuntu:** One of the most popular and user-friendly Linux distros, Ubuntu is designed for desktop and laptop computers and is based on the Debian architecture.
    
2.  **Debian:** A stable and reliable Linux distro that is popular among servers and other mission-critical systems.
    
3.  **Fedora:** A community-driven distro that is sponsored by Red Hat and is designed for developers, system administrators, and other advanced users.
    
4.  **CentOS:** A stable and secure distro that is based on the Red Hat Enterprise Linux codebase and is popular among servers and other enterprise-level systems.
    
5.  **Arch Linux:** A lightweight and customizable distro that is designed for experienced Linux users who want a high degree of control over their system.
    
6.  **openSUSE:** A versatile and easy-to-use distro that is popular among desktop users, developers, and system administrators.
    
7.  **Mint:** A user-friendly and beginner-friendly distro that is based on Ubuntu and is designed for desktop and laptop computers.
    

These are just a few examples of the many different Linux distros available. Each distro has its own strengths and weaknesses, and the best one for you will depend on your specific needs and preferences.


## What is Shell ? 

A shell is a command-line interface (CLI) program that provides a user interface for accessing an operating system's services and running commands. The shell is typically the first layer of interaction between a user and the operating system, and it provides a way for users to communicate with the system by typing commands and viewing the output.

The shell provides a prompt that allows users to enter commands and arguments. The shell then interprets these commands and runs them by calling the appropriate system functions and programs. The shell also provides various features such as command history, tab completion, and scripting capabilities, which make it a powerful tool for managing and automating system tasks.

There are several different shells available for Unix and Unix-like operating systems, such as Bash, Korn shell (ksh), C shell (csh), and Z shell (zsh), each with its own set of features and capabilities. Bash is the most widely used shell and is the default shell for many Linux distributions.

## What is Bash ? 

Bash is a popular Unix shell that provides a command-line interface (CLI) for interacting with an operating system. Bash stands for "Bourne-Again SHell," which is a reference to its predecessor, the Bourne shell (sh). Bash is the default shell on most Linux and macOS systems, and is also available on Windows 10 as part of the Windows Subsystem for Linux (WSL).  

Bash provides a set of built-in commands and utilities for performing various tasks, such as file and directory management, process control, and text manipulation. Bash also supports shell scripting, which allows users to write programs that automate repetitive tasks or perform more complex operations.  

In addition to its built-in functionality, Bash can also be extended through the use of command-line tools, utilities, and scripts that are available on the system or can be installed separately.  

Overall, Bash is a powerful and versatile tool that is widely used by developers, system administrators, and power users for managing their computing environments.  


Here are some Bash basics:

**1. Commands:** Bash can execute various commands, such as ls, cd, cat, echo, and many more. Commands are typically entered on the command line, followed by any arguments or options.

**2. Variables:** Bash supports variables, which are used to store data that can be referenced later in the script. Variables are defined using the syntax "variable=value". For example, "name=John" defines a variable named "name" with the value "John".

**3. Control structures:** Bash supports various control structures, such as if-else, for loop, while loop, case, and function. These control structures are used to control the flow of the script and perform conditional logic.

**4. Input and output:** Bash can read input from the user or from files, and it can output data to the screen or to files. The most common way to read input is through the "read" command, and the most common way to output data is through the "echo" command.

**5. Environment variables:** Bash has several built-in environment variables, such as HOME, PATH, USER, and SHELL. These variables provide information about the system and the user, and they can be accessed and modified by the script.

**6. Scripting:** Bash can be used to write scripts, which are essentially a series of commands and control structures that are executed in sequence. Bash scripts are saved as plain text files and typically have the file extension ".sh".

These are just some of the basic features of Bash. As you become more familiar with Bash, you will learn more advanced features and techniques.


# Bash and Shell Scripting - let's get the basics right

Bash is a specific type of shell, and shell scripting refers to the practice of writing scripts that run on a shell. So in a sense, **Bash is a subset of shell scripting.**

Again , the term "shell" refers to a command-line interface that allows users to interact with an operating system by running commands. A shell can interpret and execute scripts written in a specific language, such as Bash, zsh, or csh. These scripts can be used to automate tasks, configure the operating system, or perform system maintenance.

Bash is a popular shell that is widely used in Unix-based operating systems such as Linux and macOS. It is a powerful and versatile shell that supports many advanced features, such as variables, conditionals, loops, functions, and pipelines. Bash scripts can be used for a wide range of tasks, from simple file operations to complex system administration tasks.

Shell scripting, on the other hand, refers to the practice of writing scripts that run on a shell. Shell scripts can be written in various languages, such as Bash, zsh, csh, and others. They can be used to automate repetitive tasks, perform system maintenance, configure the operating system, or build complex applications.

In summary, Bash is a specific type of shell that is widely used in Unix-based operating systems, and shell scripting refers to the practice of writing scripts that run on a shell. While Bash is a popular choice for shell scripting, other shells can also be used, and scripts can be written in various languages.  


# To write and run a Bash script, follow these steps:

- **Open a text editor:** Bash scripts are plain text files, so you can use any text editor to write them. For example, you can use the built-in editor in your terminal, such as nano or vim, or a graphical text editor, such as gedit or Sublime Text.

- **Write the script:** Write your Bash script in the text editor, using the Bash syntax and commands. Make sure to save the file with a .sh extension.

- **Set the file as executable:** Before you can run the script, you need to set it as executable. You can do this by running the command "chmod +x script.sh" in your terminal, where "script.sh" is the name of your script.

- **Run the script:** To run the script, simply type its name in the terminal and press Enter. For example, if your script is named "script.sh", you would run it by typing "./script.sh". The "./" tells the terminal to look in the current directory for the script.




Here is an example of a simple Bash script that prints "Hello, World!" to the screen:

```bash
#!/bin/bash

echo "Hello, World!"
```

Save this script as "hello.sh" and set it as executable using the command "chmod +x hello.sh". Then, run the script by typing "./hello.sh" in your terminal. You should see the output "Hello, World!" printed to the screen.  
  
**Here are some common Bash commands that you might find useful:**  

**File and Directory Management**
- cd [directory]: Change to the specified directory.
- ls: List the files and directories in the current directory.
- mkdir [directory]: Create a new directory with the specified name.
- touch [filename]: Create a new file with the specified name.
- cp [source] [destination]: Copy a file or directory from the source to the destination.
- mv [source] [destination]: Move a file or directory from the source to the destination.
- rm [file]: Remove the specified file.
- rm -r [directory]: Remove the specified directory and all its contents.
- chmod [permissions] [file]: Change the permissions of the specified file or directory.  

**Text Manipulation**
- cat [file]: Display the contents of a file.
- grep [pattern] [file]: Search for lines in a file that match the specified pattern.
- sed [options] [file]: Stream editor that can be used to perform complex text transformations on a file.
- awk [options] [file]: A powerful tool for processing and manipulating text data in files.  
  
**Process Control**
- ps: Display the list of currently running processes.
- top: Display the processes currently running on the system sorted by resource usage.
- kill [process id]: Terminate the process with the specified process ID.
- killall [process name]: Terminate all processes with the specified name.

**System Information**
- uname: Display information about the current operating system.
- df: Display information about disk space usage on the system.
- free: Display information about available memory on the system.

**Miscellaneous**
- history: Display a list of the commands that have been executed in the current session.
- sudo [command]: Run a command with superuser privileges.
- man [command]: Display the manual page for a command.  
  
This is just a small sample of the many Bash commands that are available. For more information and a complete list of commands, you can consult the Bash manual or run the help command in the terminal.


# Here are some Bash challenges to get you started :


1. Write a Bash script that takes a file name as an argument and counts the number of lines in the file.

```bash
#!/bin/bash

if [ $# -ne 1 ]; then
    echo "Usage: $0 file"
    exit 1
fi

file=$1
if [ ! -f "$file" ]; then
    echo "File $file does not exist"
    exit 1
fi

lines=$(wc -l &lt; "$file")
echo "$file has $lines lines"
```

2. Write a Bash script that takes a directory name as an argument and recursively counts the number of files in the directory and its subdirectories
   
```bash
#!/bin/bash

if [ $# -ne 1 ]; then
    echo "Usage: $0 directory"
    exit 1
fi

dir=$1
if [ ! -d "$dir" ]; then
    echo "Directory $dir does not exist"
    exit 1
fi

count=$(find "$dir" -type f | wc -l)
echo "$dir has $count files"
```

3. Write a Bash script that takes a string as an argument and searches all text files in the current directory for occurrences of the string. The script should print the name of each file that contains the string.

```bash
#!/bin/bash

if [ $# -ne 1 ]; then
    echo "Usage: $0 string"
    exit 1
fi

string=$1

for file in *.txt; do
    if grep -q "$string" "$file"; then
        echo "$file contains $string"
    fi
done
```

4. Write a Bash script that takes a directory name as an argument and creates a compressed archive file (e.g., tar.gz) of all files in the directory.
   
```bash
#!/bin/bash

if [ $# -ne 1 ]; then
    echo "Usage: $0 directory"
    exit 1
fi

dir=$1
if [ ! -d "$dir" ]; then
    echo "Directory $dir does not exist"
    exit 1
fi

tar -czf "$dir.tar.gz" "$dir"
echo "Archive created: $dir.tar.gz"
```

5. Write a Bash script that takes a file name as an argument and replaces all occurrences of a specified string with another string. The script should create a backup of the original file before making any changes.

```bash
#!/bin/bash

if [ $# -ne 3 ]; then
    echo "Usage: $0 file old_string new_string"
    exit 1
fi

file=$1
if [ ! -f "$file" ]; then
    echo "File $file does not exist"
    exit 1
fi

old_string=$2
new_string=$3

cp "$file" "$file.bak"
sed -i "s/$old_string/$new_string/g" "$file"
echo "Replaced $old_string with $new_string in $file"
```


## Launch a Linux ( Ubuntu ) VM in your GCP PlayPen

To launch an Ubuntu VM on Google Cloud Platform (GCP), follow these steps:

**Please Note : The GCP PlayPen comes with no VPC configuration. In case you are using the GCP PlayPen for the first time , you will need to create a VPC first** Skip these if you already have a VPC configured and move straight to Launch a Linux ( Ubuntu ) VM section.

To create a VPC (Virtual Private Cloud) on Google Cloud Platform (GCP), follow these steps:

1. Log in to your GCP console and select your project.

2. Click on the "Navigation menu" button on the top-left corner of the console, and navigate to the VPC Network section.

3. Click on "VPC networks" and then click on "Create VPC network".

4. In the "Create a VPC network" page, fill in the following details:
```
Name: A name for your VPC network.
Subnet creation mode: Choose "Automatic" to have GCP create subnets for you, or "Custom" to create your own subnets. ( Use Automatic for simplicity )
IP address range: The range of IP addresses to be used by your VPC network.
Subnet name and IP range: If you chose "Custom" subnet creation mode, you'll need to fill in this section to define your subnets.
```
5. Once you've filled in all the necessary details, click "Create" at the bottom of the page.

6. Your VPC network will take a few seconds to be created. Once it's ready, you'll see it listed in the "VPC networks" page of your console.

That's it! You now have a VPC network created on Google Cloud Platform. You can now add subnets, configure firewall rules, and connect your VPC network to other networks using VPN or interconnect.

**Launch a Linux ( Ubuntu ) VM.**

1. Log in to your GCP console and select your project.

2. Click on the "Navigation menu" button on the top-left corner of the console, and navigate to the Compute Engine section.

3. Click on "VM instances" and then click on "Create instance".

4. In the "Create an instance" page, fill in the following details:
```
Name: A name for your instance.
Region and Zone: Choose the region and zone where you want your instance to be located.
Machine type: Choose the machine type that best suits your needs.
Boot disk: Under "Boot disk", click "Change", select "Ubuntu" as the operating system, and choose the version of Ubuntu you want to use.
Firewall: Make sure "Allow HTTP traffic" and "Allow HTTPS traffic" are checked if you want to use your instance as a web server.
```
5. Once you've filled in all the necessary details, click "Create" at the bottom of the page.

6. Your instance will take a few minutes to initialize. Once it's ready, you'll see it listed in the "VM instances" page of your console.

7. That's it! You now have an Ubuntu VM running on Google Cloud Platform. You can connect to it using SSH, and you can also configure it further by installing additional software and configuring firewall rules.


## Useful Links and References

Here are some links to useful **Linux references:**

1.  Linux Documentation Project: [https://tldp.org/](https://tldp.org/)
2.  Linux man pages: [https://linux.die.net/man/](https://linux.die.net/man/)
3.  Linux Journal: [https://www.linuxjournal.com/](https://www.linuxjournal.com/)
4.  Linux Mint User Guide: [https://www.linuxmint.com/documentation.php](https://www.linuxmint.com/documentation.php)
5.  Ubuntu Documentation: [https://help.ubuntu.com/](https://help.ubuntu.com/)

These resources provide a wealth of information on various Linux-related topics, including installation, system administration, networking, programming, and more.

Here are some links to useful **Bash scripting references:**

1.  Bash Guide for Beginners: [http://tldp.org/LDP/Bash-Beginners-Guide/html/](http://tldp.org/LDP/Bash-Beginners-Guide/html/)
2.  Bash Reference Manual: [https://www.gnu.org/software/bash/manual/bash.html](https://www.gnu.org/software/bash/manual/bash.html)
3.  Advanced Bash-Scripting Guide: [http://tldp.org/LDP/abs/html/](http://tldp.org/LDP/abs/html/)
4.  Bash Scripting Tutorial for Beginners: [https://linuxconfig.org/bash-scripting-tutorial-for-beginners](https://linuxconfig.org/bash-scripting-tutorial-for-beginners)
5.  ShellCheck: [https://www.shellcheck.net/](https://www.shellcheck.net/)

These resources provide a wealth of information on various Bash scripting-related topics, including syntax, variables, control flow, functions, and more. Additionally, ShellCheck is a tool that can help you identify and fix common errors in your Bash scripts.