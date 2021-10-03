### grep(Global Regular Expression Print)

>grep --version
>
>grep Server /etc/ntp.conf
>
>grep -i Server /etc/ntp.conf # -i case insensitive

#### Search for word (Word boundary)
> grep '\bserver\b' /etc/ntp.conf

#### Search for word, start of line

> grep '^server\b' /etc/ntp.conf

#### Remove blank and commented line

> grep -ve '^#' -ve '^$' /etc/ntp.conf # -v reverse the search

### Count matches

> grep -c name /proc/cpuinfo # -c: count matches

#### Search multiple files

> grep ___username___ /etc/*

#### Print only limited lines before/after matching line

> grep -A2 <username> /etc/passwd # -A : after
>
> grep -B2 <username> /etc/passwd # -B : before
>
> grep -C2 <username> /etc/passwd # -C : after and before
