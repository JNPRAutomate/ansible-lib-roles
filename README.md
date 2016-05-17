# Ansible-lib-roles

Library of generic / reusable roles for Ansible ..

# Roles available
- [junos-rpm](https://github.com/JNPRAutomate/ansible-lib-roles/tree/master/junos-rpm) - Configure RPM
- [junos-jti](https://github.com/JNPRAutomate/ansible-lib-roles/tree/master/junos-jti) - Configure Junos Telemetry Interface
- [junos-junos-analyticsd](https://github.com/JNPRAutomate/ansible-lib-roles/tree/master/junos-analyticsd) - Configure Analyticsd
- [junos-syslog](https://github.com/JNPRAutomate/ansible-lib-roles/tree/master/junos-syslog) - Configure Remote Syslog  


> More information on each role is available on the README.md file in each role directory

# Definition of a role
# How to use a role in another project

There are 2 main options to use a role that is not located in your main project
1. Add the path to your role library to your Ansible configuration
2. Copy the role you are planning to use into your current project under the directory `roles`

Both solutions have pros & cons; 1/ will avoid role duplication and will keep everything centralized but any change you are doing on the main role will affect all your projects.  
The choice will also depend on how well the role is written

### 1/ Add the path to your role library to your Ansible configuration

There are multiple ways to change your Ansible configuration, either globally or by project, the [ansible website](http://docs.ansible.com/ansible/intro_configuration.html) is listing primarily these:
- ANSIBLE_CONFIG (an environment variable)
- ansible.cfg (in the current directory)
- .ansible.cfg (in the home directory)
- /etc/ansible/ansible.cfg

To add a new roles library you need to change the parameters [roles_path](http://docs.ansible.com/ansible/intro_configuration.html#roles-path) under defaults

```
[defaults]
roles_path = /etc/ansible/roles:../ansible-lib-roles
```
> /etc/ansible/roles is the default directory, it needs to be preserved otherwise module like Juniper.junos will not be available anymore.

### 2/ Copy the role folder into your current project under the directory `roles`
