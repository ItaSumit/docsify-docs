#### .vmrc

>Systemwide:
>
>/etc/vimrc

>Personal config:
>
>~/.vimrc

>set bg=dark
>
>abbr _sh !#/bin/sh
>
>abbr _bash #!/bin/bash<CR>
>   
>nmap <C-N> : set invnumber<CR> # Ctrl+N : toggle line number
>
>nmap <CR> G  # enter: last line, 10+enter: line 10, 1+enter : line 1
>
>set number nohlsearch showmode 
>
>set bg=dark ai tabstop=2 expandtab

#### Modes

>Command
>
>Insert/Edit - Enyter with pressing key "i"
>
>Last line - Enter from command mode using :

#### Quit

| Key | Description |
| --- | --- |
| q | |
| q! | without making any changes |
| wq | write and quite |
| x | same as wq |
| w | Save changes |

#### Insert
| Key | Description |
| --- | --- |
|i | insert before at cursor position |
|I | insert in begining of current line |
|a | Append to current position |
|A | Append to the end of current line |
|o | insert new line below current line |
|O | insert new line below above line |
|x | delete current charater |
|dw | delete whole word |
|u | undo |
|3dw | delete 3 words |
|3x | delete 3 chars |

#### Navigation

| Key | Description |
| --- | --- |
|G | End of file |
|1G or gg | First line |
|7G or 7gg | go to line 7 |
|w and b | Move forward/backword one word |
|5w , 5b |  Move forward/backword 5 words |
|$ | End of line |
|^ | start of line |
|vi +127 filename | Direct goes to line 127 |
|vi +/sometex filename | Direct goes to first occurance of sometext |
|set number | line numbers |
|set invnumber | toggle line number |
|set nonumber | remove line niumber |
|set nohlsearch | remove searh highlight |

#### Read into vim

> Read file or command output in to current file
>
> file - last line mode then r file.txt
>
> command - last line mode then r! command

#### Write to another file
> last line mode then 
>
>w out.txt
>
>Range of line to write
>
>23,37w out.txt

#### Search and Replace

> %-  specify whole document
> range 103,199 - specify range of document
>
>e.g.
>
>%s/Inc/Ltd/
>
>9,14s/Ltd/Inc/
>
>Indent lines
>
>9,14s/^/^I^I/
>
>press key 'n' to go to next occurance

#### Indent miultiple lines
>number of lines + >>
>
>number of lines + <<

#### Shortcuts

| Key | Description | Example |
| --- | --- | --- |
| O | Insert line after |
| esc + :x | Save and exit |
| I | Moves editing cursor in beginig of line. Edit line, Press Esc. Change line, press "." key. It will repeat same editing as before. |
| number_of_line followed by dd | Cut/Delete paste multiple line | 4dd |
| number_of_lines followed by yy | yank(copy) all the lines , paste with "p"| 4yy |

