# Vagrant Installation 

You MUST do the following setup in the order stated as the applications depend on each other 

## Setup guide

### Step 1 - Ruby
Download from the following link for windows:

https://github.com/oneclick/rubyinstaller2/releases/download/RubyInstaller-2.6.6-1/rubyinstaller-devkit-2.6.6-1-x64.exe

Check version of your ruby on git
ruby --version

![rubypic](https://user-images.githubusercontent.com/104793540/184134293-c246ecb9-ea59-4a26-bb5d-8d3f31c585d2.PNG)



### Step 2 - Vagrant
#### Downloading 
Download from the following link for windows:

https://www.vagrantup.com/downloads

From the list of OS pick yours and download 
![image](https://user-images.githubusercontent.com/104793540/184134469-596b439b-dc51-4648-92af-cb6d493e782e.png)

Check version of your vagrant on git
vagrant --version

![image](https://user-images.githubusercontent.com/104793540/184136250-f3f3dd5e-fefc-40b9-8d9e-a45ec3c0b3f2.png)


### Step 3 - VirtualBox 
Use the following link to download for windows:

https://www.virtualbox.org/wiki/Downloads 

![image](https://user-images.githubusercontent.com/104793540/184135055-a9cdd357-e4a0-40ff-8be1-53c7a807ebc1.png)

### Step 4 - Checking Installations 
Create a new directory and within it nano Vagrantfile 
```python 

Vagrant.configure("2") do |config|

 config.vm.box = "ubuntu/xenial64"
# creating a virtual machine ubuntu 

end

```
run `vagrant up` command in terminal where vargrantfile is located 

run `vagrant status`
# What is DevOps env & benefits 
## Vagrant and Virtual box
![image](https://user-images.githubusercontent.com/104793540/184343497-7f79029b-699d-48df-9ced-f8872dee7fe2.png)

### Linux & Virtualisation ( + scripting)
creating linux vim 
1. run vagrant up 
2. check vagrant status 
3. vagrant ssh
4. mkdir filename - work in this or not

#### How to create automate tasks with provisioning scripts 

Automate update and upgrade 
1. `sudo nano filename.sh`
2. `sudo apt-get update -y`
3. `sudo apt-get upgrade -y`
4. ctrl x > yes > enter 
5. check content with `cat filename`
6. `ll` to check permision 
7. `sudo chmod +x filename.sh` 
8. `ll` to check again 
9. run filename.sh `sudo ./filename.sh`

### Linux commands

- find out OS name 
`uname` or `uname -a`

- how to create file in linux 
`touch filename` or `nano filename`

- how to check existing file/fodlers
`ls` or `ls -a`

- how to create a folder `mkdir fodlername`

- how to navigate inside the folder `cd foldername`

- how to come out of the folder or 1 step back `cd ..`

- how can we check our current location `pwd`
- whoami 

- how to copy file `cp filename destination`

filename_with_absolute_path 
destination_with_absolue_path

- how to remove file/folder `rm -rf file/foldername`

- how to cut paste file/ move the test file inside 

`mv filename distination`

- how to check all processes `top` and `ps aux`

- how to remove/delete/kill process ``

- `sudo su` > `exit` then enter 
can use `sudo` with any command 

- how to use `` pipe 
- how to check file permission `ll`
- change file permission `chmod +x filename`
- `r` or `w` or `rw` `all` also numbers `400` or `600` for all `700`

#### Updating and upgrading 
- update our ubuntu  OS `apt-get install update `
anytime i have permission issues use `sudo` ie `sudo apt-get install update`

- upgrade our ubuntu os 
`apt-get upgrade -y`

- how to create automate tasks with provisioning scripts 
- automate update and upgrade 

- `cat filename`

- run provision.sh `./provision.sh`

#### Solving Errors
- if errors vagrant destroy, vagrant up, vagrant ssh  
- update,uprgade, install nginx

#### Installing NGINX
- Install nginx `sudo apt-get install nginx -y`
- check if install worked `sudo systemctl status nginx `
- how to restart a process - in this case its an NGINX
- restart or start `sudo systemctl restart nginx`
- check status
- enable the process `sudo systemctl enable nginx`
