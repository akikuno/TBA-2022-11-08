# Shell 101

## What is Shell?

Shell is an environment in which we can run our **commands**.

## Grammar

The first word is the **command** to be executed, and the remaining words are arguments to the command.

For example,

```bash
echo TBA
# -> TBA
```

is a simple command (`echo`) with an argument (`TBA`).

## Pipeline `|`

A **pipeline** is a sequence of two or more commands where each command is separated from the next by ‘**|**’. Where commands are separated by ‘**|**’, the standard output of the first command is connected to the standard input of the next.

For example,

```bash
echo TBA | sed 's/TBA/Tsukuba Bioinfo Assembly/'
# -> Tsukuba Bioinfo Assembly
```

is a pipeline, where the output ‘TBA’ of the first command will be passed to the input of the second.

## Redirection `>`

The output from a command can be easily diverted to a file.

If the notation `>` file is appended to any command that normally writes its output to standard output, the output of that command will be written to file instead of your terminal.

This is known as **redirection**.

Check the following command which redirects the output of the command in the TBA.txt.

```bash
echo TBA > TBA.txt
```

### References

- https://zsh.sourceforge.io/Doc/Release/Shell-Grammar.html
- https://www.tutorialspoint.com/unix/unix-io-redirections.htm

(2022-10-23 accessed)
