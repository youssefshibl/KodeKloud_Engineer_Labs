

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

- 



