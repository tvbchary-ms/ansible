# How to setup Passwordless Authentication

## EC2 Instances

### Using Public Key

- downloand the .pem file
- move it into ~/.ssh/   directory
- change permission to read-only (chmod 400)
- create/edit ~/.ssh/config  file


##### config file content
  
```
Host <desired_ssh_loginname>
HostName <Public/Private_IP_In_Scope>
User <username>
IdentityFile <path/to/.pem/file>
```
#### Example
```
Host aws-app-instance
HostName 121.121.121.121
User ubuntu
IdentityFile <~/.ssh/my_key_pair.pem>
```
#### Now we can login using ssh <Host> 
##### - example: ssh aws-app-instance