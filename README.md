## ansible_qnsmarti - Prerequisites

```
apt-add-repository ppa:ansible/ansible
```
```
apt update
```
```
apt install ansible
```
```
ansible --version
```

## Download files from S3
```
 wget https://qnsmarti.s3.ap-south-1.amazonaws.com/xampp-linux-x64-8.1.12-0-installer.run
```
```
 wget https://qnsmarti.s3.ap-south-1.amazonaws.com/ultima-2.0.17-12-2022-1.war
```
 wget https://qnsmarti.s3.ap-south-1.amazonaws.com/apache-tomee-8.0.14-plume.tar.gz
```


./xampp-linux-x64-8.1.12-0-installer.run <br />
### pull git 

change variables var_file.yml according to client <br />

## run playbook 
ansible-playbook qn-playbook.yml <br />
check xampp using public ip <br />
check tomee with ip:8080 <br />
copy war file to /opt/tomee/webapps <br />
create db , user via phpmyadmin ( same as in the var file ) <br />
import database - ask developer <br />

## run playbook
ansible-playbook qn-stage2-playbook.yml <br />

## run playboook <br /> 
#ansible-playbook qn-ssl-playbook.yml <br />

## edit property files in the app 

image <br />
mail details <br />
license detailes <br />
college name and other display info <br />
image upload location  ( same as in the server.xml  - should be end with slash /) <br /> 
