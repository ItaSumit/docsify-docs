> echo $0 - Current executing program

> ps -fp "$$" 

> ps -fp ___processId___

> ps -fp ___processId1 processId2 ..___

> The procps package contains a set of system utilities that provide system information. Procps includes ps, free, skill, pkill, pgrep, snice, tload, top, uptime, vmstat, w, watch and pdwx.

> dpkg -S $(which ps)
>
>list tool from procps
>
>command:dpkg -L procps
>red hat system: rpm -ql procps

>uptime - provides load average(1min, 5min, 15min) 
>
>output: 15:56:21 up 43 min,  1 user,  load average: 0.26, 0.26, 0.21

> cat /proc/uptime - 
>
> outputs 2 numbers, first is total number of seconds the system has been up.
The second number is how much of that time the machine has spent idle, in seconds.

> cat /proc/loadavg

#### Managing jobs - One console and many tasks

>Ctrl + z to stop long running command and send in background in stopped mode
>jobs
>
>bg
>
>fg
>
>&

#### Run job in backgroud:
>
>Command: sleep 200 &

        ps
        kill
        killall
        grep
        pkill
        pgrep
        ps -l # -l: long listing
        pf -f
        ps -l <process-id>
        ps -ef # -e: all processes
        ps -ef | grep <search-term>
        pgrep <search-term>
        pkill <search-term>
        killall <search-term>
        kill -l # -l: list all signals
        kill -<signal> <process-id>

> Default kill signal is -15, also written as -term or -sigterm
>
>To kill , -9 or -kill or -sigkill
>
>some application does not respond to -15 (terminate), so we will need to send -9(kill) signal

#### Top

>top - continue monitor all processes with %CPU info sort
>
>top -n 1 - runs one iteration and exit
>
>top -n 2 -d 3 -two iterations with 3 sec delay

##### Sections

>uptime(load info): toggle with l (small l)
>
>tasks : toggle with t
>
>memory: toggle with m
>
>By default, top information is sorted by cpu info.
>
>Change sort field:
>
>press key f (f for field)
>
>choose field with up/down arrow navigation keys
>
>press key s (s for sort)

##### Operations
>We can operate on process in top
>
>r: renice
>
>k: kill
