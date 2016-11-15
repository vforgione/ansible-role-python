# Python

A role for installing specific versions of Python from the [DeadSnakes PPA](https://launchpad.net/~fkrull/+archive/ubuntu/deadsnakes)


## Requirements

None


## Role Variables

| name             | description                                                          | default | example |
| ---------------- | -------------------------------------------------------------------- | ------- | ------- |
| `python_version` | the version number of python to use for installing and running uWSGI | `3.5`   | `2.7`   |


## Dependencies

None


## Example Playbook

```yaml
- hosts: django-apps
  become: yes
  become_user: root
  roles:
    - role: vforgione.python
      python_version: 3.5
```

## License

MIT


## Author Information

[Vince Forgione](https://github.com/vforgione)
