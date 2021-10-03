>chmod -v -x file.sh # -v for verbose

#### unmask

>chmod +x # refers umask value
>
>chmod a+x # for all objects owner, group, 
>
>chmod u+x # for user who created the file

#### Check or get user exists:
>getent passwd ___username___

#### Add user
> sudo useradd -m <username>
>
> -m : to create user directory

#### Setting password

> RHEL8 - echo "$USER_PASSWORD" | sudo passwd "$1" --stdin
>
> All other linux - echo "$1:$USER_PASSWORD" | sudo chpasswd

#### Delete user
> sudo userdel -r <username>
>
> -r : to delete user directory

#### Switch user
> su -username

#### User check
> grep -q ^root: /etc/passwd && echo "root exists"
>
> grep -q ^root: /etc/passwd || echo "root does not exist"
