```
> ansible-config view
```
Found dbsystems is defined in /etc/ansible/hosts
```
[dbsystems]
db1
db2
```
On user, file, copy, service
```
> ansible dbsystems -b -m user -a "name=supervisor"
> ansible dbsystems -b -m file -a "path=/home/supervisor/.ssh state=directory owner=supervisor group=supervisor mode=0755"
> ansible dbsystems -b -m copy -a "src=/home/ansible/keys/supervisor/authorized_keys dest=/home/supervisor/.ssh/authorized_keys mode=0600 owner=supervisor group=supervisor"

> ansible all -b -m service -a "name=auditd state=started enabled=yes"
```