cjsh
====

## CJSH, a Python 3 Based Experimental, Programmable Unix/Linux Command Line Shell

### TL;DR

curl http://JonathansCorner.com/cjsh/download.cgi &gt; ~/bin/cjsh &amp;&amp; chmod 0755 !#:3

### What is cjsh/CJSH?

cjsh, developed by CJSH (Christos Jonathan Seth Hayward) is an experimental
Unix/Linux command-line shell, designed to search for files for the user
instead of making the user search through directory heirarchies manually, and
allow much of the power of Python as its command-line scripting language

It can be downloaded, as in the TL;DR section above, and
can be initialized (this takes some time, but it pays off in usage), by
running:

    dev ~/directory $ cjsh --update
    Creating image of file heirarchy; please wait.
    This may take some time; it may be worth the wait (but sorry...)
    Note that the following works well in nightly crontab:

        cjsh --update --silent

    The image is complete. You are free to use cjsh.
    dev ~/directory $ cjsh
    One moment, please; trying to load data...
    Loaded.
    Welcome to cjsh. Please visit JonathansCorner.com! Hit '?' for help.
    \-\-
    user @ dev.localdomain - Tue Oct  2 17:00:43 2012
    /Users/user
    cjsh&gt; [<em>TAB</em>] for index in range(10):
    ----&gt; echo %(index)d
    ----&gt; 
    0
    1
    2
    3
    4
    5
    6
    7
    8
    9
    user @ dev.localdomain - Tue Oct  2 17:02:24 2012
    /Users/user
    cjsh&gt; 

Those echo statements are not built into the (cjsh) shell. They come from an
os.system() statement, and it is possible in this way to interleave shell
commands and Python, with Python variables accessible to the shell commands, at
least at a basic level.
