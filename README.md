# Learn Ansible Lab

Machine Agent Linux Play
=========

Installs AppDynamics machine agent on a target machine. As a result of a successful run machine agent is installed as a service and reporting to a controller.

Requirements
------------

- Create a Target node (Linux, Centos or RedHat) to be used to install machine agent on
- Obtain controller connection details (host, access key, account name)
- Have Ansible installed on a Control node
- Ability to SSH into Target nodes from Control node
- Download Machine agent .zip to the root of this project

Role Variables
--------------
```
agent_version: # full agent version

sim_enabled: # true/false to enable/disable server visibility

appd_linux_root: # path to agent files on a target host
machine_agent_dest_folder_linux: "{{ appd_linux_root }}/machine-agent"

ma_agent_dest_file: # name of the machine agent destination file
ma_agent_source_file: # name of the machine agent source file (downloaded machine agent .zip file name)

java_system_properties: # leave blank

create_appdynamics_user: # controls if appdynamics user should be created on target machine
appdynamics_user: # user and group name
```

Example Running Playbook
----------------

`ansible-playbook playbooks/machine_agent_play.yaml`

