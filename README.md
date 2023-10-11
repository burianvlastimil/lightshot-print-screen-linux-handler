[![Download the latest version](https://img.shields.io/badge/Download-Latest%20version-orange)](https://github.com/burianvlastimil/lightshot-print-screen-linux-handler/releases/latest) &nbsp; &nbsp; &nbsp; &nbsp; [![Donate via PayPal](https://img.shields.io/badge/Donate%20%24-via%20PayPal-%23013088)](https://github.com/burianvlastimil/lightshot-print-screen-linux-handler#donations) &nbsp; &nbsp; &nbsp; &nbsp; [![GPLv3 License](https://img.shields.io/badge/License-GPLv3-blue.svg)](https://github.com/burianvlastimil/lightshot-print-screen-linux-handler/blob/master/LICENSE) &nbsp; &nbsp; &nbsp; &nbsp; [![ShellCheck Passing](https://img.shields.io/badge/ShellCheck-Passing-brightgreen)](https://github.com/burianvlastimil/lightshot-print-screen-linux-handler)

***

# Lightshot print screen Linux handler

This script handles global print screen key strokes for you to fully enjoy [Lightshot screenshot tool](https://app.prntscr.com/en/) (home page) on any Linux.

It is a standard [POSIX](https://en.wikipedia.org/wiki/POSIX) (wiki) shell script, it should work in any [Linux](https://en.wikipedia.org/wiki/Linux) (wiki) distribution (more precisely, your [shell](https://en.wikipedia.org/wiki/Unix_shell) (wiki)).

## What the script does NOT

- It does not download Lightshot for you.
- It does not install Lightshot for you.
- It does not launch Lightshot for you! This is very important.

## What the script does actually

This script's sole purpose is to simulate (send) hotkey to Lightshot, be it Print, Control + Print, or anything else completely.

***

## Requirements

- One necessary command-line tool to have manually installed (same package name):
	- [`xdotool`](http://manpages.ubuntu.com/manpages/focal/man1/xdotool.1.html) (Ubuntu man page): In Ubuntu the package is in the _universe_ part of official archive.

- One more necessary package which should be pre-installed on most [distributions](https://en.wikipedia.org/wiki/Linux_distribution) (wiki):
	- `procps` containing [`pgrep`](https://linux.die.net/man/1/pgrep) (man page): In Ubuntu the package is in the _main_ part of official archive.

- [X Window System](https://en.wikipedia.org/wiki/X_Window_System) (wiki), with any [desktop environment](https://en.wikipedia.org/wiki/Desktop_environment) (wiki).

- [Lightshot](https://app.prntscr.com/en/wine-lightshot.html) (installation info page) properly installed into [Wine](https://www.winehq.org/) (home page).

***

## Usage instructions

### Download and Preparation

Visit the [latest release download page](https://github.com/burianvlastimil/lightshot-print-screen-linux-handler/releases/latest) (direct link). If you download the file `lightshot_print_screen`, you will need to open your terminal and give it **permission to read and execute** to all users with:

```
chmod 755 lightshot_print_screen
```

Note, that you will be able to avoid this step of changing permissions if you download the source code or clone the repository, however I advise to download that single file directly as you will not have to remove anything afterward.

### General

Now you need to place it somewhere, e.g. to your home directory inside `~/bin`, and put a path to it e.g. in Linux Mint 20 Cinnamon to the:

**Keyboard** → **Shortcuts** → **Custom Shortcuts** → click on button named **Add custom shortcut** and fill the form out.

### Command-line interface

Let me just point out, that there are many error checks along the whole script, so I advise you to run it within your terminal while your Lightshot is running to possibly debug any and all misbehaviors.

There is also the help switch (not `--help`):

```
./lightshot-print-screen -h
```

which will point out the possibility for you to feed the key combination you have configured in your Lightshot interface without ever editing the script:

```
Script  : Lightshot print screen Linux handler
Version : 6.0 (final)
GitHub  : https://git.io/fx2US
--------------------------------------------------------------------
Description: This script works with XDOTOOL to trigger Print Screen
key combination in Lightshot application installed on Linux in Wine.
License: GPL 3.0. The code itself can be further enhanced by others.
The script, however, won't launch Lightshot for you due to variable
installation locations which make it impossible. You need to run it!
--------------------------------------------------------------------
Usage in terminal: ./lightshot_print_screen [-k "HotKey"]

    -k 'HotKey': Optional switch requiring one argument,
        which is the print screen hotkey combination.
        For the left Control key and the Print Screen key
        that would be 'Control_L+Print' (as an example).

    -h: Show this help.

Usage in desktop environment:

    You need to find Keyboard shortcuts, and re-map Print to run
    this script, an example from Linux Mint is placed on GitHub.
```

### Graphical interface

There is none. This script however launches the Lightshot print screen editor directly.

***

## Screenshot from Linux Mint 20 Cinnamon

![Screenshot from Linux Mint 20](https://www.vlastimilburian.cz/github_images/lightshot-linux-mint-20.png)

***

## Reporting bugs and suggestions

Please open a [new issue ticket](https://github.com/burianvlastimil/lightshot-print-screen-linux-handler/issues/new) (direct link) or you can also mail me at [info@vlastimilburian.cz](mailto:info@vlastimilburian.cz) (email link).

***

## Donations

### Donate via PayPal

Donations are possible via my PayPal account issued on the same email address as mentioned above.

### Donate via Bank

If, for any reason, you cannot use PayPal, my bank account number is:

**Czech** (National Bank Account Number):
```
4423481043/0800
```

**IBAN** (International Bank Account Number):
```
CZ16 0800 0000 0044 2348 1043
```

**BIC/SWIFT** (Business Identifier Code):
```
GIBACZPX
```
