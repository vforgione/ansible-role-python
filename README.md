# Python Ansible Role

This role installs python, python dev headers, pip and virtualenv on Ubuntu systems.


## Usage

### Variables

#### Required

There are __no required variables__ for this role.

#### Configurable

| Name           | Default | Description                                                                                                                          |
| -------------- | ------- | ------------------------------------------------------------------------------------------------------------------------------------ |
| python_version | 3.5     | The version number of Python you want to install from the [Deadsnakes PPA](https://launchpad.net/~fkrull/+archive/ubuntu/deadsnakes) |

### Playbook Examples

#### Minimal

```yaml
- hosts: all
  become: yes
  become_user: root
  roles:
    - role: python
```

This will install the default configuration of `python3.5`, `python3-dev`, `pip3` and `virtualenv` (installed by `pip3`).

__Note:__ `pip3` is used to isolate any future funny business with site packages. You should also be using virtualenvs everywhere anyway...
 
#### Configured

```yaml
- hosts: all
  become: yes
  become_user: root
  roles:
    - role: python
      python_version: 2.6
```

This will install `python2.6`, `python-dev`, `pip` and `virtualenv`.
