# Ansible role [storage](https://galaxy.ansible.com/ui/standalone/roles/buluma/storage/documentation)

Create partitions, volume groups, volumes, filesystems and mounts

|GitHub|Version|Issues|Pull Requests|Downloads|
|------|-------|------|-------------|---------|
|[![github](https://github.com/buluma/ansible-role-storage/actions/workflows/molecule.yml/badge.svg)](https://github.com/buluma/ansible-role-storage/actions/workflows/molecule.yml)|[![Version](https://img.shields.io/github/release/buluma/ansible-role-storage.svg)](https://github.com/buluma/ansible-role-storage/releases/)|[![Issues](https://img.shields.io/github/issues/buluma/ansible-role-storage.svg)](https://github.com/buluma/ansible-role-storage/issues/)|[![PullRequests](https://img.shields.io/github/issues-pr-closed-raw/buluma/ansible-role-storage.svg)](https://github.com/buluma/ansible-role-storage/pulls/)|[![Ansible Role](https://img.shields.io/ansible/role/d/buluma/storage)](https://galaxy.ansible.com/ui/standalone/roles/buluma/storage/documentation)|

## [Example Playbook](#example-playbook)

This example is taken from [`molecule/default/converge.yml`](https://github.com/buluma/ansible-role-storage/blob/master/molecule/default/converge.yml) and is tested on each push, pull request and release.

```yaml
---
- name: Converge
  hosts: all
  become: true
  gather_facts: true

  roles:
    - role: buluma.storage
```

The machine needs to be prepared. In CI this is done using [`molecule/default/prepare.yml`](https://github.com/buluma/ansible-role-storage/blob/master/molecule/default/prepare.yml):

```yaml
---
- name: Prepare
  hosts: all
  gather_facts: false
  become: true
  serial: 30%

  roles:
    - role: buluma.bootstrap
```

Also see a [full explanation and example](https://buluma.github.io/how-to-use-these-roles.html) on how to use these roles.

## [Role Variables](#role-variables)

The default values for the variables are set in [`defaults/main.yml`](https://github.com/buluma/ansible-role-storage/blob/master/defaults/main.yml):

```yaml
---
# defaults file for storage

storage_default_fstype: ext4

# storage_partitions:
#   - name: /dev/sdb
#     number: 1
#     part_end: 4GiB
#     label: gpt
#   - name: /dev/sdb
#     number: 2
#     flags:
#       - lvm
#     part_start: 4GiB
#     part_end: 8GiB

# storage_volumegroups:
#   - name: group1
#     devices:
#       - /dev/sdb2
#     size: 8
#   - name: group2
#     devices:
#       - /dev/sdb2
#     size: 128M

# storage_volumes:
#   - name: var1
#     vg: group1
#     size: 16

# storage_filesystems:
#   - name: /dev/group1/var
#     filesystem: ext4

# storage_mounts:
#   - name: /var
#     src: /dev/group1/var1
#     owner: root
#     group: root
#     mode: "0755"
#     opts: defaults
#     boot: true
#     dump: 0
#     passno: 2
```

## [Requirements](#requirements)

- pip packages listed in [requirements.txt](https://github.com/buluma/ansible-role-storage/blob/master/requirements.txt).

## [State of used roles](#state-of-used-roles)

The following roles are used to prepare a system. You can prepare your system in another way.

| Requirement | GitHub | Version |
|-------------|--------|--------|
|[buluma.bootstrap](https://galaxy.ansible.com/buluma/bootstrap)|[![Ansible Molecule](https://github.com/buluma/ansible-role-bootstrap/actions/workflows/molecule.yml/badge.svg)](https://github.com/buluma/ansible-role-bootstrap/actions/workflows/molecule.yml)|[![Version](https://img.shields.io/github/release/buluma/ansible-role-bootstrap.svg)](https://github.com/shadowwalker/ansible-role-bootstrap)|

## [Context](#context)

This role is a part of many compatible roles. Have a look at [the documentation of these roles](https://buluma.github.io/) for further information.

Here is an overview of related roles:

![dependencies](https://raw.githubusercontent.com/buluma/ansible-role-storage/png/requirements.png "Dependencies")

## [Compatibility](#compatibility)

This role has been tested on these [container images](https://hub.docker.com/u/buluma):

|container|tags|
|---------|----|
|[Alpine](https://hub.docker.com/r/buluma/alpine)|all|
|[Amazon](https://hub.docker.com/r/buluma/amazonlinux)|Candidate|
|[EL](https://hub.docker.com/r/buluma/enterpriselinux)|8, 9|
|[Debian](https://hub.docker.com/r/buluma/debian)|all|
|[Fedora](https://hub.docker.com/r/buluma/fedora)|all|
|[opensuse](https://hub.docker.com/r/buluma/opensuse)|all|
|[Ubuntu](https://hub.docker.com/r/buluma/ubuntu)|all|

The minimum version of Ansible required is 2.12, tests have been done to:

- The previous version.
- The current version.
- The development version.

If you find issues, please register them in [GitHub](https://github.com/buluma/ansible-role-storage/issues)

## [Changelog](#changelog)

[Role History](https://github.com/buluma/ansible-role-storage/blob/master/CHANGELOG.md)

## [License](#license)

[Apache-2.0](https://github.com/buluma/ansible-role-storage/blob/master/LICENSE)

## [Author Information](#author-information)

[Shadow Walker](https://buluma.github.io/)
