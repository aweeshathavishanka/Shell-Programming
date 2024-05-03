# What is Shell Script

A shell script is a program designed to be run by the Unix shell, a command-line interpreter. The various dialects of shell scripts are considered to be scripting languages. Typical operations performed by shell scripts include file manipulation, program execution, and printing text. Here’s a breakdown of what makes shell scripting notable:

## Features of Shell Scripts

1. **Automation** -
   Shell scripts allow you to automate repetitive tasks by combining multiple commands into a single script that can be executed with one command.

2. **Batch Processing** -
   Scripts can process batches of files automatically, applying the same commands or operations to each file in the batch.

3. **Environment Setup** -
   They can be used to configure a user’s environment setting automatically when they log in or start a session.

4. **System Administration:** - They are widely used in system administration for tasks like backing up data, updating systems, and managing users.
   <br>

## Components of a Shell Programing

- **Shebang (#!):** - The first line in many shell scripts which tells the system which interpreter to use to execute the script, e.g., `#!/bin/bash `for a Bash script.

- **Comments** - Begin with `#`, and provide explanations about what the script or parts of the script do.

- **Commands** - Any command that can be executed in the terminal can be included in a shell script.

- **Variables:** - Used to store information that can be used and manipulated by the script.

- **Control Structures:** - include `if` statements, loops (`for`, `while`), and case statements, which allow for branching and repetition of actions.

- **Functions** -Reusable pieces of code that can be called anywhere from the script, reducing redundancy and improving readability.

## An Example Shell Script

```bash
#!/bin/bash

# This script lists files and prints a greeting

echo "Hello, $(whoami)! Here's the list of files in your current directory:"
ls -l

```

<br>
<br>

## How to Run a Shell Script

To run a shell script from the command line:

1. **Make the script executable:** Use the command `chmod +x scriptname.sh` to make the script executable.

2. **Execute the script:** - You can execute the script by prefixing it with `./`, like `./scriptname.sh`, or by specifying the interpreter explicitly like `bash scriptname.sh` if execution permission isn’t set.

Shell scripting is a powerful tool that can greatly simplify and automate tasks on Unix and Linux systems. Its utility in automating complex sequences of tasks makes it invaluable for systems administration and repetitive file operations.
<br>
<br>
<br>
<br>
<br>

# Shell Scripting

## `cat /etc/shell`

1. `cat`:

This is a standard Unix/Linux command used to concatenate and display the contents of files to the standard output (your screen, typically). When you use cat followed by a file name, it will print the contents of that file.

2. `etc/shells` :

It lists the full paths of the shell interpreters (like Bash, Zsh, etc.) that are available and recognized by the system. This file is used by various programs to verify that a given shell is a valid login shell.

```bash
cat /etc/shells
```

## `echo $SHELL`

1. `echo`:

This is a shell command used to display a line of text/string that is passed as an argument. It's frequently used in scripting and command line operations to output the values of variables and expressions.

2. `$SHELL`

This is an environment variable in Unix-like systems that stores the path to the user's default shell. Environment variables are dynamic values which the system or other programs use to affect the way processes will behave on a computer.

When you enter echo $SHELL in a terminal and press Enter, the shell interprets this command as a request to print the value of the SHELL environment variable. The output will be the full path to the default shell that was set for the current user. For example, it might print something like /bin/bash, /bin/zsh, or another shell depending on the system configuration and user settings.

This command is particularly useful for quickly checking which shell you are currently using, especially if your system has multiple shells installed and you switch between them.

## Change working shell

1. C Shell (`csh`)

```bash
csh
```

This command will start a new C shell session. If csh is not installed on your system, you might need to install it first. On systems like Ubuntu, you can install it using `sudo apt install csh`.

2. Bourne Shell (`sh`)

To switch to the Bourne shell, which is the original Unix shell developed by Stephen Bourne, you can use:

```bash
sh

```

Note that on many modern systems,`/bin/sh`is often linked to a more modern shell like `dash `(Debian Almquist Shell) that aims to be POSIX-compliant and minimalistic, or it might be linked to `bash` in POSIX mode.<br>

3. Bash Shell(`shell`)

This will start a new Bash session. Bash is the default shell on many Linux distributions and comes with many features conducive to interactive use and scripting.

### Additional Info

- **Temporary vs. Permanent Change:** Running these commands only changes the shell for the duration of the current terminal session. Once you close the terminal, your shell will revert to whatever is configured as the default for your user account.

- **Changing the Default Shell:** If you want to change your default shell permanently, you can use the`chsh`(change shell) command:

```bash
chsh -s /path/to/new/shell
```

For example, to change to Bash permanently, you would run:

```bash
chsh -s /bin/bash
```

You will need to log out and log back in for the change to take effect.

- **Checking Your Current Shell:** If you are unsure which shell you're currently using, you can use the `echo $0 `or `echo $SHELL`commands. `echo $0` often shows the shell being used for the current session, while `echo $SHELL` shows the default shell set for your user.

## change back to previous shell

If you've switched to a different shell during a terminal session and want to return to the shell you were using previously, there are a couple of straightforward ways to do this, depending on your situation:

### If You're Using Subshells

If you've entered a new shell by simply typing the name of the shell (like` bash`, `csh`, or `sh`) at the command prompt, you're essentially starting a subshell on top of your original shell. To return to your original shell:

- Type `exit` or press `Ctrl-D`: This will close the current subshell and bring you back to the shell from which you started the new shell. `exit` terminates the current session, and `Ctrl-D` sends an EOF (End-of-File) to the terminal, which also causes the current shell to exit if there are no running jobs.

### If You Logged In Again

If you used the `chsh`command to permanently change your shell and then logged out and back in, you'd need to change your login shell back:

- **Use `chsh` again:** You can run the `chsh -s /path/to/original/shell` command to set your shell back to the original. For example, if your original shell was Bash, you would run:

```bash
chsh -s /bin/bash
```

### Using a Simple Command (Temporary)

For a temporary change, just type the name of your original shell at the command prompt. If you were using Bash originally, just type:

```bash
bash
```

This method only affects the current terminal session and reverts back once the terminal is closed.

### Remember:

- **Temporary Changes:** Using the shell name directly (like `bash` or `sh`) only affects the current session or the current terminal window/tab.
- **Permanent Changes:** Using `chsh` affects all future terminal sessions and requires logging out and back in.

<br>
<br>
<br>
<br>
<br>

## What is Shell Script?

- A command<br>

  - Utilities coming with OS<br>
  - Is used to do a particular task

- A programe<br>
  - Sequence of commands called as shell script<br>
  - Can be read/write by a text editor
  - Can be developed by using programming techniques
