#### SED

> Stream editor sed can be used to edit the file
>
> sed -i '/^#/d; /^$/d' /etc/ntp.conf
>
> -i : indicates inplace audit

		 sed 'p' /etc/passwd # prints each line twice, printing matching patterns and output from standard out
		 sed -n 'p' /etc/passwd # -n: suppress standard output, print only matching lines
		 sed -n '1,5p' /etc/passwd # prints first 5 lines
		 sed -n '/^user/p' /etc/passwd # prints line start with given regex
		 sed -n ' /^#/ d ; /^$/ d' /etc/passwd # deletes commented and empty lines, only on screen output
		 sed -i.bak ' /^#/ d ; /^$/ d' /etc/passwd # deletes commented and empty lines # writes file with backup

#### Print Patterns

> '1,4 p' ___filename___
>
> '1,$ p' ___filename___
>
> '/___regex___/ p' ___filename___

#### Substitute

		sed '<range> s/<string or regex>/<replacement>/' <filename> # delimeter after 's' can be anything, #range can be line number or regex

		sed '/^root/ s@/bin/bash@/bin/sh@p' <filename>

		with regular expression:
		sed ' 6,9 s/^/  /g' <filename> # adding space in starting of line 6 to 9

#### Append/Insert/Delete

	sed '<range or /regex/> a <string to append>' <filename>
	sed '<range or /regex/> i <string to append>' <filename>
	sed '<range or /regex/> d' <filename>

#### AWK

> awk -W version

		 awk ' { print } ' /etc/passwd
		 awk 'BEGIN { print "List of users" } { print } END  { print NR  } ' /etc/passwd # With header and footer. NR: Number of rows

		 awk 'BEGIN { print "List of users" } { print NR, $0 } END  { print NR  } ' /etc/passwd # With header and footer. NR: Number of rows

		 ifconfig eth0 | awk -F":" '/HWaddr/{print $3 $4 $5 $6 $7}'

		 ifconfig llw0 | awk -F":" '/ether/{print toupper( $3 $4 $5 $6 $7 )}' # onmac
