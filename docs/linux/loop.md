        for u in user{1..3} ; do 
            echo $u; 
        done

        for u in user{1..4} ; do 
            sudo useradd $u;   
            echo  "Password1" | sudo passwd   --stdin $u;   
        done

        for u in user{1..4} ; do 
            sudo useradd $u;       
            echo "$u:Password1" | sudo chpasswd ; 
        done
