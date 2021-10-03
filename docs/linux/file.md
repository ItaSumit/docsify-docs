#### While copying, removing, moving files

> filename* - filename followed by any number of characters

> filemname? - filename followed by single characterss

#### Options (cp and mv)

> -i - interactive

> -R - recursive 
>cp -R files/ backup/
>
>ls -R backup/

> -a - maintaines file attributes(ownerships..) while copying 

#### Options for rm 

> rm - delete file

> rm -i - interactive delete file

> rm -i filename* -  delete file with filename followed by any character intercatively

> rm -rf - recursive delete

> rmdir - remove empty directory

#### cat

>cat -vet filename
>
>-E- display $ at th end of each line
>
>-T - display TAB character as ^I
>
>-v - shows nonprinting

> Convert windows notepad files with dos2unix to execute on unix

#### Display lines
> nl ___filename___ # line numbers

#### Top lines

> head ___filename___

> head -n 2 ___filename___

#### Bottom lines

> tail ___filename___

> tail -n 2 ___filename___

> tail -2 ___filename___

> tail -f ___filename___ #- follow


#### Cut - Display certain columns

>-d = specify delimeter
>
>-f = specify columns
>
>e.g.
>
>scut -f1,3 -d":" /etc/passwd

#### less- Page of file
>less is more
>
>less can page up and down.
>
>less can search text in file

#### Sort

>sort -r filename # -r reverse
>
>sort -k4 -t"," filename #-k column
>
>sort -k4 -r -t"," filename #-k column
>
>cut -f4 -d"," filename | sort -u
>
>sort -k4 -n -t"," filename # -n numeric sort

####  Search files

### locate

> locare ___filename___
>
> locate -r ___regular expression___
>
>Find all sh scripts
>
>locate -r "\.sh$"
> locate with grep
>
> locate ___filename___ | grep ___pattern___
>
> updateddb # updates locate command database

#### Find

> find ___directory_to_search____

### Options


>-type d # d is directory
>
>-type f # f is file

#### Name
>-name ___"pattern"___
>
>-iname ____"pattern>____

#### Size
>-size +1M # size units k, M , G

#### Time
>time checks with content and attributes
>
>-cmin n,
>-ctime n
>-cnewer
>
>time checks with content
>
>-mmin n
>-mtime n
>-newer
>

#### Empty file
>-empty
>

#### Depth
>-maxdepth


#### Operators

>-and 
>
>-or
>
>-not
>
>Group multiple operators with parenthesis ()

#### Actions

> -delete
>
> -ls
>
> -print(default)
>
> -quit

#### User defined actions
> -exec <command> '{}' ';' # {}- current path name, ;- delimeter indicating end of command
>
> -ok instead of -exec to be intreactive

#### Improving effeciency with actions

> When the -exec action is used, it launches a new instance of the specified command each time a matching file is found. There are times when we might prefer to combine all of the search results and launch a single instance of the command. 
>
>use '+' instead of ';' to combine results


#### Xargs

>xargs accepts input from standard input and converts it into an argument list for a specified command
>
>find ~ -type f -name 'foo*' -print | xargs ls -l
>
>find ~ -iname '*.jpg' -print0 | xargs --null ls -l

#### Find examples

>https://www.tecmint.com/35-practical-examples-of-linux-find-command/













