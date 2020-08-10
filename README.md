# Ansible
## Application Deployment
## Configuration Management
## Orchestration
## Provisioning
## Security & Compliance



#### The management of your software on top of your hardware. Maintains the consistency of your product based on its req, design and functional attributes because the configuration management is applied over the entire life-cycle of your system. Hence it provides us with a very good visibility and control. You can continually check monitor the performances of all our assistants.

#### If any of the assistants are degrading the configurations management will notify us and we can prevent errors before they occuror even replace the server if needed. The management system holds the entire historical data of your infrastructure.

#### It documents all the snapshots of the infrastructure. So overall the configuration management infrastructure facilitates the orderly management of your system information and system changes so that it can use it for beneficial purposes.

#### Ansible - Configuration Management, Deployment & Orchestration tool. Automates the whole IT infrastructure(Automates the Cloud and IT process)-has 150 modules are customizable.

# Architecture

## CMDB Configuration Management DataBase
## Ansible Automation Engine

#### Inventory(list of all ip adresses of all the host machines) --> #### Playbook-(Entire work flow of our system -(Modules- core files-executed on all the node machines, APIs(support cmd tools i.e pyton API, Plugins-trigger what needs to be run on the playbook i.e connection plugin - enable the docker machine to run )
### Hosts machines via connection plugins or SSH.

#### Playbooks are written in YAML code.
#### Hosts
#### Variables
#### tasks
#### Handlers

### Playbook to install
```
---
- hosts: webservers
  tasks:
    -name: install apache2
     apt: name=apache2 update_cache=yes state=latest

  notify:
   - restart apache2

  handlers:
   -name :restart apache2
    service: name=apache2 state=restarted
```
