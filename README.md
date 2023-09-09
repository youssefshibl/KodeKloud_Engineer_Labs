![Screenshot2](https://github.com/youssefshibl/KodeKloud_Engineer_Labs/assets/63800183/f76ab057-8248-476a-809f-72c976168f8f)


# KodeKloud Engineer Labs

## Linux

#### Level 1

-  ###### 005 - Linux User Expiry

    ```bash
    useradd -e 2021-01-28 user1 # set expire data for user1
    chage -l user1 # list data of user as well as expire data
    chage -E 2022-07-15 user1 # change expire data for exist user 
    ```

- ###### 006 - Linux User Files

  ``````bash
  find / -user user1 -exec [command] {} \; # execute command after find 
  find /home/usersdata/ -type f -user user1 -exec cp --parents {} /test \; 
  # this command find user1 files in this dir and copy them to /test 
  ``````

- ###### 007: Disable Root Login
  ``````bash
  # there are flag in /etc/ssh/sshd_config
  # `PermitRootLogin yes`
  nano  /etc/ssh/sshd_config # change PermitRootLogin to `no`
  systemctl restart sshd # restart service
  ``````
- ###### 008: Linux Archives
  ``````bash
  tar -cvzf test.tar.gz /data/test # compress test dir in test.tar.gz
  mv test.tar.gz /home/  # move test.tar.gz to /home/
  ``````
- ###### 009: Linux File Permissions
  ``````bash
  chmod o+rx /tmp/xfusioncorp.sh #change Permissions of script read and execute
  ``````
- ###### 010: Linux Access Control List
  ``````bash
  setfacl -m u:user1:-,user2:r /etc/resolv.conf # setfacl to set special permission to file
  getfacl /etc/resolve.conf
  # file: etc/resolv.conf
  # owner: root
  # group: root
  user::rw-
  user:user1:---
  user:user2:r--
  group::r--
  mask::r--
  other::r--
  ``````
- ###### 011: Linux String Substitute
    ``````bash
  grep Random /root/nautilus.xml | wc -l # get match word and count them
  sed -i 's/Random/Maritime/g' /root/nautilus.xml   # replace all "Random" by "Maritime"
  ``````
- ###### 012: Linux Remote Copy
    ``````bash
  scp -r /tmp/nautilus.txt.gpg steve@172.16.238.11:/home/code
  # copy files from local by remote by "scp" 
  ``````    
  


