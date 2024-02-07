
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

## Escape Sequences

Bash recognizes special escape sequences

- $' ' the quoted string
- echo -e 
- printf %b

```
\n    newline
\t    tab
\'    single quote $'...'
\"    double quote $"..."
\?    question mark  \"air quotes\"?
\\    backslash
```

## Quoting

```
;     command separator
&     background execution
()    command grouping
|     pipe
< >   redirection
$     variable substitution
#     comment
```

- `echo 'single quote "protects" the double'`
- `echo "aren't you \"shocked\" ?"`
- echo `ls | wc -l` "files in" `pwd` | lolcat 
- `echo "the value of \$x is $x"  20 `
- `echo 'space\tand\ttime`


## Command forms

```
cmd &           execute command in background
cmd1;cmd2       run command 1 then command 2
{cmd1;cmd2;}    run commands as group in _current shell_
(cmd1;cmd2;)    run command as group in _subshell_
cmd1|cmd2       use command 1 output for command 2
cmd1 `cmd2`     command 2 output for command 1
cmd1 $(cmd2)    nesting shell command substitions
cmd1 && cmd2    execute command 1 if successful, then command 2
cmd1 || cmd2    execute either command, cmd2 never runs if cmd1 is true
```

- `cd ~/Documents; ls` _this works for Bash aliases too_
- `(date; who; pwd) > 3commands.txt`
- `sort countries.txt | grep -i "iceland" `


## redirection commands

```
cmd > file    send output of command to a file (overwrites)
cmd >> file   send output of command to a file (appends)
cmd < file    input for command from a file
cmd <> file   open file for reading and writing

cmd 2> file   send standard error to a file, output shown
cmd >& file   send output and errors to file (overwrites)
cmd &> file   * preferred method * (overwrites)
cmd &>> file  appends output adb error to file

cmd | tee file    output in terminal and append to file
cmd |& tee file   output in terminal and overwrites to file
```






## list files in directories

- folders Hash and DEFCON

- Note: ls {folderA, folderB} = error

```
ls {Hash,defcon}   
```

## rename file extension

textfile into a markdown file
```
mv secret{.txt,.md}
```










## Numbers

### print numbers 1 to 10

quickly print numbers in terminal
```
echo {1..10}
```

### print numbers by 2

increment 1 to 20 by 2
```
echo {1..20..2}
```

### print numbers with zeros

```
echo {01..10}
```





## other

- `pr -N` prints out the Nth page, used with `sort file`













## String concatenation

echo letters to string words

```
echo me{ga,dian,an} stats       # mega median mean stats
```







