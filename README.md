# linux_lib

[![quality](https://img.shields.io/ansible/quality/27910)](https://galaxy.ansible.com/vbotka/linux_lib)[![Build Status](https://app.travis-ci.com/vbotka/ansible-linux-lib.svg?branch=master)](https://app.travis-ci.com/vbotka/ansible-linux-lib)

[Ansible role.](https://galaxy.ansible.com/vbotka/linux_lib/) Ansible Linux library of tasks.

Feel free to [share your feedback and report issues](https://github.com/vbotka/ansible-linux-lib/issues).

[Contributions are welcome](https://github.com/firstcontributions/first-contributions).


## Description

Do not run this role. It's a collection of independent tasks. The purpose of this role is to provide a library of reusable tasks to be included in playbooks and other roles.

Tested with Ubuntu 18.04 and 20.04. Some tasks tested with CentOS 7.


## Requirements

### Collections

None.

### Roles

None.


## Variables


See defaults, vars and source of the tasks.


## Workflow

1) Install the role

```
shell> ansible-galaxy role install vbotka.linux_lib
```

2) Change variables

```
shell> editor vbotka.linux_lib/vars/main.yml
```

Review OS specific variables in *vars/*. Optionally put customized variables into the *vars* directory and fit the parameter *vars_from* of the module *include_role*.

3) Create the inventory

```
shell> cat hosts
[host1]
host1.example.com
[host1:vars]
ansible_connection=ssh
ansible_user=root
ansible_python_interpreter=/usr/bin/python3.6
ansible_perl_interpreter=/usr/bin/perl
```

4) Include role's tasks in a playbook, or in any other role

Best practice is to include *vars_from: "{{ ansible_os_family }}"*

```
shell> cat test-linux-lib.yml
- hosts: host1
  vars_files:
    - <Play specific variables>
  tasks:
    - include_role:
        name: vbotka.linux_lib
	tasks_from: <File to load from a role's tasks/ directory>
	vars_from: "{{ ansible_os_family }}"
```

5) Run the playbook

```
shell> ansible-playbook test-linux-lib.yml
```

## License

[![license](https://img.shields.io/badge/license-BSD-red.svg)](https://www.freebsd.org/doc/en/articles/bsdl-gpl/article.html)


## Author Information

[Vladimir Botka](https://botka.info)
