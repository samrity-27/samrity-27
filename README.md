#unix bash (bourne again shell)
- shell - interface between you and the operatinng system
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
## super user
- sudo = superuser(admin rights)
- apt = ubuntu package manager 
- `sudo_adduser_smriti`
- `su` - smriti
## file permissions
- chmod *user*,*group*,*others* + read4,write2,execute1`
- `chmod u + rwx`
- `./`current directory
- `echo`
# commands
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
-  pipe use  - grep "kiwi" fruits.txt | wc 
- `wc` word count (it counts number of lines ,words and characters)
- `sort -n` (sorting)
 - `sort -nr` (reverse sorting)
 - `head` display first 10 lines
 - `tail` display last 10 lines
 - `grep`= basic grep (used for pattern matching),
`egrep`= Extended grep
 `fgrep`= fixed grep
 `rgrep` = recursive grep 
- V, --version Output the version number of grep and exit. `grep -V`
-  -E, --extended-regexp  interpret PATTERNS as extended regular expressions (ERE)
-  -F, --fixed-strings  interpret PATTERNS as fixed strings, not regular expressions.
-  -G, --basic-regexp Interpret PATTERNS as basic regular expressions 
- P, --perl-regexp  interpret PATTERNS as Perl-compatible regular expressions (PCREs).  This option is experimental when combined with the -z (--null-data) option, and grep -P may warn of unimplemented features.
  ### common useful grep options
  | options | description |
  ----------|-------------|
  | `grep -i` | Ignore case (Apple = apple) |
  | `grep -v`  | invert match (show lines that DO NOT match) |
  | `grep -n`  | Show line numbers |
  | `grep -r/R` | recursive search |
  | `grep -c` | count match |
  | `grep -l` | show filenames with matches |
  | `grep -o` | show only matches parts of line |
  ## important symbols
  | symbol | name  |
  |--------|-------|
  ~        | tilde|
  ! |exclamation mark|
  @ |at sign |
  $ | dollar sign |
  ^ | caret       |
  * | asterisk    |
  : | colon       |
  ; | semi colon  |

  
