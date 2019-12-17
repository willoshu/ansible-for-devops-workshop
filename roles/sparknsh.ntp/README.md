# Ansible Role: NTP

#### Version: 1.0.5

[![](https://img.shields.io/badge/role-sparknsh.ntp-blue.svg)](https://galaxy.ansible.com/sparknsh/ntp)

Development of this project is managed in a private repository then pushed out to [GitLab](https://gitlab.com/sparknsh/ansible-role-ntp) and [GitHub](https://github.com/sparknsh/ansible-role-ntp) when we have a new version for you. If you have any issues please contact [sparknsh](https://www.sparknsh.com/contact?type=issue&name=ansible-role-ntp)

## Role Variables

```yaml
ntp__enabled: true
ntp__timezone:

ntp__conf_tpl: ntp.conf.j2

ntp__servers: []

ntp__restrict: []
```

#### Example

```yaml
ntp__enabled: true
ntp__timezone: Etc/UTC

ntp__conf_tpl: ntp.conf.j2

ntp__servers:
  - "time.nist.gov iburst"
  - "ntp1.npl.co.uk iburst"
  - "ntp.sydney.nmi.gov.au iburst"
  - "time.google.com iburst"

ntp__restrict:
  - "127.0.0.1"
  - "::1"
```

## Example Playbook

```yaml
- hosts: all
  vars_files:
    - vars/main.yml
  roles:
     - { role: sparknsh.ntp }
```

## License

MIT

## Author Information

This role was created in 2019 by [sparknsh](https://www.sparknsh.com) at [Rebel Media, Inc.](https://www.rebelmedia.io/)
