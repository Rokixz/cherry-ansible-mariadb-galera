# A simple Ansible playbook for building MariaDB Galera Cluster in Cherry Servers environment

Requirmenets:

  - Ansible >= v2.*;
  - Python >= v3.*;
  - Cherry servers ansible library;
  - Cherry servers python module cherry-python;
  - Shell.

# Getting started
  - Create an account and top up the credit in https://portal.cherryservers.com environment;
  - Create a new project;
  - Prepare an empty and clean directory for the working environment;
  - Install the Python module using **pip install cherry-python**
  - Generate either private and public keys into the working dir;
  - Clone this repository for Ansible playbooks and templates into the working dir.

# Installation
- Create the API token using the client's portal and export it into the environment variable:
```
export CHERRY_AUTH_TOKEN="4bdc0acb8f7af4bdc0acb8f7afe78522e6dae9b7e03b0e78522e6dae9b7e03b0"
```
- Download the library files into the **working dir/library** from https://bitbucket.org/cherryservers/cherry_ansible_module;
- As soon the repository is cloned, modify the variables in **servers_deploy.yml**, **vars.yml** and **templates/galera.cnf** according your project and the needs;
- Deploy your Galera Cluster by running the playbook:
```
ansible-playbook servers_deploy.yml
```
**That's it! As soon the process is finished, your MariaDB Galera cluster is ready for use.**
