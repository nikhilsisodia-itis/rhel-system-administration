# IO Redirection and Piping

## Input and Output Redirection

- Redirection allows you to change the standard input (stdin), standard output (stdout), and standard error (stderr) of commands.
- The symbols used for redirection are:
  - `>` : Redirects stdout to a file, overwriting the file if it exists.
  - `>>` : Redirects stdout to a file, appending to the file if it exists.
  - `<` : Redirects stdin from a file.
  - `2>` : Redirects stderr to a file, overwriting the file if it exists.
  - `2>>` : Redirects stderr to a file, appending to the file if it exists.
  - `&>` : Redirects both stdout and stderr to a file, overwriting the file if it exists.
  - `&>>` : Redirects both stdout and stderr to a file, appending to the file if it exists.
- Examples

```bash
# Redirect stdout to a file
echo "Hello, World!" > output.txt
# Append stdout to a file
echo "Hello again!" >> output.txt
# Redirect stderr to a file
ls non_existent_file 2> error.txt
# Redirect both stdout and stderr to a file
ls existing_file non_existent_file &> all_output.txt
```

## Piping

- Piping allows you to take the output of one command and use it as the input to another command.
- The pipe symbol `|` is used to create a pipeline between commands.
- Examples

```bash
# Use grep to filter the output of ls command
ls -la | grep Downloads
```
