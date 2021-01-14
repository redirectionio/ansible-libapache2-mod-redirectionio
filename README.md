# Ansible redirectionio-apache_module role

redirection.io is a Web traffic redirection manager. It provides a collection of tools for website administrators, SEO agencies and developers, which help analyze HTTP errors, setup HTTP redirections and monitor the traffic efficiently.

This role installs the [redirection.io](https://redirection.io/) Apache2 module. It supports Debian and RHEL-based Linux distributions.

Once installed, the [redirection.io](https://redirection.io/) Apache2 module might be used in Apache Virtualhosts, as
described [in the related documentation](https://redirection.io/documentation/developer-documentation/apache-module#configuration).

## Installation

Simply run the following command:

```
ansible-galaxy install redirectionio.apache_module
```

## Role variables

By default, this role installs the last stable version of [libapache2-mod-redirectionio](https://github.com/redirectionio/libapache2-mod-redirectionio).
This behavior can be modified using the following role variables:

 * `redirectionio_apache_module_channel` (default: `stable`): choose a specific release channel (`stable` or `beta`)
 * `redirectionio_apache_module_main_version` (default: `2`): main version of the Apache module. This allows to upgrade safely your system without BC break with a new main version
 * `redirectionio_apache_module_version` (default: `*`): specific version of the Apache module. Use `*` to use the latest available version. Valid versions are of the form: `[timestamp]:[version]-[build]`, if you want a specific version like `2.0.0`, you should use `:2.0.0-`

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
