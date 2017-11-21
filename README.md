# iKNSA Formation LAMP Vagrant Installation

## This installation procedure is for native ubuntu/xenial (16.04) 64bits with Virtualbox and vagrant installed or using git-bash on windows

Start by installing git and set up your ssh connection.

### @Important Leave all default values. No passphrase and the newly generated key must be ~/.ssh/id_rsa

```
ssh-keygen -t rsa -b 4096 -C "your@email.com"
eval "$(ssh-agent -s)"
ssh-add ~/.ssh/id_rsa
```
Copy the content of the id_rsa.pub and paste it in github.

Then run:
```
ssh -T git@github.com
```
and accept with yes

Clone the repository

```
git clone https://github.com/iknsa-formation/lamp-xenial-vagrant-box.git
```
Go into the newly cloned repository 

```
cd lamp-xenial-vagrant-box
```

Then launch the install bash file 

```
./install.sh
```

Edit your local hosts file
```
vim /etc/hosts
```
Add the following lines:
```
192.168.33.10   formation.dev
```

Once the installation is complete and if there are no errors, you are good to go

### The MySQL password will be set to 'paris'

Connect to your vagrant:
```
vagrant ssh
```

If you have any problems
```
debug
ask google
```
