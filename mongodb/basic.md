Install (CentOS)
```
> sudo su
> cat << EOF > /etc/yum.repos.d/mongodb-org-4.0.repo
[mongodb-org-4.0] 
name=MongoDB Repository 
baseurl=https://repo.mongodb.org/yum/redhat/7/mongodb-org/4.0/x86_64/ 
gpgcheck=1 
enabled=1 
gpgkey=https://www.mongodb.org/static/pgp/server-4.0.asc 
EOF
> yum install -y mongodb-org
> service mongod start
> exit
```
Import
```
> mongoimport -d cities -c cityinfo --type CSV --file /home/cloud_user/data/cities.csv --headerline
```
Test
```
> mongo
> use cities
> db.cityinfo.find({State:"GA"})
```