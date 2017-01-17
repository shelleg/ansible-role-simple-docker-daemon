Ansible Role Simple Docker Daemon
=================================


<img align="left" width="100px" height="100px" margin="10px 10px 10px 10px" src="https://www.docker.com/sites/default/files/Engine.png"></img>
A simplistic docker deamon role, result is a single Docker Daemon running on Centos 7 & Xenial.
This role was developed to get a docker daemon up an running in no time ... to get running, I assume more complex Dokcer senarios will be introduced in Swarm || K8s perspectives.

The role addes apt/yum official docker repositories & keys + installs the os package defaults.

Requirements
------------
- Internet access

Role Variables
--------------
```yamlex
docker_group: docker      # The gourp to add users too in order to manage containers
docker_group_members: []  # An emplty list you would most defintelly override in the playbook level
```

Dependencies
------------

- None

Example Playbook
----------------

Including an example of how to use your role (for instance, with variables passed in as parameters) is always nice for users too:

    - hosts: servers
      roles:
         - role: shellg.simple-docker-daemon
           # add the vagrant user as a docker container administrator
           docker_group_members:
            - vagrant 

License
-------

MIT

Author Information
------------------

Haggai Philip Zagury -> Tikal Knowledge
