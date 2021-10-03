#### Redirections

>       >  write to file
>
>       >> append to file

> set -o noclobber NoClobber
>
>       >| iglore noclobber
>
>       < read from file

> when we do not care about output of command:
>
>ls /invaliddir > /dev/null 2>&1 

#### Pipelines

> | unnamed pipes
>
> mfinfo - Named pipe

#### Redirecting standard output 

        ls /etc > file1.txt
        ls /etc 1> file1.txt
        ls /etc >> file1.txt

#### Readirecting standard error

        ls /etc 2>> file1.txt
        ls /etc 2>> file1.txt
        ls /etc > file1.txt 2>&1

#### NoClobber

> Prevents overwriting existing files
>
> set -o noclobber
>
>Override safely
>
>ls /etc >| file1.txt

#### Read from file
>df -h > diskfree.txt
>
>mail root -s "Free Disk Space" < diskfree.txt

#### Pipes

> Sends outout of one command to input of another command
>
> ls -l | wc -l

#### Named pipes (Inter-Process communications)
        mkfifo mypipe
        Process1 : ls -l > mypipe
        Process2:  wc-l < mypipe

> ls -l testnamespipe
>
>output: prw-rw-r-- 1 sumit sumit 0 Jun 27 15:07         testnamespipe
>
> notice p in begining of above line 

>ls -F testnamespipe
>
>output: testnamespipe|
>
>notice | in end of above line

#### tee

>Sends output to file AND to the screen at same time
>
>wc -l file1.txt | tee file2.txt



