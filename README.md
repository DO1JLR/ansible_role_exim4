# ansible_role_exim4

Ansible role to configure exim4.
By default you can tell exim4 that it will send mail via smarthost.

To do this you have at leaset set the smarthost FQDN in the variable: ``exim4__dc_smarthost:``.

 Example Playbook:
----------------
```
- name: run exim4 role
  hosts: localhost
  roles:
    - {role: dansible_role_exim, tags: exim4}
  vars:
    exim4__dc_smarthost: mx01.example.com
```

 Test if it is working
---------------------
To test if your exim4 configuration is working, maybe this will help:
```
mail': echo "This is a test" | mailx -s "Test Message" -v you@example.com
```

 Testing
----------
This role is tested with [these github-action](https://github.com/search?q=topic%3Acheck-ansible+topic%3Agithub-actions+org%3Aroles-ansible&type=Repositories) tests for different versions of differen linux systems. Linting is tested via travis-ci and the  [ansible-lint action](https://github.com/marketplace/actions/ansible-lint).
If you want to find out more about our tests, please have a look at the github marketplace.

| test status | Github Marketplace |
| :---------  | :----------------  |
| [![Ansible Lint check](https://github.com/do1jlr/ansible_role_exim4/workflows/Ansible%20Lint%20check/badge.svg)](https://github.com/do1jlr/ansible_role_exim4/actions?query=workflow%3A%22Ansible+Lint+check%22) | [ansible-lint action](https://github.com/marketplace/actions/ansible-lint) |
| ![Yamllint GitHub Actions](https://github.com/do1jlr/ansible_role_exim4/workflows/Yamllint%20GitHub%20Actions/badge.svg) |  [yamllint gitHub actions](https://github.com/marketplace/actions/yamllint-github-action) |
| | |
| [![Ansible check debian:stable](https://github.com/do1jlr/ansible_role_exim4/workflows/Ansible%20check%20debian:stable/badge.svg)](https://github.com/do1jlr/ansible_role_exim4/actions?query=workflow%3A%22Ansible+check+debian%3Astable%22) | [ansible test with debian stable](https://github.com/marketplace/actions/check-ansible-debian-stable) |
| [![Ansible check debian:latest](https://github.com/do1jlr/ansible_role_exim4/workflows/Ansible%20check%20debian:latest/badge.svg)](https://github.com/do1jlr/ansible_role_exim4/actions?query=workflow%3A%22Ansible+check+debian%3Alatest%22) | [ansible test with debian latest](https://github.com/marketplace/actions/check-ansible-debian-latest) |
| [![Ansible check debian:sid](https://github.com/do1jlr/ansible_role_exim4/workflows/Ansible%20check%20debian:sid/badge.svg)](https://github.com/do1jlr/ansible_role_exim4/actions?query=workflow%3A%22Ansible+check+debian%3Asid%22) | [ansible test with debian sid](https://github.com/marketplace/actions/check-ansible-debian-sid) |
| [![Ansible check debian:buster](https://github.com/do1jlr/ansible_role_exim4/workflows/Ansible%20check%20debian:buster/badge.svg)](https://github.com/do1jlr/ansible_role_exim4/actions?query=workflow%3A%22Ansible+check+debian%3Abuster%22) | [ansible test with debian buster](https://github.com/marketplace/actions/check-ansible-debian-buster) |
| [![Ansible check debian:stretch](https://github.com/do1jlr/ansible_role_exim4/workflows/Ansible%20check%20debian:stretch/badge.svg)](https://github.com/do1jlr/ansible_role_exim4/actions?query=workflow%3A%22Ansible+check+debian%3Astretch%22) | [ansible test with debian stretch](https://github.com/marketplace/actions/check-ansible-debian-stretch) |
| | |
| [![Ansible check ubuntu:latest](https://github.com/do1jlr/ansible_role_exim4/workflows/Ansible%20check%20ubuntu:latest/badge.svg)](https://github.com/do1jlr/ansible_role_exim4/actions?query=workflow%3A%22Ansible+check+ubuntu%3Alatest%22) | [ansible test with ubuntu latest](https://github.com/marketplace/actions/check-ansible-ubuntu-latest) |
| [![Ansible check ubuntu:bionic](https://github.com/do1jlr/ansible_role_exim4/workflows/Ansible%20check%20ubuntu:bionic/badge.svg)](https://github.com/do1jlr/ansible_role_exim4/actions?query=workflow%3A%22Ansible+check+ubuntu%3Abionic%22) | [ansible test with ubuntu bionic](https://github.com/marketplace/actions/check-ansible-ubuntu-bionic) |
| | |
| [![Ansible check centos:latest](https://github.com/do1jlr/ansible_role_exim4/workflows/Ansible%20check%20centos:latest/badge.svg)](https://github.com/do1jlr/ansible_role_exim4/actions?query=workflow%3A%22Ansible+check+centos%3Alatest%22) | [ansible test with centos latest](https://github.com/marketplace/actions/check-ansible-centos-latest) |
| [![Ansible check centos:centos8](https://github.com/do1jlr/ansible_role_exim4/workflows/Ansible%20check%20centos:centos8/badge.svg)](https://github.com/do1jlr/ansible_role_exim4/actions?query=workflow%3A%22Ansible+check+centos%3Acentos8%22) | [ansible test with centos centos8](https://github.com/marketplace/actions/check-ansible-centos-centos8) |
| [![Ansible check centos:latest](https://github.com/do1jlr/ansible_role_exim4/workflows/Ansible%20check%20centos:centos7/badge.svg)](https://github.com/do1jlr/ansible_role_exim4/actions?query=workflow%3A%22Ansible+check+centos%3Acentos7%22) | [ansible test with centos centos7](https://github.com/marketplace/actions/check-ansible-centos-centos7) |
