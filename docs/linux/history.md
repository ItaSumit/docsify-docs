#### History
> Command history persisted in file ~/.bash_history

#### Repeat last command: 
>
>esc+.

#### Repeat last command with first letter search !___letter___

>ex: !v # executes last vim command
!n # executes last nano command

#### Repeat last command's last argument

>!$

#### Executes last command which contains etc anywhere

>!?etc

#### Search command from history
> Ctrl + r

#### Write history to ~/.bash_history, system does it automatically when we logout
>history -a 

Repeat last command with number in history
>!___number___

#### Control history with variable HISTCONTROL

>HISTCONTROL=erasedups

#### Clear history

> history -c

#### Read history from ~/.bash_history file
> history -r

#### Append history
> history -w