# analyseModxPerf
get Modx time spent in snippet, chunk and in processing tags
# How it works
It adds some hack code in two files where are parsed snippets, chunks and tags :
* modparser.class.php
* modx.class.php

# How to install

See your Modx Version.

If you've got the one given at chapter "Modx Versions compliance", you can replace the files in your modx directory with the ones provided here.

If not, do a diff between the files and add the code that is indicated with a "hack starts":

```php
/**
         * hack #2 starts
         */
```
and closed with a "hack ends".

```php
        /**
         * hack #2 ends
         */
```

# How to use

The hack code is activated through Settings variables that need to be created:
* parser_timer - set to 1 to activate the timers
* parser_print - set the output format 

The results after parse are logged in ```'core/cache/logs/parser_timer/*.log'```


# Modx Versions compliance
* version 2.7.1

# Credits

These modifications are totally inspired from this blog article from https://web.archive.org/web/20180601065954/http://www.virtudraft.com/blog/unofficial-parser-timer-for-modx-revolution.html by  Novriko P. Parhusip in  Nov 07, 2014
