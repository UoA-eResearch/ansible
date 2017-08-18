Ansible playbook to install anconda
====================================


This project contains the simplest possible [ansible](http://docs.ansible.com/ansible) playbook to download and install anaconda.

### How to use

 - Install ansible on your computer (sudo pip install ansible...).
 - Set $ANSIBLE_HOME.
 - Clone this project.
 - Edit the `envs/hosts` file and enter the IP address of the server you are deploying to.
 - Edit the `roles/anaconda/defaults/main.yml` file and change the version of anaconda.
 - Run the playbook :

      ```
      source $ANSIBLE_HOME/hacking/env-setup
      cd ansible-anaconda
      $ANSIBLE_HOME/bin/ansible-playbook -i envs/ playbook.yml --user=$USER --ask-sudo-pass
      ```
      
