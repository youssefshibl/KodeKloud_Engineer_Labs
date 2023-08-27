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


