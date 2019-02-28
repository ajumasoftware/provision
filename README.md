# provision
Ansible Scripts to Provision Basic Django Site:  Nginx->Gunicorn

# Provision Steps

1) Start EC2, Lightsail instance

2) Login and add you id_rsa to the .ssh directory
3) Update permissions on id_rsa:  chmod 400 ~/.ssh/id_rsa

4) Run provision script:
ansible-playbook  -s -u ubuntu ansible/standalone.yml -i hosts --extra-vars='HOST=standalone DOMAIN=ajumasoftware.com' -e 'ansible_python_interpreter=/usr/bin/python3'
