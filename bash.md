<p style="text-align:center;"><img title="a title" alt="Alt text" src="/bash-resources/bash-logo-small.png"></p?>

# Bash & Shell Scripting

*Please Note : Though this repository has been created considering users of all levels (beginners, intermediate and experts) , but it is recommended that before using the repo , you should complete a docker course offered by pluralsight which is available to all LGB employees. The course will provide all the required and idepth knowledge about docker and should be supplemented by hands On labs supplied as part of this repo.*

**Here is the course link and description -- >   <<Link to be added>>**


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


# Bash and Shell Scripting - let's the the basics right

Bash is a specific type of shell, and shell scripting refers to the practice of writing scripts that run on a shell. So in a sense, **Bash is a subset of shell scripting.**

The term "shell" refers to a command-line interface that allows users to interact with an operating system by running commands. A shell can interpret and execute scripts written in a specific language, such as Bash, zsh, or csh. These scripts can be used to automate tasks, configure the operating system, or perform system maintenance.

Bash is a popular shell that is widely used in Unix-based operating systems such as Linux and macOS. It is a powerful and versatile shell that supports many advanced features, such as variables, conditionals, loops, functions, and pipelines. Bash scripts can be used for a wide range of tasks, from simple file operations to complex system administration tasks.

Shell scripting, on the other hand, refers to the practice of writing scripts that run on a shell. Shell scripts can be written in various languages, such as Bash, zsh, csh, and others. They can be used to automate repetitive tasks, perform system maintenance, configure the operating system, or build complex applications.

In summary, Bash is a specific type of shell that is widely used in Unix-based operating systems, and shell scripting refers to the practice of writing scripts that run on a shell. While Bash is a popular choice for shell scripting, other shells can also be used, and scripts can be written in various languages.  


**To write and run a Bash script, follow these steps:**

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


**Here are some Bash challenges to get you started :**


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
