# yauh.rundeck
Ansible role for setting up Rundeck job scheduler and runbook automation

## Requirements
SSH access to the remote machine

## Role Variables

```
rundeck_deb_url: http://dl.bintray.com/rundeck/rundeck-deb/
rundeck_deb_package: rundeck-2.5.2-1-GA.deb
rundeck_deb_package_sha: 4f801d8ffed357c9d592dd082a431f32637cbdbc
rundeck_config_properties:
  - key: grails.serverURL
    value: http://rundeck.local:4440
  - key: loglevel.default
    value: VERBOSE
rundeck_users:
  - name: root
    password: password
    roles:
      - admin
      - architect
      - deploy
      - build
      - user
```

## Dependencies
yauh.java8

## Example Playbook
Including an example of how to use your role (for instance, with variables passed in as parameters) is always nice for users too:

```
- hosts: all
  roles:
     - { role: yauh.rundeck }
```

## License
BSD

## Author Information
Stephan Hochhaus stephan@yauh.de

[https://github.com/yauh](https://github.com/yauh)
