## Introduction to ad hoc commands in Ansible

- An Ansible ad hoc command uses the /usr/bin/ansible command-line tool to automate a single task on one or more managed nodes. ad hoc commands are quick and easy, but they are not reusable. 
- So why learn about ad hoc commands? ad hoc commands demonstrate the simplicity and power of Ansible. 

#### Why use ad hoc commands?
ad hoc commands are great for tasks you repeat rarely. For example, if you want to power off all the machines in your lab for Christmas vacation, you could execute a quick one-liner in Ansible without writing a playbook. An ad hoc command looks like this:
```
$ ansible [pattern] -m [module] -a "[module options]"
```
#### ad hoc tasks use cases
- Use cases for ad hoc tasks
- Rebooting servers
- Managing files
- Managing packages
- Managing users and groups
- Managing services
- Gathering facts
- Check mode
- Patterns and ad-hoc commands


##### 1. Simple reboot command
```
ansible <target-manageed-node(s)> -b -m reboot
```
-  This command will reboot and gives the following status:
```
 <target-managed-node> | CHANGED => {
    "changed": true,
    "elapsed": 162,
    "rebooted": true
}
```