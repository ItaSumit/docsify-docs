#### User Input
>read -s -p "Enter your input: " INPUT
>
>-s = Silent, do not echo the typed letters
>
>-p = Prompt message
>
>If variable is not added in last, user input will be stored in $REPLY

#### Default Value

>user_password=${2:-Password1}
>
>If 2nd argument is not given by user defalu value (i.e. Password1) will be used

> Function parameters works in same was as script parameters
