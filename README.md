Git
===

This [Ansible](http://www.ansible.com/home) role installs and configures [Git](http://git-scm.com/) - the famous open source distribution version control system.

## Prerequisites

* Add the role to the project's Ansible galaxy requirements file and install it via the ansible-galaxy command
* Use one of the Git tag versions if you want to stick to a certain version of this role (stable versus head)

## Supported Platform

* CentOS 6
* CentOS 7
* OSX 10.10 or newer

## How to use

* Add the following line to your Ansible's playbook role section if you want to use the Git role with its defaults:
```
roles:
    - ansible-git
```
* If you want to pass custom values for the available variables, add something similar to the line below:
```
roles:
    - { role: ansible-git, git_install_from_source: true, git_source_install_version: "2.3.5" }
```

## Configuration

### Variables

| Variable | Description | Default value | Mandatory |
|----------|-------------|---------------|-----------|
| git_source_install_mirror_url_packages | The URL pointing to the web location where the source packages can be found | https://www.kernel.org/pub/software/scm/git | No |
| git_install_from_source | Flag to enable a git installation from source. This may be a good alternative if the git package being shipped with the OS distro is outdated. | false | No |
| git_source_install_version | Used to specify the exact Git version to be installed from source | 2.3.5 | No |
| git_use_https_for_git_proto | Force git to use https instread of the git protocol. This may be useful in case there are blocking firewalls in between. | false | No |
| git_disable_ssl_cert_check | Disable SSL cert check. This may be useful if working with self-signed certs (for safety reasons not recommended) | false | No |
