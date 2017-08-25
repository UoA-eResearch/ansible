Ansible playbook to install software packages
==============================================


This project contains [ansible](http://docs.ansible.com/ansible) playbook to download and install:
- Anaconda (Python 3.6 and 2.7)
- R 
- RStudio
- Docker 
- X2GoServer (with MATE bindings)

### How to use

 - Install ansible on your computer `pip install ansible`, by default it installs in `/home/$USER/.local`. 
 - Clone this project.
 - Edit the [`envs/hosts`](envs/hosts) file and enter the FQDN or IP address of the server you are deploying to.
 - Edit the [`roles/anaconda/defaults/main.yml`](roles/anaconda/defaults/main.yml) file and change the version of anaconda.
 - Edit the [`roles/r/defaults/main.yml`](roles/r/defaults/main.yml) file and change the site-library and packages. Check [README.md](roles/r/README.md) for details.
 - Edit the [`roles/rstudio/defaults/main.yml`](roles/rstudio/defaults/main.yml) file and change the version of rstudio.
 - Run the playbook :

      ```
      cd ansible
      ansible-playbook -i envs/ playbook.yml --user=$USER --ask-sudo-pass
      ```
      
### Note: all the servers in `envs/hosts` should allow ssh auth using keypair
