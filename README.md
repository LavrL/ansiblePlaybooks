Small Ansible playbook

Scenario for playbook:

    * log into server
    * Update server
    * Install apache
    * Create file "myFile.html" in folder at /var/www/html/
    * echo "This is my text for Homepage" >>  myFile.html
    * Copy myFile.html into /var/www/html/

Some small configuration before running ansible playbook

    vi /etc/ansible/ansible.cfg
    host_key_checking = False

    vi /etc/ansible/hosts
    [web]
    Your_public_ip ansible_ssh_user=ubuntu ansible_ssh_private_key_file=/path/to/Mykey.pem ansible_python_interpreter=/usr/bin/python3

Your_public_ip = public IP of your server 
ansible_ssh_user = ssh user 
ansible_ssh_private_key_file = location of private key 
