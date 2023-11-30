

* meta
    * `man` generates a system manual page for a command that is its own executable (almost all of them)
        * `man python`
    * `help` generates a system manual page for a builtin command (you may not need this often, but it's good to try)
        * `help ls`
* structure
    * programs have:
        * input stream
        * output stream
        * error stream
    * by default both output and error are often "print to the shell", but they're separate
* globs
    * `*.txt` matches anything which ends with .txt
        * `ls *.txt` does what you would hope it would do
    * `file_00*_REVISED` will match file_001_REVISED, file_007_REVISED, and even file_00THISISNOTINTHELIST_REVISED
    * there are more features of globs which you can look into if you find them useful
* redirection
    * `|` output of one command -> input of another command
        *  `ps aux | grep wizard`
    * `>` output of a command -> a file (blanks the file)
        *  `python leethax.py > result.txt`
    * `>>` output of a command -> a file (doesn't blank the file)
        * `python leethax.py >> weekly_log.txt`
* process management
    * 


### see also actual comprehensive references etc

* https://devhints.io/bash
* https://github.com/jlevy/the-art-of-command-line