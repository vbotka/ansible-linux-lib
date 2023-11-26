# linux_lib

[![quality](https://img.shields.io/ansible/quality/27910)](https://galaxy.ansible.com/vbotka/linux_lib)[![Build Status](https://app.travis-ci.com/vbotka/ansible-linux-lib.svg?branch=master)](https://app.travis-ci.com/vbotka/ansible-linux-lib)

[Ansible role.](https://galaxy.ansible.com/vbotka/linux_lib/) Ansible Linux library of tasks.

Feel free to [share your feedback and report issues](https://github.com/vbotka/ansible-linux-lib/issues).

[Contributions are welcome](https://github.com/firstcontributions/first-contributions).


## Description

Do not run this role. It's a collection of independent tasks. The
purpose of this role is to provide a library of reusable tasks to be
included in playbooks and other roles.

Tested with Ubuntu 20.04 and 22.04. Some tasks tested with CentOS 7.


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

2) Include or import a task from *vbotka.linux_lib* in a playbook, or
   in any other role


```
shell> cat test-linux-lib.yml
- hosts: host1
  tasks:
    - include_role:
        name: vbotka.linux_lib
	tasks_from: install_package.yml
      vars:
        ll_ipkg_list: [wpasupplicant, wpagui, net-tools, ifupdown, wireless-tools]
```

3) Run the playbook

```
shell> ansible-playbook test-linux-lib.yml
```

## License

[![license](https://img.shields.io/badge/license-BSD-red.svg)](https://www.freebsd.org/doc/en/articles/bsdl-gpl/article.html)


## Author Information

[Vladimir Botka](https://botka.info)
