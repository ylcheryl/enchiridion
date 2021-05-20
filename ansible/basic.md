## Control: Install ansible and setup inventory
```
sudo yum install ansible
sudo su - ansible
ssh-keygen
ssh-copy-id node1

sudo su - ansible
touch /home/ansible/inventory
echo "node1" >> /home/ansible/inventory
```

## Node: ansible account sudo
```
ssh cloud_user@node1
sudo visudo
Add the following line to the file and save:
ansible    ALL=(ALL)       NOPASSWD: ALL
```
## Verify
```
ansible -i /home/ansible/inventory node1 -m ping > /home/ansible/output
```
