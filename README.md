Ansible Role: Yara
=========
[![Molecule Test](https://github.com/darsh12/ansible-yara/actions/workflows/ci.yml/badge.svg)](https://github.com/darsh12/ansible-yara/actions/workflows/ci.yml)

Build the latest version of yara from source. Yara helps in identifying and classifying malware. 
The main motivation was to configure it on Wazuh agents

Requirements
------------
None. Required packages and downloaded

Role Variables
--------------
Available variables and their default values are found at `defualts/main.yml`
```yaml
enable_ssl: false
enable_cuckoo: false
enable_magic: false
enable_dotnet: false
```

Each variable is a yara module that can be enabled to configure

Additional information on each module can be found at the [documentation](https://yara.readthedocs.io/en/stable/modules.html)

Dependencies
------------
None

Example Playbook
----------------

Including an example of how to use your role (for instance, with variables passed in as parameters) is always nice for users too:

```yaml
- hosts: server
  vars_files:
    - vars/main.yml
  roles:
    - { role: darsh12.yara }
```

`vars/main.yml`
```yaml
enable_ssl: true  # true/false
enable_cuckoo: false  # true/false
enable_magic: true  # true/false
enable_dotnet: false  #true/flase
```

License
-------

MIT/BSD

Author Information
------------------

Role created in 2021