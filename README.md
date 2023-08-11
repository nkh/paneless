# NAME

	paneless - multipane pager

![GUI](https://github.com/nkh/paneless/blob/main/media/paneless.png)

# SYNOPSIS

	paneless [-t -a -l -L] file <(seq 5) file ...

# DESCRIPTION

***paneless*** reads its input stream from its arguments (no piping), format them to fit the terminal, and colors them.

Processing multiple large inputs may take time to process, so does input that contains ANSI color codes. 

Once processed vertical scrolling is fast; horizontal scrolling re-processes all the inputs.

## Options

| short      | long          | function                                         |
| ---------- | ------------- | ------------------------------------------------ |
| -a         | --ansi        | input contains ANSI color code                   |
| -c file    | --custom=file | add custom commands                              |
| -e="k=v"   |               | store option for custom commands                 |
| -l         | --line-number | overlay the top line number                      |
| -L         |               | overlay the bottom line number                   |
|            | --no-color    | do not color text                                |
|            | --status-line | reserve space for status line                    |
| -t=tabsize |               | set tab size (8 default)                         |
| -h         | --help        | display help                                     |

## Bindings

| binding | function                       |
| ------- | ------------------------------ |
| q       | quit                           |
| Q       | quit leaving the panes visible |
| c       | show command bindings          |
| r       | refresh                        |
| R       | reload                         |
| CTL-B   | page down                      |
| PGUP    | page down                      |
| SPACE   | page up                        |
| PGDN    | page up                        |
| CTL-F   | page up                        |
| j       | scroll down                    |
| k       | scroll up                      |
| DOWN    | scroll down                    |
| UP      | scroll up                      |
| gg      | go to the first line           |
| G       | go to the last line            |
| l       | move right                     |
| RIGHT   | move right                     |
| h       | move left                      |
| LEFT    | move left                      |
| /       | searn                          |
| n       | find next                      |
| N       | find previous                  |
| gff     | fzf find                       |
| b       | fzf find                       |
| zl      | flip line number overlay       |
| zt      | flip line total display        |

# DEPENDENCIES

- Bash
- Perl
	- Text::ANSI::WideUtil (required for input with ANSI colors codes) 
- FZF

# INSTALL

Clone the repository and add it to your PATH; or link/copy the files to somewhere in your PATH.

# CONFIGURATION

The *paneless* file you run contains the configuration and bindings (press 'c' to see the bindings in FZF).

You can change the color used by *paneless* as well as the bindings (vim-like by default).

# AUTHORS

    Khemir Nadim ibn Hamouda
    https://github.com/nkh
    CPAN ID: NKH
    
# LICENCE

	© Nadim Khemir 2023, Artistic licence 2.0
