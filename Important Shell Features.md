# Important shell features

1. Command execution
2. Filename substitution
3. I/O Redirection
4. Pipes Mechanism
5. Subshell
6. Variables

### 1. Command Execution

This is the primary function of any shell. It interprets user input and executes commands. Commands can be anything from built-in shell commands, such as `cd` for changing directories, to system commands like `ls` to list directory contents, or even scripts and programs installed on the system. The shell looks up these commands in the directories listed in the `PATH` environment variable and executes them.

### 3. Filename Substitution (also known as Globbing):

Shells can interpret wildcards (such as `* `and `?`), which are used to match filenames. For example, `*.txt` refers to all files in the current directory with a `.txt` extension. This feature allows users to specify multiple files without typing all their names. The shell automatically expands these patterns to the applicable filenames before executing a command.

### 3. I/O Redirection:

Input and output (I/O) redirection allows users to redirect the input to and output from commands to files, or even from one command to another. For example:

- `>` redirects the output of a command to a file, overwriting the existing content (`e.g., ls > filelist.txt`).

- `>>` appends the output of a command to the end of a file (e.g., `echo "Hello" >> greetings.txt`).

- `<` redirects input from a file to a command (e.g., `sort < unsorted.txt`).

### 4. Pipes Mechanism:

A pipe (`|`) allows the output of one command to be used as the input to another command. This is a powerful feature for chaining commands together to perform complex data processing tasks. For example, `cat file.txt | grep "searchstring" | sort` uses `cat` to read the contents of `file.txt`, `grep` to filter those contents, and sort to `sort` the result.

### 5. Subshell

A subshell is a child shell that is created from a parent shell. It inherits a copy of all the environment variables from the parent but can operate independently. Changes made in the subshell, such as setting variables or changing directories, do not affect the parent shell. Subshells are often created implicitly by parentheses: (`cd some_directory; ls`) will change the directory and list its contents without affecting the current directory of the parent shell.

### 6.Variables

Variables in a shell can store data that can be used later. These can be environment variables, which are inherited by all child processes and typically used to configure the system environment, or they can be local variables, which are used within scripts or during the session. Variables can be created and manipulated directly within the shell (`VAR="value"` sets `VAR` to `"value"`), and their values can be retrieved using the `$ `prefix (e.g.,` echo $VAR`).
