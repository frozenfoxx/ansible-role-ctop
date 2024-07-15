# ansible-role-ctop

Ansible role that installs [ctop](https://github.com/bcicen/ctop).

# Requirements

None

## Role Variables

All variables are listed below (see also `defaults/main.yml`).

```yml
ctop_version: "0.7.7"
```

# Usage

Add the role to your requirements.yml:

```yml
- name: frozenfoxx.ctop
    src: https://github.com/frozenfoxx/ansible-role-ctop
    version: main
```

Include the role as usual:

```yml
ansible.builtin.import_role: frozenfoxx.ctop
```

# Contributing

Pull requests welcome.
