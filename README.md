# provision
Ansible Scripts to Provision Basic Django Site:  Nginx->Gunicorn

ansible-playbook  -s -u ubuntu ansible/standalone.yml -i hosts -e 'ansible_python_interpreter=/usr/bin/python3' --extra-vars='HOST=standalone'
