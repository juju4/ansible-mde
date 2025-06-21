[![Actions Status - Master](https://github.com/juju4/ansible-mde/workflows/AnsibleCI/badge.svg)](https://github.com/juju4/ansible-mde/actions?query=branch%3Amaster)
[![Actions Status - Devel](https://github.com/juju4/ansible-mde/workflows/AnsibleCI/badge.svg?branch=devel)](https://github.com/juju4/ansible-mde/actions?query=branch%3Adevel)

# mde ansible role

Setup Microsoft Defender for Endpoint
* https://learn.microsoft.com/en-us/microsoft-365/security/defender-endpoint/microsoft-defender-endpoint-linux?view=o365-worldwide
* https://learn.microsoft.com/en-us/microsoft-365/security/defender-endpoint/linux-preferences?view=o365-worldwide
* https://github.com/juju4/mde-baseline-ansible
* https://github.com/juju4/mde-baseline (inspec)

## Requirements & Dependencies

### Ansible
It was tested on the following versions:
 * 2.13

### Operating systems

Tested on Ubuntu 20.04, 22.04.

## Example Playbook

Just include this role in your list.
For example

```
- host: myhost
  roles:
    - juju4.mde
```

you probably want to review variables

## Variables

TBD

## Continuous integration

```
$ pip install molecule docker
$ molecule test
$ MOLECULE_DISTRO=ubuntu:20.04 molecule test --destroy=never
```


## Troubleshooting & Known issues

* MDE can cause performance issues. Most often it is related to auditd and an appropriate process exclusion will help.

## Resources

* [Common mistakes to avoid when defining exclusions, MDE](https://learn.microsoft.com/en-us/defender-endpoint/common-exclusion-mistakes-microsoft-defender-antivirus)
* [Important points about exclusions](https://learn.microsoft.com/en-us/defender-endpoint/configure-exclusions-microsoft-defender-antivirus#important-points-about-exclusions)

## License

BSD 2-clause
