basic bash meta for non programmer friend

* meta
    * `man` generates a system manual page for a command that is its own executable (almost all of them)
        * `man python`
    * `-h` is a flag for help, which many programs implement (but it's up to them)
    * `!a` run last command you ran beginning with a
        * can be longer also `!python`
        * doesn't last between sessions (cleanly)
    * everything listed in here pretty much has flags, you can read more on them if they interest you
* structure
    * many commands accept flags, which are generally in the form of `-f` or `--long-flag`
        * but this is just a conventional standard, some programs will accept `f` or `-long-flag`
        * read the manual/docs/whatever
        * `command -f --long-flag`
        * sometimes you will find flags which take arguments, which again may vary slightly in format
        * commonly `command -f Argument --long-flag=LongArgument` 
    * programs have:
        * input stream
        * output stream
        * error stream
    * by default both output and error are often "print to the shell", but they're separate
    * `q` will stop most programs which take over the screen entirely (e.g. `top`)
    * ctrl-c will force stop basically everything else
        ~~there are some exceptions lmao type `vi` and see what happens~~
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
        * `command > /dev/null` redirects output nowhere (so it runs silently unless it prints errors)
    * `>>` output of a command -> a file (doesn't blank the file)
        * `python leethax.py >> weekly_log.txt`
        * you can suppress the errors too but you probably shouldn't need to do that, you can look it up
* process management
    * `&` run in background
        * means it doesn't lock up your input, but it will still produce output at the same time, which may be disruptive to your attempts at input
        * `sleep 300 &`
        * it can't accept input either at this time 
        * including ctrl-c and others
    * `fg` move background to foreground
        * it accepts input again
    * ctrl-z pause the current program, it is treated as being in the background and will restart when moved to the foreground
        * or `bg` unpause, run in background
    * `top` interactive task manager
    * `ps` non-interactively, task lists
        * `ps` everything in *your* terminal
        * `ps a` everything in *a* terminal
        * `ps x` everything else
        * `ps u` list with more info
        * these can be combined, and there are other flags
        * with `x`, will give you too much to sort through manually
* files
    * `file` gives you a file type
        * `file suspiciousinternetmedia.exe.wtf`
    * `less` interactively scroll through a text file
    * `head` view the first (by default) 10 lines of a text file
    * `find` list anything matching a name in a folder and all its subfolders, *with full path names*
        * `find .` every file in the current folder and its subfolders
        * `find images/REDACTED` every file in the folder images/REDACTED



### see also actual comprehensive references etc

* https://devhints.io/bash
* https://github.com/jlevy/the-art-of-command-line