# Ansible redirectionio-apache_module role

This role installs the [redirection.io](https://redirection.io/) Apache2 module. It supports Debian and RHEL-based Linux distributions.

Once installed, the [redirection.io](https://redirection.io/) Apache2 module might be used in Apache Virtualhosts, as
described [in the related documentation](https://redirection.io/documentation/developer-documentation/apache-module#configuration).

## Installation

Simply run the following command:

```
ansible-galaxy install redirectionio.apache_module
```

## Role variables

This role does not provide variables.

## Example playbook

```yml
- hosts: webservers
  roles:
    - { role: redirectionio.apache_module, become: true }
```

## Dependencies

This role has no dependency.

## License

This role is available under the terms of the MIT License.
