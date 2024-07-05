what-causes-ssh-error-kex-exchange-identification-connection-closed-by-remote

ERROR-ssh-copy-id root@10.128.0.11
/usr/bin/ssh-copy-id: INFO: Source of key(s) to be installed: "/root/.ssh/id_rsa.pub"
/usr/bin/ssh-copy-id: INFO: attempting to log in with the new key(s), to filter out any that are already installed
/usr/bin/ssh-copy-id: INFO: 1 key(s) remain to be installed -- if you are prompted now it is to install the new keys
root@10.128.0.11: Permission denied (publickey).
SOLUTION-----
copy key--- 
         /root/.ssh/id_rsa.pub------ from master
paste--- 
        /root/.ssh/authorized keys-------- in slave
give permissions in slave server
        chmod 700 ~/.ssh
        chmod 600 ~/.ssh/authorized_keys
restart sshd 
        sudo systemctl restart sshd
