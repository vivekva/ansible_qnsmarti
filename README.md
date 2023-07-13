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
 wget https://qnsmarti.s3.ap-south-1.amazonaws.com/apache-tomee-8.0.14-plume.tar.gz
```

## Install XAMPP Manually

```
./xampp-linux-x64-8.1.12-0-installer.run
```
## Pull this git project to the server

### change variables in the  `var_file.yml` according to client

## Run playbook 
```
ansible-playbook qn-playbook.yml
````

check xampp using public ip <br />
check tomee with ip:8080 <br />
create `database`  `username` and its `password`  via PHPMyAdmin ( same as in the var file ) <br />
import database - ask developer <br />
copy the war file to `/opt/tomee/webapps` <br />
check the app with ip:8080/buildname

### Restart tomee service if needed
```
sh /opt/tomee/bin/shutdown.sh
```
```
sh /opt/tomee/bin/startup.sh
```

## Run playbook 
```
ansible-playbook qn-stage2-playbook.yml
```

## run playbook
```
ansible-playbook qn-ssl-playbook.yml
````

## Edit property files in the app 

image <br />
mail details <br />
license details <br />
WEB-INF/classes/com/ipsr/email/notification/conf.properties <br />
QnLive/WEB-INF/classes/com/ipsr/email/notification/ <br />
college name and other display info <br />
image upload location  ( same as in the server.xml  - should end with slash /) <br /> 
