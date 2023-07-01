# ansible_qnsmarti - Prerequisites

apt-add-repository ppa:ansible/ansible <br />
apt update <br />
apt install ansible <br />
ansible --version <br />
cat /etc/ansible/ansible.cfg <br />
 wget https://qnsmarti.s3.ap-south-1.amazonaws.com/xampp-linux-x64-8.1.12-0-installer.run <br />
 wget https://qnsmarti.s3.ap-south-1.amazonaws.com/ultima-2.0.17-12-2022-1.war <br />
 wget https://qnsmarti.s3.ap-south-1.amazonaws.com/apache-tomee-8.0.14-plume.tar.gz <br />
./xampp-linux-x64-8.1.12-0-installer.run <br />
pull git <br /> 

change variables var_file.yml according to client <br />

run playbook <br />
#ansible-playbook qn-playbook.yml <br />
check xampp using public ip <br />
check tomee with ip:8080 <br />
copy war file to /opt/tomee/webapps <br />
create db , user via phpmyadmin ( same as in the var file ) <br />
import database - ask developer <br />

run playbook <br />
#ansible-playbook qn-stage2-playbook.yml <br />

run playboook <br /> 
#ansible-playbook qn-ssl-playbook.yml <br />

edit property files in the app <br />

image <br />
mail details <br />
license detailes <br />
college name and other display info <br />
image upload location  ( same as in the server.xml  - should be end with slash /) <br /> 
