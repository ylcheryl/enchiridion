## Setup SSH
```
> ssh-keygen
> cat ~/.ssh/id_rsa.pub
```
Copy output. 

Go to Github->Settings->SSH and GPG Keys

https://learn.acloud.guru/handson/ee48386b-ce12-4804-9b20-27af29b12dab

## Setup repo
Github. Create repo. e.g. enchiridion

Select SSH before copying URL
```
> git clone git@github.com:ylcheryl/enchiridion.git
> cd enchiridion
> code .
```
Create/update files.
```
git add .
git status
git commit -am "first commit"
```
git remote add origin git@github.com:ylcheryl/enchiridion