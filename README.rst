B O T L
=======


**NAME**

::

    botl - BOTL


**SYNOPSIS**

::

    python3 -m botl cmd [key=val] [key==val]
    python3 -m botl.console
    python3 -m botl.daemon
    pytohn3 -m botl.service


**DESCRIPTION**

::

    BOTL has all the python3 code to program a unix cli program, such as
    disk perisistence for configuration files, event handler to
    handle the client/server connection, deferred exception handling to not
    crash on an error, a parser to parse commandline options and values, etc.

    BOTL uses object programming (OP) that allows for easy json save//load
    to/from disk of objects. It provides an "clean namespace" Object class
    that only has dunder methods, so the namespace is not cluttered with
    method names. This makes storing and reading to/from json possible.

    BOTL is Public Domain.


**INSTALL**

::

    $ pip install botl


**CONFIGURATION**


use alias botl="python3 -m botl "

irc

::

    $ botl cfg server=<server>
    $ botl cfg channel=<channel>
    $ botl cfg nick=<nick>

sasl

::

    $ botl pwd <nsvnick> <nspass>
    $ botl cfg password=<frompwd>

rss

::

    $ botl rss <url>
    $ botl dpl <url> <item1,item2>
    $ botl rem <url>
    $ botl nme <url> <name>

opml

::

    $ botl exp
    $ botl imp <filename>


**SYSTEMD**

::

    $ botl srv > botl.service
    $ sudo mv botl.service /etc/systemd/system/
    $ sudo systemctl enable botl --now

    joins #botl on localhost


**USAGE**


without any argument the bot does nothing

::

    $ botl
    $

see list of commands

::

    $ botl cmd
    cfg,cmd,dne,dpl,err,exp,imp,log,mod,mre,nme,
    pwd,rem,req,res,rss,srv,syn,tdo,thr,upt


start a console

::

    $ botl -c
    >


use -v to enable verbose

::

    $ botl -c -v
    BOTL since Tue Sep 17 04:10:08 2024
    > 


use -i to init modules

::

    $ botl -c -i
    >



start daemon

::

    $ botl -d
    $


start service

::

   $ botl -s
   <runs until ctrl-c>


**COMMANDS**

::

    here is a list of available commands

    cfg - irc configuration
    cmd - commands
    dpl - sets display items
    err - show errors
    exp - export opml (stdout)
    imp - import opml
    log - log text
    mre - display cached output
    pwd - sasl nickserv name/pass
    rem - removes a rss feed
    res - restore deleted feeds
    rss - add a feed
    srv - create service file
    syn - sync rss feeds
    tdo - add todo item
    thr - show running threads


**SOURCE**

::

    source is at https://github.com/otpcr/botl


**FILES**

::

    ~/.botl
    ~/.local/bin/botl
    ~/.local/pipx/venvs/botl/*


**AUTHOR**

::

    Bart Thate <bthate@dds.nl>


**COPYRIGHT**

::

    BOTL is Public Domain.
