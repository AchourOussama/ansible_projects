# Install Nginx and Deploy game application 

This ansible project automates the following : 

- Nginx installation
- Application deployment  

Therefore , the main playbooks for this projects are : 

- playbook for installing the nginx server and starting it (for both CentOS and Ubuntu os)

- playbook for unzipping the application archive file and deploying it on the nginx server 

## How to use ? 

We offers two ways for executing the project:  

1. Via running standalone ansible playbooks
2. Via running ansible roles 

The difference is just a matter of playbooks organizations and manageability best practices . 

### 1. Executing standalone playbooks 

Go to the **standalone playbooks** folder , on the host machine execute the following commands : 

- ansible-playbook nginx_playbook.yaml
- ansible-playbook playbook_stacker.yaml

### 2. Ansible Roles

For manageability reasons , we opted for organizing the previous playbooks in format of ansible roles , where we created two roles (each one is for a functionality of this project): 

**install-nginx** : installs nginx and make it ready for use

**deploy-application** unpacks the application file and deploy it on nginx

On the target machine, go to the **standalone playbooks** folder , and execute the following command: 

- ansible-playbook nginx_gameapp_playbook.yaml

This command will run the two roles.



