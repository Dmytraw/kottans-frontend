###What i learned about Command Line Interface (CLI)
1) `ls` - LiSt files in dir
2) `root` stands for directory which is the parent of all other directories
3) `pwd` - `p`rint `w`orking `d`irectory - see where i am lokated via cli
4) `cd` - `c`hange `d`irectory - change location to another directory
5) `mkdir` - `m`a`k`e `dir`ectory - create a new empty directory
6) `touch` - create a file inside directory
7) `&&` - for chaning few commands (e.g.: `mkdir mydir && cd mydir && touch myfile.css`)
8) `-a` - option for `ls` which shows `a`ll files incl. hidden
9) `-t` - option for `ls` helps to print the results of `ls` sorted by time of modification
10) `-l` - option for `ls` print the results in long format
11) `ls -l` displays results in a table of 7 columns:

    1) Access rights (what actions could be performed by current user on this directory - read/write/delete etc)
    2) Number of chuld directories and files
    3) Username of fileowner
    4) The name of group
    5) Size of file in bytes
    6) The date and time when the file was modified
    7) Name of file or dir

12) `cp file1 file2` - `c`o`p`y contents of `file1` into `file2`. Might also copy directories or multiple files in directories like `cp dir1/file1 dir1/file2 dir2` (copies `file1` and `file2` from `dir1` into `dir2`)
13) `cp * dir` - copies every file from current directory to a directory `dir`
14) `cp m*.txt dir` - copies every file with `txt` extension and starts with `m` to a directory `dir`
15) `mv` - like `cp` but works like `cmd+x` && `cmd+v`
16) `rm` - `r`e`m`ove file/directory
17) `-r` option for `rm` command removes all subdirs of directory we are removing
18) `>` - redirect - puts stdinput in ceratin file `echo 'Hello' > file.txt`
19) `cat` - a command that shows contents of the file
20) `>` overwrites, `>>` merges
21) `cat lakes.txt | sort > sorted-lakes.txt` - take contents of `lakes.txt` then sort it and store it file `sorted-lakes.txt`
22) `sort deserts.txt | uniq` - leave only unique lines in the file
23) `grep` - command designed to search through file lines by regular expression(`g`lobal `r`egular `e`xpression `p`rint). 
    - `grep <regex> <file to search>`
    - `grep <regex> -R <directory to search>` - display files and lines with match
    - `grep <regex> -Rl <directory to search>` - only files with match
24) `sed` - `s`tream `ed`itor - edit files via cli. 
    - `sed 's/text_to_find/text_to_replace_found_text_with' file_to_perform_changes`
25) `~` stands for home folder
25) `.bash_profile` is a system file which is responsible for environmental settings. `source ~/.bash_profile` activates it
26) `alias`es are time saviours
27) `export PS1='ξ '` will change default value of the terminal symbol
28) `env` return the list of environmental variables
