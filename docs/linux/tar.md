#### Tar (Uncompressed tar)

        command: tar -cvf etc.tar /etc 

        -v: verbose
        -c: create
        -f: filename

        command: ls -lh etc.tar

        command: du -sh /etc
        command: du -sh etc.tar

        Notice the size returned from above du commands

        -s: summery
        -h: human readable

#### Tar with gzip (Compressed tar)

> tar -cvfz etc.tgz /etc

#### Tar with bzip2

> tar -cjvf etc.tar.bz2 /etc

#### Check size summary

> Command:ls -lh etc*
>
> Command: file etc*

#### Tar with time

> time tar -cvf etc.tar /etc

#### Uncompress

> tar -tf etc.tar
>
> tar -tzf etc.tgz # -t : test
>
> tar -xzvf etc.tgz # -x: expand
>
> tar -xjvf etc.tar.bz2


