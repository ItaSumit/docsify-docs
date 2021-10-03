> readlink ___linkedfile___

> ls -ld <dirname>/ # -d: list directories themselves, not their contents

> ls -F <dirname> # -F : append indicator (one of */=>@|) to entries

> ls --color=auto <dirname>

> alias: ls='ls --color=auto'

#### Execute ls command without using alias:
> command: \ls

> Directory has always minimum 2 links. One is actual name and secons is '.' inside itself

> ls -t <dirname> # -t: sort by last modified time
>
> ls -l <dirname> # -l: long listing
>
>ls -tr <dirname> # -t: sort by last modified time, -r: reverse

> ls -lrt /etc | less
