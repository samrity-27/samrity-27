# shell - interface between you and the operatinng system
- Terminal basics
- `pwd` (present working directory)
- `ls` . `ll` - (list files)
- `cd` ( change directory )
- `mkdir` ( make directory)
- `rm` (remove )
- `cat` (view)
- `nano` v,m (edit)
- `cp` (copy)
- `mv` (move)
-ctrl + o = save 
- ctrl + x = exit 
- ctl + l (to clear the terminal)
- ctrl + alt+ t = to open terminal
# shell script = more than one command exicute together 
- `cal - M` , `cal - p` (calender)
# standard command ,cat + enter = keyboard 
- ctrl + d = stop standard command 
- `ls - l` (file date)
- `ls - g` - l (total)
- `ls -hal` (file size in kb mb)
- `ls - tl`
- `ls - a` for hidden files 
- `ls -ltr` (1st to last)
- `ls - Sl 9` ASCENDING ORDER , ls - Srl Descending order 
- `ls - R` (all directories)                                                                
## 13th june
- sudo = superuser(admin rights)
- apt = ubuntu package manager 
- `sudo_adduser_smriti`
- `su` - smriti
## file permissions
- chmod *user*,*group*,*others* + read4,write2,execute1`
- `chmod u + rwx`
- `./`current directory
- `echo`
# 16th june
- commands
  `type -t` check bash command type
  - path location `echo $PATH`
  - Shebang is compulsory to run file
   - #!/bin/bash
    .sh means script
 -  `which` command path
- | command | output of `type -t`|meaning
  ----------|--------------------|-------
  `cd`      |builtin             |shells internal command
  `ls`      |alias               | external command
  `pwd`     | builtin            | shells internal command
  `which`   | file               | external command
  `ll`      | alias              | external command
  `echo`    | builtin            | shells internal command
  `mv`      | file               | external command
  `rm`      | file               |    "
  `mkdir`   | builtin file       |internal command 
  `cp`      | file               | external command
  `cat`     | file               | "
  `nano`     | file               | "
  - # pipes and sorting
- `wc` word count (it counts number of lines ,words and characters)
 - `wc *.pdb` (list)
- `l *.pbd`  (line list)
  - `sort -n` (sorting)
 - `sort -nr (reverse sorting)
 - `head` display first 10 lines
 - `tail` display last 10 lines
  
