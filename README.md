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
pull git 

change variables var_file.yml according to client

run playbook
#ansible-playbook qn-playbook.yml
check xampp using public ip
check tomee with ip:8080
copy war file to /opt/tomee/webapps
create db , user via phpmyadmin ( same as in the var file )

run playbook
#ansible-playbook qn-stage2-playbook.yml

run playboook
#ansible-playbook qn-ssl-playbook.yml
