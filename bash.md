
# Bash

The commands shown are my notes of useful commands, therefore not all commands will be shown.


`bash [options] [arguments]`

execute commands from:
- terminal 
- a file
- standard input
- when `-s` 

## Command line options

- `-c str` reads command from  str

```
bash -c "echo hello"
```

- `-s` standard output

```
bash -s someFile.md
```
This started a Bash terminal shell


## Filename metacharacters

```
*        match any string of zero or more characters
?        match any single character
[abc..]  match any character inside the [ ]
~        home directory
~name    home directory of user name
```