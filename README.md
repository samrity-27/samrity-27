# Unix Bash (Bourne Again Shell)
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
# Shell script = more than one command exicute together 
- `cal - M` , `cal - p` (calender)
# Standard command ,cat + enter = keyboard 
- ctrl + d = stop standard command 
- `ls - l` (file date)
- `ls - g` - l (total)
- `ls -hal` (file size in kb mb)
- `ls - tl`
- `ls - a` for hidden files 
- `ls -ltr` (1st to last)
- `ls - Sl 9` ASCENDING ORDER , ls - Srl Descending order 
- `ls - R` (all directories)                                                                
## Super user
- sudo = superuser(admin rights)
- apt = ubuntu package manager 
- `sudo_adduser_smriti`
- `su` - smriti
## File permissions
- chmod *user*,*group*,*others* + read4,write2,execute1`
- `chmod u + rwx`
- `./`current directory
- `echo`
# Commands
- commands
  `type -t` check bash command type
  - path location `echo $PATH`
  - Shebang is compulsory to run file
   - #!/bin/bash
    .sh means script
 -  `which` command path
- | Command | Output of `type -t`|Meaning
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
  - # Pipes and Sorting
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
  ### Common useful grep options
  | Options | Description |
  ----------|-------------|
  | `grep -i` | Ignore case (Apple = apple) |
  | `grep -v`  | invert match (show lines that DO NOT match) |
  | `grep -n`  | Show line numbers |
  | `grep -r/R` | recursive search |
  | `grep -c` | count match |
  | `grep -l` | show filenames with matches |
  | `grep -o` | show only matches parts of line |
  ## Important Symbols
  | Symbol | Name  |
  |--------|-------|
  ~        | tilde|
  ! |exclamation mark|
  @ |at sign |
  $ | dollar sign |
  ^ | caret       |
   *| asterisk    |
  :| colon       |
  ;| semi colon  |
# How to install Ubuntu in Window 
- Enable WSL (window subsystem for linux) `wsl --install`
- if wsl is already installed we can use ubuntu manually using 'wsl --install -d Ubuntu'
- enable windows subsystem for Linux
# Permission File 
 - `chmod +x folder` (give run permission to file or directory) , r - to read file , w - to edit file , x - to run file 
# Bash script example
#!/bin/bash (shebang)
`echo "Hello Smriti"`
# SRA (sequence reader archive)
- SRA is a NCBI's (National Centre for Biotechnology information) repository where thay store raw sequencing data (mostly next generation sequencing data like illumina,PacBio)
  - # SRA Toolkit  is used to download SRA files and can convert these files into FASTQ format 
- To download SRA toolkit use command 
`sudo apt-get install sra-toolkit`
or we can manually install it from NCBI site  , To check download use command  `vdb-dump --version`
# Download SRA file 
use command `prefetch SRR12345678`
- convert SRA file into FASTQ 
use command `fastq-dump SRR12345678` For Paired End data
- use `fastq-dump --split-files SRR12345678` to check FASTQ file use `head SRR12345678_1.fastq`
# Download FASTQC Program 
- FastQC is a quality control tool used to check the quality of raw sequence data from high-throughput sequencing platforms (like Illumina).
It reads FASTQ files and gives a report that helps you decide:
Is your data good enough to use?
Are there any problems or biases in the sequences?
Do you need to trim or filter the data?
- use bash command `sudo apt update` `sudo apt install fastqc`
- `unizip fastqc o.1zip`
- 'cd fastqc'
- 'chmod +x fastqc'
- Run the file `./`
- command `explorer.exe .` used to open current linux folder into window 
- # FASTQC FILE
- When you run FastQC on a FASTQ file, it generates two important files for each input:
- 1. filename_fastqc.html
This is a visual report.
You can open it in a browser.
It shows graphs and summaries about the sequence quality, GC content, duplicates, overrepresented sequences, etc.
- 2. filename_fastqc.zip
This contains the raw data and graphs behind the HTML report.
It includes a folder with a text file named fastqc_data.txt, which gives detailed scores and stats for each analysis module.
# FASTP Program 
- FASTP is a ultra-fast all in one FASTQ preprocessor tool which is used for the quality control and filtering mostly next generation sequences to clean and assess them
- it perform many tasks like Adapter trimming , Quality filtering , Per base quality cutting , Length filtering , and Output reports
- # FASTP Download Steps
- conda must be installed 
- use command `apt install fastp`
- 'chmod +x fastp'
#  Commands used to filter error from raw file
- write script
#!/usr/bin/bash
- write path /user/bin/fastp
-  `fastp -i R1 12345_ -o SSR..clean_.fastq  I R2 12344_ O SSR..Clean _.fastq`
-  'which' command is used to know the file path
-  command to remove more than 1 file altogether use common name and last name
-  `rm*_clean_*_fastq.zip`
-  to run file = `./fastp.sh`
# K-mer counting using jellyfish tool
- jellyfish is a k-mer counter , jellyfish takes all reads (clean reads),breaks them into k-mers,and counts how many times each k-mer occurs.
- generates a histogram (frequency vs. number of k-mers)
- this histogram is then used by genomescope 
- 1 k-mers : short DNA sequence of length , k = number of nucleotide (A,T,G,C) , mer = parts
- commands to install jelly fish `sudo apt update` then `sudo apt install jellyfish` to check install `jellyfishh --version`
 # Counts k-mers from FASTQ File
- 1 `jellyfish count -C -m 21 -s 100m -t 8 -o mer_counts.jf Filename.Fastq`
- 2 create k-mer frequency Histogram `jellyfish histo -t8 mer_counts,jf>mer_counts.histo`
 | Words | Meaning |
 | ------ | -------|
 | C      | count k-mers |
 | m      | size of k-mers |
 | s      | Hash size |
 | t8     | threads(pc based) |
 | o      | output file|
 | clean FASTQ | clean file
 | Histo  | convert binary .jf into Histogram |
 | t8     | number of threads |
 |  mer_count_hist | Redirect output into a file |  
  # Generate Histogram File using k-mer counts
  - `jellyfish histo -t 8 mer_counts1.jf >mer_counts.histo`
# Genomescope   Tool
- input = The k-mer Histogram from jellyfish
- also specify = k-mer size , Read type , Genome ploidy 
    
