



## Download Media

## Setup VM Configs
* Disk
30G

## Boot Into the Installation Media
* Test media and Intallation Process

## Installation Wizard
* Language -> American English

### Software
* Installation Source -> Closest mirror
* Software Selection  -> Server

### System
* Installation Destination
- [x] Custom
- [x] Done
- [x] Create them automatically to generate the boot partition
- [x] Encript my data 
* Edit the lvm
 * Desired Capacity
 * Enter encryption key
* Disable Kdump

## User Settings
* Root Password
* User creation
    * Full Name
    * Username
    - [x] Make this user Administrator
    * Password
* Lock Root Account

## Once On the New Booted System

* Log in
* sudo yum update && sudo yum upgrade
* sudo yum vim
* sudo vim /etc/ssh/sshd_config
    * Port 4242
    * PermitRootLogin no
* firewall
    * sudo firewall-cmd --zone=public --set-target=DROP --permanent
    * sudo firewall-cmd --zone=public --add-port=4242/tcp --permanent
    * sudo firewall-cmd --reload

* SELinux SSH
    * sudo semanage port -a -t ssh_port_t -p tcp 4242

* hostname
    * sudo hostnamectl set-hostname YourLogin
