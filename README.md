# provision
Ansible Scripts to Provision Basic Django Site:  Nginx->Gunicorn

# Provision Steps

1) Start EC2, Lightsail instance
   - Make sure to upload your proper ssh key if it's not already in the list.

2) Update the hosts file (this directory) with the IP address

3) Login and add you id_rsa to the .ssh directory
4) Update permissions on id_rsa:  chmod 400 ~/.ssh/id_rsa

5) Run provision script:
ansible-playbook  -s -u ubuntu ansible/standalone.yml -i hosts --extra-vars='HOST=standalone DOMAIN=ajumasoftware.com' -e 'ansible_python_interpreter=/usr/bin/python3'
