# provision
Ansible Scripts to Provision Basic Django Site:  Nginx->Gunicorn

# Provision Steps

1) Start EC2, Lightsail instance

2) Login and add you id_rsa to the .ssh directory

3) Run provision script:

ansible-playbook  -s -u ubuntu ansible/standalone.yml -i hosts -e 'ansible_python_interpreter=/usr/bin/python3' --extra-vars='HOST=standalone'
