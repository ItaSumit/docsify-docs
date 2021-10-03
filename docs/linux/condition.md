>To test variable value , use conditiion in square bracket or with command test

>For test output from command , no need to use [] or test command.


>Testing non-zero value: -n
>
>example:
>
>while ! [ -n "$inputstring" ]

>-n : checks for string with empty spaces.
>
>check **man test** for more checks

        #!/bin/bash
        if [ $# -eq 0 ]  ; then
                read -p "Enter a username: "        user_name
                read -sp "Enter a password: "       user_password
                echo ""
                read -sp "Enter the password again:         " user_password_check
                if [ "$user_password" !=        "$user_password_check" ] ; then
                        echo -e "\n${0}: Passwords      do not match!"
                        exit 1
                fi
        else
                user_name="$1"
                user_password="${2:-Password1}"
        fi
        echo -e "\n$user_name $user_password"