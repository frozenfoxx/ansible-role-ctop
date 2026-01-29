# ansible-role-ctop

Ansible role that installs [ctop](https://github.com/bcicen/ctop) - a top-like interface for container metrics.

## Requirements

None

## Supported Platforms

- Debian (buster, bullseye, bookworm)
- Ubuntu (bionic, focal, jammy)
- RHEL/CentOS/Rocky/AlmaLinux (8, 9)
- Fedora (38, 39, 40)
- Alpine Linux
- Arch Linux

### Supported Architectures

- amd64 (x86_64)
- arm64 (aarch64)

## Role Variables

All variables are listed below (see also `defaults/main.yml`).

```yml
# Version of ctop to install
ctop_version: "0.7.7"
```

## Usage

### Using Ansible Galaxy

```bash
ansible-galaxy install frozenfoxx.ctop
```

### Using requirements.yml

Add the role to your requirements.yml:

```yml
- name: frozenfoxx.ctop
  src: https://github.com/frozenfoxx/ansible-role-ctop
  version: main
```

Install the role:

```bash
ansible-galaxy install -r requirements.yml
```

### In a Playbook

```yml
---
- hosts: servers
  roles:
    - role: frozenfoxx.ctop
      ctop_version: "0.7.7"
```

Or using import_role:

```yml
- name: Install ctop
  ansible.builtin.import_role:
    name: frozenfoxx.ctop
```

## Testing

This role uses [Molecule](https://molecule.readthedocs.io/) for testing.

```bash
# Install molecule with docker driver
pip install molecule molecule-docker

# Run tests
molecule test
```

## Contributing

Pull requests welcome.

## License

Apache-2.0
