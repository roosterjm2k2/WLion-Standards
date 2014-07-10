WLion-Standards
===============

Code Standards for White Lion for PHP_CodeSniffer

Caveats
=======

- Its a work in progress; I have most of our rules implemented, im still working on assignment alignment
- You might get some false positives; Sometimes it thinks an empty line shouldn't be ther when it should be - still working on tweaking this
- It might miss some things; again, still working on it.  Even if it doesn't catch everything, it does pretty well at this point, so its goign to save code-review time
- If you want to help make this better, let me know, I'll add you to the repo (or better, we can move this to wlion repos)


Usage - Sublime Text
====================

(If you don't already have Sublime [Package Control](https://sublime.wbond.net/installation) installed - do that first!)

The first thing you need to do is install PHP_CodeSniffer with pear: *(Make sure you're on your local machine, not dev2/3)*

```
$: pear install PHP_CodeSniffer
```

Then you need to install **SublimeLinter** and **SublimeLinter-phpcs** via Package Control

After you install both of those, open the user preferences for the SublimeLinter Package:

![User Settings Menu](menu.png?raw=true "SublimeLinter User Settings in ST3/OSX")

You will need to modify 2 properties (commented inline):

```JSON
...
        "linters": {
            "phpcs": {
                "@disable": false,
                "args": [],
                "excludes": [],
                "standard": "${home}/Desktop/WLion" /* This is where you cloned this repo */
            }
        },
        "mark_style": "outline",
        "no_column_highlights_line": false,
        "paths": {
            "linux": [],
            "osx": [
                "/usr/local/Cellar/php54/5.4.29/bin" /* This is your pear bin path */
            ],
            "windows": []
        },
...
```

Once you do this, you shouldn't need to restart ST, but I had to so you might have to as well.  




