# How to setup Passwordless Authentication

## EC2 Instances

### Using Public Key

- downloand the .pem file
- move it into ~/.ssh/   directory
- change permission to read-only (chmod 400)
- create/edit ~/.ssh/config  file


##### config file content
  
```bash
Host <desired_ssh_loginname>
HostName <Public/Private_IP_In_Scope>
User <username>
IdentityFile <path/to/.pem/file>
```
