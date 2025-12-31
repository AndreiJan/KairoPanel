#Important Information 
This is some important stuff right here. 


## Connecting to the Server - Important Step 

Follow these steps: 
1. On your local machine, go and edit this file and paste the following: 
```bash 
#This will add the entire test environment to your known hosts. Ensure that you have test_environment in the ssh folder
ssh -i $env:USERPROFILE\.ssh\<SSH_KEY_NON_PUB_FILE> root@<IP_ADDRESS>


#Type this as you need to configure te configuration file to add the site. This will connect the "push" to the server. 
notepad $env:USERPROFILE\.ssh\config

#Add this to the specified file:
host <IP_ADDRESS>
    HostName <IP_ADDRESS>
    User root
    IdentityFile C:\Users\<USERNAME>\.ssh\<PROVIDED_SSH_KEY_NON_PUB> #Provided by me (Andrei Mendoza)
    IdentitiesOnly yes
```

2. After doing that, run this command to push the changes: 
```bash
#This will push changes to the Panel
git push production main

```


3. After running that, review changes by visiting http://<IP_ADDRESS>:8083
