Ansible playbook to install software packages
==============================================


This project contains the simplest possible [ansible](http://docs.ansible.com/ansible) playbook to download and install anaconda.

### How to use

 - Install ansible on your computer (sudo pip install ansible...), by default it installs in `/home/$USER/.local`, if not then add its installed directory to `$PATH` 
 - Clone this project.
 - Edit the `envs/hosts` file and enter the FQDN or IP address of the server you are deploying to.
 - Edit the `roles/anaconda/defaults/main.yml` file and change the version of anaconda.
 - Run the playbook :

      ```
      cd ansible
      ansible-playbook -i envs/ playbook.yml --user=$USER --ask-sudo-pass
      ```
      
### Note: all the servers in `envs/hosts` should allow ssh auth using keypair
